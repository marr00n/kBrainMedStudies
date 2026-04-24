Based of: [The Best Way to Acquire Knowledge from Readings](https://medium.com/heptabase?source=post_page---publication_nav-7c6e8629fd5e-abf9357814d1---------------------------------------)
Claude Discussion: [Claude](https://claude.ai/chat/6ef015e4-ca6c-4394-b0de-9818b9fd70bc)
# Obsidian Study Method (Optimist Revision)

## Core Principle
- Deep understanding comes from the *process* of articulating and re-describing knowledge — not from producing polished notes
- The highest-value cognitive task is writing descriptive titles that capture the core claim; optimise your time for this
- Offload mechanical work (splitting, collating) to an LLM so your limited study time is spent on thinking, not formatting

## Phase 1 — Read and Highlight (Source Capture)
- No change from original method
- Open PDF chapter in Obsidian via PDF++
- Highlight liberally on first pass — flag anything important, surprising, or connecting to prior knowledge
- Capture highlights into a single markdown note per chapter
  - Title format: `Highlights — [Topic] — [Source]`
- This is your literature card; selectivity comes later

## Phase 2 — Atomise into Concept Notes (LLM-Assisted)
- Feed the highlights note to an LLM with instructions to:
  - Split the highlights into atomic concept notes (one concept per note)
  - Give it an 'Title pending' for each note so you do the work of summarising the information.
  - Preserve the original highlight text as the note body
- Review each LLM-generated note:
  - **Accept** the draft title if it genuinely captures the core claim in one sentence
  - **Rewrite** the title if it feels vague, too broad, or doesn't pass the recall test (could you recall the concept from the title alone in six months?)
  - **Reject and merge/split** if the LLM drew the concept boundaries in the wrong place
- Track which titles you rewrote — these are your weak spots and signal where to invest more attention
- Title test remains the same:
  - ❌ "Baroreceptor reflex"
  - ✅ "The baroreceptor reflex buffers acute BP changes via vagal and sympathetic modulation of HR and vascular tone"
- After reviewing titles, add your own annotations or reworded explanations beneath the highlight text where it helps your understanding
- Heuristic: if you want a second heading inside a note, it still needs splitting

```
# Role
You are a study assistant helping an anaesthetics registrar atomise highlighted textbook content into concept notes for an Obsidian vault.

# Input
You will receive a markdown document containing highlighted passages from a single textbook chapter. The highlights are roughly sequential and may follow the chapter's section structure.

# Task
Split the highlights into atomic concept notes. Each concept note must contain exactly one concept.

For each concept note, produce a **body** based on the original highlight text. Lightly rewrite the highlights so they read as complete, coherent sentences — fill in implied subjects, link sentence fragments, and resolve dangling references (e.g. "this drug" → name the drug). Do not add new clinical information, interpretation, or commentary beyond what is stated or clearly implied in the source text. If a highlight already reads as a complete sentence, leave it alone.

Do not draft titles. The user will add titles manually after review.

# Output Format
Return the concept notes as a single markdown document using the horizontal rule (---) as the delimiter between notes.

[Concept note A]

---

[Concept note B]

---

# Rules
- One concept per note. If a passage contains two distinct ideas, create two notes.
- If multiple non-adjacent highlights support the same concept, merge them into one note.
- Rewriting must be minimal and faithful. Keep the source text's terminology, phrasing, and level of detail. The goal is readability, not paraphrasing.
- Include any adjacent user written notes, and process them with the highlights
- Do not add explanations, annotations, or commentary. The user will add their own annotations later.
- Do not omit or summarise any highlight content. Every highlighted passage must appear in at least one concept note.

# Context
The user is an anaesthetics registrar studying at clinical registrar level, not primary exam depth. The source text is from the Ottawa Anesthesia Primer or equivalent clinical teaching texts.

# Input Document
[Paste highlights document here]
```
## Phase 3 — Spatial Mapping on Canvas
- No change from original method
- Open an Obsidian canvas and drag concept notes onto it
- Arrange notes spatially — related concepts close together
- Draw arrows to show causal or sequential relationships
- Group clusters into named sections
  - Name sections with the same care as concept note titles — these are what you scan first on review
- Friction here (e.g. can't articulate a connection) signals gaps in understanding — that's the learning
- For cross-source integration: reuse concept notes from previous sessions on the same canvas

## Phase 4 — Write a Summation Note
- No change from original method
- Write a new note synthesising your understanding in your own words
- For clinical content: use OHA-style note format for concise reference structure
- Wikilink to concept notes rather than duplicating their content
- The summation is the narrative thread stitching atomic concepts into a coherent whole

## Phase 5 — Generate Anki Cards
- No change from original method
- Feed summation note or concept notes into Anki flashcard workflow
- Concept notes are ideal input — already atomic, each maps to one or a few cards
- One-sentence titles make strong cloze deletion candidates

## Key Pitfall to Avoid
- Do not rubber-stamp LLM draft titles without engaging critically — passive acceptance defeats the purpose
- The time saved by automating the split should be reinvested into title review and annotation, not skipped entirely
- If you find yourself accepting every draft title without change, slow down — you're likely not thinking hard enough about what the concept actually means