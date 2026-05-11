---
name: generating-anki-flashcards
description: "Generates Anki-ready flashcards (basic and cloze) from study material, saved as CSV files ready to import into Anki. Use when the user says \"make cards from this\", \"create flashcards\", \"make Anki cards\", or \"help me revise this\". Use for any spaced repetition or active recall card creation request."
model: sonnet
---

## How to Make Flashcards
1. Receive input and read the material
2. Apply the card creation approach to each block (→ see below)
3. **Deduplication check**: Review all generated cards. For each fact, confirm it appears in only one card type. If the same fact appears as both a basic and a cloze card, keep only the cloze version.
4. Format as CSV — wrap any field containing a tab in double quotes (see CSV Escaping Rules)
5. Save files and report to user

---

## Approaching Each Block of Content

### Thinking Process

Apply these steps to every piece of content before generating cards:
1. Identify the key facts.
2. Split into the smallest testable units.
3. Decide on Card Type for each unit.
4. Write flashcards following the card writing principles.
5. Ensure clarity and no overlap between cards.

### Card Type Decision Rules
Never mix multiple unrelated ideas in one card. Split into several cards instead.

**Default to CLOZE.** Cloze is the primary card type. Every fact should be considered for cloze first. Only use basic cards when cloze genuinely cannot express the knowledge well.

**Use CLOZE cards for:**
- Specific values, doses, thresholds, durations, percentages, definitions, classifications, time distinctions, severity gradings — virtually any discrete fact.
- Any fact where the answer is a short phrase that fits naturally inside a sentence.
- Groups of related facts that can be tested together with multiple cloze deletions (e.g. severity grades, time-based classifications).
- Example: "The induction dose of propofol is {{c1::2–2.5 mg/kg}} in healthy adults."

**Use BASIC (front–back) cards only when:**
- The answer is a longer conceptual explanation that cannot be reduced to a fill-in-the-blank.
- The answer is an open-ended list of 3+ items where cloze deletions would be unwieldy (causes of…, complications of…, differentials for…).
- The question requires a qualitative or comparative answer that doesn't fit cloze syntax.
- Example: "What are the causes of intra-operative hypotension?" → list on the back.

### CRITICAL — No Fact Duplication Across Card Types

**Each fact must appear in exactly one card type.** If a fact is expressed as a cloze card, it must NOT also appear as a basic card (or vice versa). This is the single most important rule for avoiding bloated, redundant decks.

Before finalising output, review every basic card and check: "Is this same fact also covered by a cloze card?" If yes, delete the basic card. The cloze version is almost always the better card for recall of discrete facts.

### Card Writing Principles

These rules are derived from Wozniak's SuperMemo research and apply to every card generated.

#### Atomic knowledge
- One concept per card — never cram multiple facts into one
- If a back requires more than one sentence, split into multiple cards
- Test one thing; if you need "and", make two cards

#### Minimum information
- Keep fronts short and unambiguous — one clear correct answer
- Remove filler words; use active voice
- Add a subject prefix for disambiguation: `Suxamethonium — onset?` not `What is the onset of suxamethonium?`

#### Avoid lists
- Never put a list of 4+ items on a card — it's nearly impossible to retain reliably
- For list-type answers, decide based on likely recall need:
  - Items recalled **individually** → one card per item
  - List recalled **as a whole** → one card with the full list on the back
  - Both needed → make both (see Redundancy for critical concepts)
- If a classification must be tested as a whole, use a cloze with multiple gaps

#### Combat interference
- When two items are similar (e.g. two drugs with similar doses), add a distinguishing cue to each card's front
- Example: `Rocuronium (non-depolarising) — intubating dose?` vs `Suxamethonium (depolarising) — intubating dose?`

#### Context cues
- Add the subject domain to the front where it aids retrieval without adding noise
- Example: `Pharmacology: MAC of sevoflurane in adults?` vs just `MAC of sevoflurane?`
- Use sparingly — only when ambiguity or interference is likely

#### Redundancy for critical concepts
- For high-yield facts, generate the same concept from 2–3 angles using **different question framing** — but always using the same card type (chosen per the decision rules above)
- **Never generate both a basic and a cloze card for the same fact.** Pick one type per fact and commit to it. If a fact works as a cloze (and most discrete facts do), it must only be a cloze.
- Don't overdo — reserve for concepts that genuinely require deep encoding

#### Understand before memorising
- If the source material is unclear or appears to contain errors, flag it before generating cards
- Don't generate cards from content that hasn't been understood — they won't stick

---

## General Quality Rules
- If a detail is not in the source text, do not invent it.

---

## Duplicate Awareness

Anki uses the first field to detect duplicates. Ensure the Front (basic) or Text (cloze) field is unique for every card. Do not create two cards with identical first fields.

---

## Output Format

Output is **two CSV files**, saved to disk:
- `cards_basic.csv` — for Basic (and reversed card) notes
- `cards_cloze.csv` — for Cloze notes

Only create a file if there are cards of that type. If only basic cards were generated, only produce `cards_basic.csv`.

Each file **must begin with Anki file headers** (lines starting with `#`) before any card data.

After the headers, each line is one card. No preamble, no commentary, no numbering — only header lines then data lines.

### cards_basic.csv

```
#separator:tab
#html:true
#tags column:3
#columns:Front	Back	Tags
#notetype:_Basic - DecEyeStrain
Suxamethonium — NMB class?	Depolarising neuromuscular blocker	anaesthetics::pharmacology::nmb
```

- **Note type**: `Basic (and reversed card)` — Anki automatically generates both forward and reverse cards from a single row. Do not manually output reverse pairs; one row per concept is correct.
- **Columns**: Front, Back, Tags
- **Tags**: space-separated if multiple (e.g. `"anaesthetics::pharmacology tag2"`)

### cards_cloze.csv

```
#separator:tab
#html:true
#tags column:3
#columns:Text	Extra	Tags
#notetype:_Cloze - DecEyeStrain
Suxamethonium has an onset of {{c1::60 seconds}} and duration of {{c2::10–15 minutes}}.		anaesthetics::pharmacology::nmb
```

- **Note type**: `Cloze`
- **Columns**: Text, Extra, Tags

### CSV formatting rules

- UTF-8 encoding
- Use `<br>` for line breaks within a field
- The `#` header lines must appear before any data rows

---

## CSV Escaping Rules

**CRITICAL -- Never use tab characters inside field content.** The CSV delimiter is a tab. Do not insert literal tab characters within any field.

- When listing items inside a field (causes, complications, features), separate them with commas.
- The only tab characters in the file are the column delimiters between fields.
- If a field contains a double-quote, wrap the **entire field** in double quotes and escape each inner double-quote by doubling it.
- Semicolons are now safe to use freely inside field content (they are no longer the delimiter).
- Examples:
  - `one[TAB]two[TAB]three` -- tabs here are column delimiters (correct)
  - `<b>Causes of hypotension</b>[TAB]Hypovolaemia, vasodilation, cardiac depression[TAB]tag` -- list items separated by commas (correct)
  - `one[TAB]"she said ""hello"""[TAB]three` -- escaped quotes inside field (correct)

**Newline rule:** Escaped multi-line fields using literal newlines do not work correctly with cloze deletions in Anki. Always use `<br>` for line breaks inside fields. Never use literal newlines within a field.

---

## Field Rules

**Basic cards:**
- **Front:** A clear question.
- **Back:** The answer. Use HTML for formatting (`<br>`, `<ul><li>`), not Markdown.

**Cloze cards:**
- **Text:** One or two clozes in Anki syntax. Example: `The induction dose of propofol is {{c1::2–2.5 mg/kg}} in healthy adults.`
- **Extra:** Optional short explanation or context (≤ 25 words), or leave blank.
- Use `c1`, `c2`, etc. for multiple clozes in one card.

---

## Formatting Rules

- Use HTML for any formatting inside fields: bold `<b>`, italic `<i>`, line breaks `<br>`, underline <u>, lists `<ul><li>`. Do not use Markdown syntax.
- For mathematical or scientific notation, use LaTeX wrapped in Anki's MathJax delimiters: `\( inline \)` or `\[ display \]`.
- Use all symbols as literal characters — do not escape them as HTML entities. Anki renders these natively. This includes but is not limited to: `<`, `>`, `&`, `°`, `≥`, `≤`, `±`, `→`, `←`, `↑`, `↓`, `×`, `÷`, `≠`, `α`, `β`, `γ`, `μ`, `∆`. Never write `&lt;`, `&gt;`, `&amp;`, `&deg;`, `&ge;`, `&le;` or any other named or numeric HTML entity.

---
### Application of Bold, Italics, Underlines

These apply to **both Basic back fields and Cloze Text fields**. Do not skip formatting on cloze cards.

- Bold
  - Put on the cards subject matter
  - Use for one item only where possible
- Italics
  - Use for hints that would help reconstruct the answer
  - Use for common exam wording or framing
  - Use for contrast pairs and commonly confused concepts
  - Use for one item only where possible
- Underline
  - Use for the exact examinable answer 

Example (Basic back field):
The most likely <b>acid–base disorder in salicylate toxicity</b> is <u>mixed respiratory alkalosis and metabolic acidosis.</u>
<i>Early salicylate toxicity often stimulates the respiratory centre.</i>
<i>Not an isolated metabolic acidosis</i>.

Example (Cloze Text field):
<b>Suxamethonium</b> has an onset of {{c1::<u>60 seconds</u>}} and a duration of {{c2::<u>10–15 minutes</u>}}. <i>Metabolised by plasma cholinesterase.</i>
---

## Tag Conventions

Identify the primary, secondary, and tertiary focus of the card. Then, apply as many tags as possible.
Tags are lowercase.
Replace spaces in tags with underscores. e.g. `hello world` -> `hello_world`.
Multiple tags are separated by spaces (not semicolons).
Tags use `::` notation for hierarchy. Multiple tags are space-separated within the Tags field.

### Anaesthetics content — ANZCA Primary Exam

**Assume content is for the ANZCA Primary Exam unless told otherwise**, therefore use the curriculum-mapped tags from:
`references/anzca-primary-curriculum-tags.md`

This file contains:
- A tag for every curriculum section and subsection (e.g. `anzca::primary::respiratory::physiology::gas_transport`)
- A learning outcome code tag format (e.g. `anzca::code::BT_PO_1.31`)
- A quick-reference table of code prefixes
- A worked example

Apply **both** a section tag and a code tag where the learning outcome is identifiable. See that file for full instructions.

### General subject tags (when told that the content is non-ANZCA)

| Subject area | Tag |
|---|---|
| Anaesthetics (general) | `anaesthetics` |
| Pharmacology | `anaesthetics::pharmacology` |
| Anatomy | `anaesthetics::anatomy` |
| Physiology | `anaesthetics::physiology` |
| Equipment | `anaesthetics::equipment` |
| Regional | `anaesthetics::regional` |
| Obstetrics | `anaesthetics::obstetrics` |
| Paeds | `anaesthetics::paeds` |

---

## Example Output

Input: *"Suxamethonium is a depolarising neuromuscular blocker. Dose is 1-2 mg/kg IV. Onset 60 seconds. Duration 10-15 minutes. Metabolised by plasma cholinesterase. Side effects include hyperkalaemia, bradycardia, malignant hyperthermia, and masseter spasm."*

Note how each fact appears in **exactly one** card type. Discrete values (dose, onset, duration, metabolism) are cloze cards. The open-ended list (side effects) is a basic card. No fact is duplicated across types.

Output: **cards_basic.csv**
```
#separator:tab
#html:true
#tags column:3
#columns:Front	Back	Tags
#notetype:_Basic - DecEyeStrain
<b>Suxamethonium</b> — side effects?	Hyperkalaemia, bradycardia, malignant hyperthermia, masseter spasm	anaesthetics::pharmacology::nmb
```

Output: **cards_cloze.csv**
```
#separator:tab
#html:true
#tags column:3
#columns:Text	Extra	Tags
#notetype:_Cloze - DecEyeStrain
<b>Suxamethonium</b> is a {{c1::<u>depolarising</u>}} neuromuscular blocker.		anaesthetics::pharmacology::nmb
The <b>IV intubating dose of suxamethonium</b> is {{c1::<u>1–2 mg/kg</u>}}.		anaesthetics::pharmacology::nmb
<b>Suxamethonium</b> has an onset of {{c1::<u>60 seconds</u>}} and duration of {{c2::<u>10–15 minutes</u>}}.		anaesthetics::pharmacology::nmb
<b>Suxamethonium</b> is metabolised by {{c1::<u>plasma cholinesterase</u>}}.		anaesthetics::pharmacology::nmb
```

---

## After generating

Tell the user:
- The file(s) saved and their paths
- How many basic and cloze cards were generated
- Import instructions: In Anki, go to **File → Import**, select the CSV, confirm the note type and field mapping, then import.