---
name: oha-medical-notes
description: >
  Transform source material (video transcripts, journal articles, presentations, lecture notes, clinical guidelines)
  into concise clinical reference notes in the style of the Oxford Handbook of Anaesthesia (OHA). Use this skill
  whenever the user provides text, a transcript, or any medical/clinical content and asks to convert it into notes,
  study notes, clinical notes, OHA-style notes, handbook-style notes, or reference notes. Also trigger when the user
  says "make notes from this", "convert this to notes", "summarise this as clinical notes", "OHA format",
  "handbook format", or pastes a block of medical text and asks for it to be tidied, restructured, or condensed.
  Even if the user doesn't explicitly say "OHA", if they provide medical content and ask for structured clinical
  notes, use this skill.
model: sonnet
---

# OHA-Style Medical Note Generation

Convert source material into clinical reference notes that emulate the *Oxford Handbook of Anaesthesia* (5th edition) in structure, voice, and formatting.

---

## Before you begin

**Read the style guide.** Before generating any notes, read the full style guide at:

```
references/style-guide.md
```

This file is the authoritative reference for voice, formatting, symbols, abbreviations, structure, and quality standards. Follow it closely — it contains specific do/don't examples, symbol tables, approved abbreviations, and transformation rules that govern every aspect of the output.

The path is relative to this skill's directory. Use the `view` tool to read it.

---

## Workflow

1. **Read the style guide** (see above — do this every time, no exceptions).
2. **Identify the source type**: video transcript, journal article, presentation/slides, clinical guideline, highlights file, or general prose.
3. **Identify the topic type**: disease/condition, procedure/technique, drug/agent, or emergency/acute presentation.
4. **Extract the clinical bottom line** — what does the anaesthetist need to know and do?
5. **Handle embedded images** — if the source contains image or figure references (`![[...]]` or `![](path)`), read each image using the Read tool, understand what it depicts, and plan where it belongs in the output. Do not silently drop figures.
6. **Transform** the content following the rules in the style guide (Section 5: Content Transformation Rules).
7. **Structure** using the appropriate OHA template for the topic type (Section 2.2 of the style guide). Embed figures at the contextually appropriate location with a brief italicised caption (e.g. `*Fig. 1 — FA/FI curves for common volatile agents*`).
8. **Apply formatting** — symbols, abbreviations, bullet conventions, units (Sections 3–4 of the style guide).
9. **Run the quality checklist** (Section 9 of the style guide) before presenting the output.
10. **Output** — ask the user whether they want the notes saved to a file or displayed inline in the conversation, then deliver accordingly. If context makes the preference obvious (e.g. the user specified a destination path, or said "show me"), skip asking and proceed.

---

## Output format

Output is an OHA-style clinical reference note in Markdown. It may be saved to a `.md` file or displayed inline — ask the user if not specified (see workflow step 10).

### Filename convention

Use a descriptive kebab-case filename derived from the topic:
- `aortic-stenosis.md`
- `obesity-anaesthetic-considerations.md`
- `sugammadex.md`
- `awake-tracheal-intubation.md`

### Markdown structure

```markdown
# Topic Title

Brief opening paragraph — epidemiology, pathophysiology, or definition in 2–4 sentences of prose.
This orients the reader. Keep it tight.

## Subheading (e.g. Preoperative Assessment)

- Bullet point with key information.
- Another point — use symbols (↑ ↓ → ±) to compress.
	- Nested sub-point for elaboration.
- Drug doses include route and weight-basis: "Propofol 1–2.5mg/kg IV".

## Haemodynamic Goals

- Maintain SR.
- Avoid ↓ SVR.
- Target HR 60–80bpm.

## Conduct of Anaesthesia

- Arterial line before induction.
- Slow, careful induction — titrate to effect.
- Avoid histamine-releasing agents.

---
*Source: [source description — e.g. "Dr Smith, Grand Round presentation, March 2026"]*
```

### Key formatting rules (summary — the style guide has full detail)

- **Bullets** are the primary unit of information. Use `- ` for top-level; tab + `- ` for nested sub-points.
- **Symbols**: ↑ ↓ → ← ± ≥ ≤ ~ used liberally to compress text.
- **Units** always attached, no space: `70kg`, `5mL`, `100mmHg`.
- **British English** throughout: anaesthesia, haemoglobin, oesophagus.
- **OHA terminology**: tracheal tube (TT), supraglottic airway (SGA), flexible optical bronchoscope (FOB), awake tracheal intubation (ATI), cricoid force, CICO, eFONA.
- **Abbreviations**: common anaesthetic abbreviations used freely (HR, BP, MAP, SpO2, FiO2, GA, RSI, etc.). Less common ones defined on first use.
- **Cross-references**: use wikilinks — `(see [[Massive Transfusion]])`.
- **En-dash for ranges**: `6–10mmol/L`, `1–2mg/kg`.
- **Time abbreviations**: sec, min, hr, d, wk, mo, yr.

### Topic-type templates

Choose the appropriate structure based on what the source material covers:

**Disease/Condition** → Opening paragraph → Clinical relevance → Preoperative assessment → Investigations → Perioperative management → Haemodynamic goals → Postoperative care → Special considerations

**Procedure/Technique** → Indications → Contraindications → Equipment/preparation → Technique (step-by-step) → Complications and management → Tips/pitfalls

**Drug/Agent** → Class/mechanism → Indications → Dose (adult ± paediatric) → Onset/duration → Cautions/CI → Side effects → Notes

**Emergency/Acute** → Use the summary box format (see style guide Section 6)

---

## Content transformation principles

These are the core rules for converting source material. The style guide (Section 5) has full detail and examples.

1. **Extract the clinical bottom line first.** What does the anaesthetist need to know and do?
2. **Strip teaching scaffolding.** Remove "Today we're going to talk about...", "As you can see...", "This is really important because...".
3. **Collapse repetition.** If a point is made three ways, state it once.
4. **Convert prose to bullets.** Anything that can be a bullet, should be.
5. **Replace verbose phrases with symbols** (↑ ↓ → ± ≥ ≤, 2° to, etc.).
6. **Preserve numerical precision.** Doses, thresholds, measurements — keep them exact.
7. **Maintain clinical nuance.** "Consider" vs "always" — preserve the distinction.

### Source-specific handling

- **Video transcripts**: Discard fillers, self-corrections, tangents. Identify core teaching points (often signposted by emphasis or repetition). Restructure into logical OHA sections regardless of presentation order.
- **Journal articles**: Focus on methods, key results (numbers), and clinical implications. Convert findings into actionable clinical statements.
- **Presentations/slides**: Slide titles often map to subheadings. Tighten existing bullet points further. Use speaker notes for nuance if available.
- **Highlights files (Obsidian)**: Source will contain a mix of quoted textbook passages, user annotations, and embedded image references. Treat user annotations as primary — they reflect the user's own understanding and should be incorporated faithfully. For each image reference (`![](path)` or `![[...]]`), read the image, identify what it shows (graph, diagram, table, figure), and embed it in the output at the point where the surrounding text calls for it. Adjust the image path to be correct relative to the output file's location. Add a brief italicised caption beneath each image describing what it depicts.

---

## What good output looks like

### Example: Obesity & Anaesthesia (from a verbose transcript)

**Input** (excerpt):
> "So when we're thinking about obese patients, one of the really key things to remember is that their functional residual capacity is already reduced when they're awake, right? And then when you induce them, it drops even further..."

**Output** (excerpt):
```markdown
## Respiratory Considerations

• FRC is ↓ in awake obese patients and ↓↓ following induction → may encroach upon closing capacity.
• O2 consumption is ↑ by metabolically active adipose tissue, with associated ↑ CO2 production.
• O2 desaturation occurs rapidly in the obese, apnoeic patient.
```

---

## After generating

Present the `.md` file to the user and tell them:
- The filename and topic covered
- A one-line summary of what was generated (e.g. "OHA-style notes on aortic stenosis covering preop assessment, haemodynamic goals, and conduct of anaesthesia")
- If the source material was ambiguous or incomplete, flag what was unclear or what you had to infer