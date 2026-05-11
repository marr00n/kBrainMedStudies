# Arterial Blood Gas Interpretation

The ABG provides a real-time window into a patient's acid-base status, respiratory function, and metabolic compensation. Systematic interpretation — applied consistently — prevents errors and unmasks mixed disorders that may be missed on clinical grounds alone.

---

## Key Reference Values

| Parameter | Normal Range |
|-----------|-------------|
| pH | 7.35–7.45 |
| PaCO<sub>2</sub> | 35–45mmHg |
| HCO<sub>3</sub><sup>−</sup> | 22–26mmol/L |
| Base excess (BE) | −2 to +2mmol/L |
| PaO<sub>2</sub> | 10–13kPa (75–100mmHg) |

---

## The Core Rule: Direction of Effect

Memorise these two relationships before anything else:

- **CO<sub>2</sub> is an acid** → CO<sub>2</sub> ↑ → pH ↓; CO<sub>2</sub> ↓ → pH ↑
	- CO<sub>2</sub> and pH move in **opposite** directions.
- **HCO<sub>3</sub><sup>−</sup> is a base** → HCO<sub>3</sub><sup>−</sup> ↑ → pH ↑; HCO<sub>3</sub><sup>−</sup> ↓ → pH ↓
	- HCO<sub>3</sub><sup>−</sup> and pH move in the **same** direction.

---

## Step-by-Step Interpretation Algorithm

### Step 1 — Identify the pH disturbance
- pH <7.35 → **acidosis**
- pH >7.45 → **alkalosis**

### Step 2 — Identify the primary cause
Ask: which parameter is abnormal in the direction that explains the pH?

| pH | CO<sub>2</sub> | HCO<sub>3</sub><sup>−</sup> | Primary disorder |
|----|------|-------|-----------------|
| ↓ | ↑ | Normal/↑ | Respiratory acidosis |
| ↓ | Normal/↓ | ↓ | Metabolic acidosis |
| ↑ | ↓ | Normal/↓ | Respiratory alkalosis |
| ↑ | Normal/↑ | ↑ | Metabolic alkalosis |

### Step 3 — Check for appropriate compensation
The body attempts to restore pH towards normal — never fully correcting it. If compensation exceeds or falls short of expected, a concurrent independent process is present.

### Step 4 — Calculate the anion gap (if metabolic acidosis)
See below.

### Step 5 — Interpret in clinical context
Correlate with SpO<sub>2</sub>, lactate, electrolytes, and clinical picture.

---

## Compensation Rules

### Metabolic acidosis → Respiratory compensation (↓ CO<sub>2</sub>)

Use **Winter's Formula:**

> **Expected PaCO<sub>2</sub> = (1.5 × HCO<sub>3</sub><sup>−</sup>) + 8 ± 2**

- Actual CO<sub>2</sub> > expected → concurrent **respiratory acidosis**
- Actual CO<sub>2</sub> < expected → concurrent **respiratory alkalosis**

### Respiratory acidosis → Metabolic compensation (↑ HCO<sub>3</sub><sup>−</sup>)

| Type | Expected HCO<sub>3</sub><sup>−</sup> rise per 10mmHg ↑ CO<sub>2</sub> |
|------|------|
| Acute | ~1mmol/L |
| Chronic | ~3–4mmol/L |

- Minimal HCO<sub>3</sub><sup>−</sup> rise → **acute** (kidneys not yet compensated)
- Substantial HCO<sub>3</sub><sup>−</sup> rise → **chronic** (days of renal adaptation)

### Respiratory alkalosis → Metabolic compensation (↓ HCO<sub>3</sub><sup>−</sup>)
- In pure respiratory alkalosis with appropriate compensation, HCO<sub>3</sub><sup>−</sup> should be **↓**.
- If HCO<sub>3</sub><sup>−</sup> is ↑ in the context of ↓ CO<sub>2</sub> → mixed respiratory + metabolic alkalosis.

---

## Identifying Mixed Disorders

- **Compensation** → one parameter is abnormal in a direction that *corrects* the pH.
- **Mixed disorder** → both CO<sub>2</sub> and HCO<sub>3</sub><sup>−</sup> are abnormal in directions that *worsen* the pH (or both push it the same way in alkalosis).

> Mixed acidosis = ↓ pH + ↑ CO<sub>2</sub> + ↓ HCO<sub>3</sub><sup>−</sup> → both systems driving acidosis. Use Winter's formula to confirm — if actual CO<sub>2</sub> > expected, concurrent respiratory acidosis is present.

---

## The Anion Gap

Used to classify metabolic acidosis once identified. Quantifies unmeasured anions in plasma.

> **AG = Na<sup>+</sup> − (Cl<sup>−</sup> + HCO<sub>3</sub><sup>−</sup>)**

**Normal AG: 8–12mmol/L**

| AG | Interpretation | Mnemonic |
|----|---------------|---------|
| ↑ (>12) | Unmeasured acid accumulating | **MUDPILES** |
| Normal (8–12) | Loss of HCO<sub>3</sub><sup>−</sup> or gain of Cl<sup>−</sup> | **HARDUP** |

### High Anion Gap — MUDPILES
- **M**ethanol
- **U**raemia
- **D**iabetic ketoacidosis
- **P**ropylene glycol
- **I**soniazid/Iron
- **L**actic acidosis *(most common perioperatively)*
- **E**thylene glycol
- **S**alicylates

### Normal Anion Gap — HARDUP
- **H**yperchloraemia *(e.g. large-volume 0.9% NaCl resuscitation)*
- **A**ddison's disease
- **R**enal tubular acidosis
- **D**iarrhoea *(HCO<sub>3</sub><sup>−</sup> loss)*
- **U**reteric diversion
- **P**ancreatic fistula

---

## Advanced Considerations

### Albumin correction
Normal AG assumes albumin ~40g/L (major unmeasured anion). In hypoalbuminaemia — common in sick perioperative patients — AG is falsely ↓.

> **Corrected AG = measured AG + 0.25 × (40 − albumin g/L)**

Apply before concluding AG is normal in a critically ill patient.

### Delta ratio
Used in high AG metabolic acidosis to detect a concurrent normal AG acidosis or metabolic alkalosis hidden beneath.

> **Delta ratio = (AG − 12) / (24 − HCO<sub>3</sub><sup>−</sup>)**

- <0.4 → concurrent normal AG acidosis
- 0.4–1 → mixed high + normal AG acidosis
- 1–2 → pure high AG acidosis
- >2 → concurrent metabolic alkalosis

---

## Summary Algorithm (Quick Reference)

```
pH low → acidosis
  ├─ CO₂ ↑ → Respiratory acidosis
  │     └─ Check HCO₃⁻: acute (~1mmol/L per 10mmHg) vs chronic (~3–4mmol/L per 10mmHg)
  └─ HCO₃⁻ ↓ → Metabolic acidosis
        ├─ Apply Winter's formula → is CO₂ appropriate?
        └─ Calculate anion gap
              ├─ High → MUDPILES
              └─ Normal → HARDUP

pH high → alkalosis
  ├─ CO₂ ↓ → Respiratory alkalosis
  │     └─ Expect HCO₃⁻ ↓ as compensation; if HCO₃⁻ ↑ → mixed alkalosis
  └─ HCO₃⁻ ↑ → Metabolic alkalosis
        └─ Expect CO₂ ↑ as compensation

Both systems worsening pH → Mixed disorder
```

---

*Source: Claude Tutorial session — systematic ABG interpretation, May 2026*
