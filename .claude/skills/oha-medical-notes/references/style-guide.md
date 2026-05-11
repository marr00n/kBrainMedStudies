# Oxford Handbook of Anaesthesia (OHA) — Style Guide for LLM Note Generation

> **Purpose:** This document defines the structure, voice, formatting, and conventions used in the *Oxford Handbook of Anaesthesia* (5th edition). It is intended as a system-level reference for an LLM tasked with converting medical education content (video transcripts, journal articles, presentations, etc.) into clinical reference notes that emulate the OHA style.

## 1. Voice & Tone

### 1.1 Core Principles

* **Authoritative but concise.** Write as a senior clinician briefing a competent trainee. Assume the reader has baseline medical knowledge.
* **Imperative and direct.** Use commands: "Maintain SR", "Avoid hypotension", "Consider an arterial line". Do not hedge unnecessarily.
* **Clinically pragmatic.** Prioritise actionable information over exhaustive explanation. The reader needs to *do*something, not write an essay.
* **Economical with words.** Every sentence should earn its place. Strip filler, qualifiers, and academic throat-clearing.

### 1.2 Sentence Style

* Prefer short, declarative sentences.
* Use fragments where meaning is clear (e.g. "Duration 10min", "Rare condition", "Use IBW").
* Passive voice is acceptable when the agent is obvious ("Blood glucose should be monitored hourly").
* Active imperatives are preferred for management ("Give IV crystalloid", "Titrate to effect").

### 1.3 What to Avoid

* Verbose academic phrasing ("It has been demonstrated in the literature that...")
* First person ("I recommend...")
* Excessive hedging ("It might possibly be worth considering...")
* Conversational fillers ("So basically...", "It's worth noting that...")
* Repetition of information already stated

## 2. Document Structure

### 2.1 Hierarchy

The OHA uses a consistent hierarchy within each topic, e.g.:

```
Chapter Title (e.g. "Cardiovascular disease")
  └─ Topic Heading (e.g. "Aortic stenosis")
       ├─ Opening paragraph (brief epidemiology/pathophysiology, 2–4 sentences)
       ├─ Subheadings as needed:
       │    ├─ History and examination
       │    ├─ Investigations
       │    ├─ Preoperative / Perioperative / Postoperative management
       │    ├─ Haemodynamic goals
       │    ├─ Conduct of anaesthesia
       │    ├─ Special considerations
       │    └─ Complications
       └─ Further reading (if applicable)
```

### 2.2 Typical Section Templates

**Disease/Condition Topic:**

1. Brief pathophysiology (1 paragraph, prose)
2. Clinical relevance to anaesthesia (why this matters perioperatively)
3. Preoperative assessment (bulleted)
4. Investigations (bulleted)
5. Perioperative management (bulleted, often with a "Haemodynamic goals" box)
6. Postoperative care (bulleted)
7. Special considerations / complications

**Procedure/Technique Topic:**

1. Indications
2. Contraindications
3. Equipment / preparation
4. Technique (step-by-step, bulleted)
5. Complications and management
6. Tips / pitfalls

**Drug/Agent Topic:**

1. Class and mechanism
2. Indications
3. Dose (adult ± paediatric)
4. Onset / duration
5. Cautions and contraindications
6. Side effects

## 3. Formatting Conventions

### 3.1 Bullet Points

The primary unit of information delivery in the OHA. Nearly all clinical content is bulleted.

* **Top-level bullets**: use `- ` (hyphen + space)
* **Nested bullets**: use a tab then `- ` for each level of indentation
* Bullets are typically 1–3 sentences. Avoid single-word bullets and avoid paragraph-length bullets.
* Start bullets with the key concept, not with filler.

**Format:**

```markdown
- Top-level point.
	- Nested sub-point for elaboration.
	- Another nested point.
- Next top-level point.
```

**Good:**

```markdown
- FRC is ↓ in awake obese patients and ↓↓ following induction → may encroach upon closing capacity.
	- O2 desaturation occurs rapidly in the obese, apnoeic patient.
```

**Bad:**

```markdown
• It is important to note that the functional residual capacity tends to
  be reduced in patients who are obese when they are awake...
```

### 3.2 Symbols & Shorthand

The OHA uses symbols extensively to compress information. Adopt these liberally:

| Symbol | Meaning                                  | Example                                      |
| ------ | ---------------------------------------- | -------------------------------------------- |
| ↑      | Increased / elevated                     | "↑ risk of arrhythmias", "i blood volume"    |
| ↓      | Decreased / reduced                      | "↓ FRC", "d SpO2"                            |
| →      | Leads to / causes / results in           | "Hypoxia → acidosis → cardiac arrest"        |
| ←      | Due to / caused by                       | "Hypotension ← vasodilation"                 |
| ±      | With or without / approximately          | "Reflux ± delayed gastric emptying", "± 10s" |
| ♂      | Male                                     | "70kg ♂"                                     |
| ♀      | Female                                   | "♀, forty, fair, fat and fertile"            |
| °      | Degree (also used for primary/secondary) | "1° survey", "2° to structural disease"      |
| ≥      | Greater than or equal to                 | "Age ≥65y"                                   |
| ≤      | Less than or equal to                    | "≤0.1% bupivacaine"                          |
| ~ or 7 | Approximately                            | "~30% of patients", "71:50 cases"            |
| %      | See (cross-reference marker)             | "see % pp. 240–1"                            |
| >      | Greater than                             | "BMI >30kg/m²"                               |
| <      | Less than                                | "AHI <5"                                     |

### 3.3 Units & Measurements

* Always include units: "BMI >30kg/m²", "HR 60–100bpm", "PaCO2 >5.9kPa"
* Use standard medical abbreviations for units: mmHg, kPa, mL, mg, kg, L, g/L, mmol/L, micrograms/kg/min
* Spell out "micrograms" (not μg) per OHA convention
* Ranges use an en-dash: "6–10mmol/L", "1–2mg/kg"
* No space between number and unit: "70kg", "5mL", "100mmHg"

### 3.4 Time Abbreviations

| Abbreviation | Meaning |
| ------------ | ------- |
| sec          | second  |
| min          | minute  |
| hr           | hour    |
| d            | day     |
| wk           | week    |
| mo           | month   |
| yr           | year    |

Examples: "MI <2mo prior", "Age >60yr", "Duration 10min", "within 12hr"

### 3.5 Frequency Abbreviations

| Abbreviation | Meaning           |
| ------------ | ----------------- |
| bd           | Twice daily       |
| tds          | Three times daily |
| qds          | Four times daily  |
| PRN          | As required       |

### 3.6 Superscript & Subscript

Use HTML inline tags for superscript and subscript where needed (standard Markdown has no native syntax for these):

| Format | HTML | Example | Renders as |
| ------ | ---- | ------- | ---------- |
| Subscript | `<sub>...</sub>` | `N<sub>2</sub>O` | N₂O |
| Superscript | `<sup>...</sup>` | `CO<sub>2</sub>` `m<sup>2</sup>` | CO₂, m² |

**Common uses:**
- Chemical formulae: `N<sub>2</sub>O`, `CO<sub>2</sub>`, `O<sub>2</sub>`
- Units with exponents: `kg/m<sup>2</sup>`, `mL/kg/min<sup>-1</sup>`
- Physiological variables: `F<sub>A</sub>`, `F<sub>I</sub>`, `PaO<sub>2</sub>` (where subscript letter is conventional notation)

### 3.7 Cross-References

The OHA uses `%` as a cross-reference symbol, followed by page numbers:

* "(see % pp. 240–1)"
* "(see % p. 79)"
* "(See also % p. 971.)"

When generating notes without page numbers, adapt this to topic references inside wikilinks:

* "(see [[**Massive transfusion**]])"
* "(see [[**OSA**]], [[**Obesity**]])"

### 3.8 Tables

Tables are used for:

* Risk stratification (e.g. cardiac risk indices, ASA grading)
* Drug comparisons (dose, onset, duration, side effects)
* Classification systems (e.g. NYHA class, Mallampati)
* Differential features (e.g. VTE vs bleeding risk factors)

Keep tables compact. Use abbreviations freely within tables. Column headers should be terse.

### 3.9 Numbered Lists

Used sparingly, primarily for:

* Sequential steps in a procedure
* Numbered indications for a drug (e.g. adrenaline: 1. Anaphylaxis, 2. Bronchodilator, 3. Positive inotrope...)
* Grading systems

## 4. Abbreviations & Acronyms

### 4.1 General Rules

* **Define on first use** within a topic, then use the abbreviation thereafter.
* Common anaesthetic abbreviations may be used without definition (see list below).
* Use abbreviations aggressively to keep notes compact.

### 4.2 Standard Abbreviations (Use Without Definition)

These are so common in anaesthesia that the OHA uses them freely:

**Cardiovascular:** HR, BP, MAP, SVR, CO, CVP, ECG, AF, SR, MI, IHD, LV, RV, LVEF, JVP, CCF, BNP, AS, AR, MR, MS, AV (atrioventricular), DCCV, CVC

**Respiratory:** SpO2, FiO2, PaO2, PaCO2, ETCO2, ETO2, FRC, FEV1, FVC, PEEP, CPAP, IPPV, RR, CXR, COPD, OSA, ARDS, V/Q, HFNO

**Anaesthetic:** GA, LA, RA, RSI, SGA, TT, ETT, VL, FOB, TIVA, TCI, MAC, NMBA, NMB, PONV, LAST

**Pharmacological:** IV, IM, SC, PO, PR, NSAID, ACE, ARB, LMWH, UFH, INR, APTT

**Monitoring & Assessment:** ABG, FBC, U&E, LFT, G&S, eGFR, BIS, POCT, TOE, CPET

**General:** BMI, DM, VTE, DVT, PE, CKD, GI, CNS, ICU, HDU, ED, WHO, NICE, ATLS

**Regional:** CNB, PNB, CSE, LIA, PDPH

### 4.3 Abbreviations Requiring Definition on First Use

Less universally known abbreviations should be defined on first use:

* BCIS (bone cement implantation syndrome)
* CICO (cannot intubate, cannot oxygenate)
* eFONA (emergency front of neck airway)
* MINS (myocardial injury after non-cardiac surgery)
* VRIII (variable-rate intravenous insulin infusion)
* HFrEF, HFpEF, HFmrEF
* ROTEM, TEG

## 5. Content Transformation Rules

### 5.1 From Verbose Source → OHA-Style Notes

When converting transcripts, articles, or presentations:

1. **Extract the clinical bottom line first.** What does the anaesthetist need to know and do?
2. **Strip the teaching scaffolding.** Remove "Today we're going to talk about...", "As you can see on this slide...", "This is really important because..."
3. **Collapse repetition.** If a point is made three ways, state it once.
4. **Convert prose to bullets.** Anything that can be a bullet, should be.
5. **Replace verbose phrases with symbols:**
   * "is associated with an increase in" → "↑"
   * "leads to a decrease in" → "↓"
   * "which can result in" → "→"
   * "with or without" → "±"
   * "greater than or equal to" → "≥"
   * "secondary to" → "2° to"
6. **Preserve numerical precision.** Keep doses, thresholds, and measurements exact.
7. **Maintain clinical nuance.** Don't oversimplify to the point of being misleading. If a source says "consider" vs "always", preserve that distinction.

### 5.2 Source-Specific Guidance

**Video transcripts:**

* Discard all verbal fillers, self-corrections, time stamps, and tangential anecdotes unless clinically relevant.
* Identify the core teaching points (often signposted by emphasis or repetition).
* Restructure into logical OHA sections regardless of the order presented.

**Journal articles:**

* Focus on methods (what was done), key results (numbers), and clinical implications.
* Omit extensive background/introduction unless it provides unique context.
* Convert findings into actionable clinical statements.

**Presentations/slides:**

* Slide titles often map to subheadings. But, restructure into logical OHA sections regardless of the order presented.
* Bullet points on slides may already be near-OHA format — tighten further.
* Speaker notes (if available) may contain the nuance missing from terse slide bullets.

### 5.3 Example Transformation

**Source (verbose transcript):**

> "So when we're thinking about obese patients, one of the really key things to remember is that their functional residual capacity is already reduced when they're awake, right? And then when you induce them, it drops even further, and what that means is that you can encroach on the closing capacity. And the other thing is that because they've got all this extra adipose tissue, their oxygen consumption is increased, and they produce more CO2 as well. So the combination of reduced FRC and increased oxygen consumption means that these patients desaturate really, really quickly during apnoea."

**Output (OHA-style):**

```
• FRC is ↓ in awake obese patients and ↓↓ following induction → may
  encroach upon closing capacity.
• O2 consumption is ↑ by metabolically active adipose tissue, with
  associated ↑ CO2 production.
• O2 desaturation occurs rapidly in the obese, apnoeic patient.
```

## 6. Emergency/Quick-Reference Format

For acute presentations and emergencies, the OHA uses a distinctive summary box format:

```
| Condition     | Brief pathophysiology description                    |
| Presentation  | Key clinical features, vital sign changes             |
| Immediate action | First-line interventions                          |
| Follow-up action | Second-line treatments                            |
| Investigations | Relevant tests                                      |
| Also consider | Differential diagnoses                               |
```

Example:

```
| Condition     | IgE-mediated type 1 hypersensitivity → histamine and  |
|               | serotonin release from mast cells and basophils        |
| Presentation  | ↑ HR, ↓ BP, rash, wheeze, oedema                      |
| Immediate action | Remove trigger. 100% O2. Elevate legs + fluid      |
|               | resuscitation. IV adrenaline 20–50 micrograms          |
| Follow-up     | Chlorphenamine 10–20mg. Hydrocortisone 100–300mg       |
| Investigations | Plasma tryptase; directed allergy testing, ABG        |
| Also consider | Airway obstruction, asthma, tension pneumothorax,      |
|               | sepsis, cardiogenic shock                              |
```

## 7. Drug Formulary Format

When summarising drugs, use this structured format:

```
**Drug Name**
- Class/mechanism: [brief description]
- Indications: [numbered if multiple distinct uses]
- Dose (adult): [route, dose, frequency]
- Dose (paediatric): [if applicable]
- Onset/duration: [e.g. "Onset 30s. Duration 10min"]
- Cautions/CI: [key contraindications]
- Side effects: [key adverse effects]
- Notes: [practical pearls — e.g. "Use IBW", "Give via central line"]
```

## 8. Spelling & Terminology

* **British English spelling** throughout: anaesthesia (not anesthesia), oesophagus, haemoglobin, colour, theatre, etc.
* **Preferred OHA terminology:**
  * Tracheal tube (TT), not endotracheal tube (ETT)
  * Supraglottic airway (SGA), not supraglottic airway device (SAD)
  * Flexible optical bronchoscope (FOB), not fibreoptic bronchoscope
  * Awake tracheal intubation (ATI), not awake fibreoptic intubation (AFOI)
  * Cannot intubate, cannot oxygenate (CICO), not "can't intubate, can't ventilate"
  * Cricoid force, not cricoid pressure
  * Front of neck airway (FONA) / emergency FONA (eFONA)
* **Drug names:** Use generic (non-proprietary) names. Brand names in parentheses or with ™/® where needed: "i-gel®", "LMA ProSeal™"

## 9. Quality Checklist

Before finalising OHA-style notes, verify:

* [ ] Every bullet adds unique, actionable information
* [ ] Abbreviations are used consistently (defined on first use if not standard)
* [ ] Symbols (↑ ↓ → ± ≥ ≤) are used to compress where possible
* [ ] Units are attached to all numerical values
* [ ] British English spelling throughout
* [ ] Haemodynamic goals are presented as a discrete, terse list where relevant
* [ ] Drug doses include route, weight-basis, and frequency
* [ ] Warnings/cautions are explicit and prominent (e.g. "NEVER go without insulin" for type 1 DM)
* [ ] Content is structured in the standard OHA section order for the topic type
* [ ] Source teaching scaffolding has been fully removed
* [ ] No sentence exceeds ~30 words without good reason
* [ ] Does not include horizontal rules e.g. `---`