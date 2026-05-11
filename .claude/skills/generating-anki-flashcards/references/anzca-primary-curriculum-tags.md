# ANZCA Primary Exam — Curriculum Tag Reference

**Purpose:** When generating Anki flashcards for anaesthetics content that falls within the ANZCA Primary Exam scope, apply two independent tag layers to each card.

---

## Two Tag Layers — Separate Systems

These serve different purposes and are applied independently.

### Layer 1 — Section tag
A hierarchical topic tag for browsing cards by subject in Anki.
Format: `anzca::primary::<section>[::subsection]`
Example: `anzca::primary::respiratory::physiology::gas_transport`

### Layer 2 — Code tag
A curriculum traceability tag that identifies the specific ANZCA learning outcome the card maps to.
Format: `anzca::code::<CODE>` — with the space in the code replaced by an underscore.
Example: `anzca::code::BT_PO_1.31`

Both tags are applied to the same card, space-separated:
```
anzca::primary::respiratory::physiology::gas_transport anzca::code::BT_PO_1.31
```

Use the **Complete Code Index** below to:
1. Identify what a code refers to (learning outcome description)
2. Determine which section tag to pair with it

---

## Complete Code Index

Organised by curriculum section. Each entry shows: **Code → Learning outcome → Section tag to apply**

---

### 1. Applied Procedural Anatomy

#### 1a. Airway / Respiratory
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_AM 1.1 | Anatomy of upper airway, larynx and trachea — innervation and endoscopic appearance | `anzca::primary::anatomy::airway` |
| BT_RT 1.22 | Anatomy relevant to drainage of the pleural space | `anzca::primary::anatomy::airway` |

#### 1b. Vascular Access
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_RT 1.20 | Anatomy (including USS) for vascular access in resuscitation — antecubital, saphenous, jugular, subclavian veins; intraosseous devices | `anzca::primary::anatomy::vascular_access` |
| BT_GS 1.70 | Anatomy (including USS) of peripheral venous system for IV cannulation and PICC insertion | `anzca::primary::anatomy::vascular_access` |
| BT_GS 1.72 | Anatomy of great veins for central venous cannulation, including USS anatomy | `anzca::primary::anatomy::vascular_access` |
| BT_GS 1.74 | Anatomy of radial, brachial, femoral and dorsalis pedis arteries for arterial cannulation, including USS anatomy | `anzca::primary::anatomy::vascular_access` |

#### 1c. Neuraxial
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_RA 1.4 | Anatomy of vertebral column, spinal cord and meninges for central neuraxial block — surface markings | `anzca::primary::anatomy::neuraxial` |
| BT_RA 1.17 | Midline and paramedian approaches to sub-arachnoid and epidural space | `anzca::primary::anatomy::neuraxial` |

---

### 2. Fundamental Pharmacology

#### 2a. Pharmacodynamics
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.1 | Drug action: receptor theory, enzyme interactions, physico-chemical interactions | `anzca::primary::pharmacology::pharmacodynamics` |
| BT_GS 1.2 | Receptor activity: ionic fluxes, second messengers and G proteins, nucleic acid synthesis, evidence for receptors, regulation of receptor number and activity | `anzca::primary::pharmacology::pharmacodynamics` |
| BT_GS 1.3 | Dose-effect relationships: graded/quantal response, therapeutic index, potency/efficacy, competitive/non-competitive antagonists, partial agonists/inverse agonists, additive/synergistic effects | `anzca::primary::pharmacology::pharmacodynamics` |
| BT_GS 1.4 | Efficacy and potency with reference to dose-response curves | `anzca::primary::pharmacology::pharmacodynamics` |
| BT_GS 1.5 | Law of mass action and dynamic equilibrium; receptor affinity and dissociation constants | `anzca::primary::pharmacology::pharmacodynamics` |
| BT_GS 1.6 | Mechanisms of adverse drug effects | `anzca::primary::pharmacology::pharmacodynamics` |

#### 2b. Pharmacokinetics
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.7 | Pharmacokinetic modelling (single/multiple compartment): half-life, clearance, zero/first-order kinetics, Vd, bioavailability, AUC, extraction ratio | `anzca::primary::pharmacology::pharmacokinetics` |
| BT_GS 1.8 | Drug absorption — clinically utilised routes of administration | `anzca::primary::pharmacology::pharmacokinetics` |
| BT_GS 1.9 | Drug distribution: protein binding, lipid solubility, pH, pKa — altered in physiological and pathological disturbance | `anzca::primary::pharmacology::pharmacokinetics` |
| BT_GS 1.10 | Mechanisms of drug clearance — effect of physiological and pathological disturbance | `anzca::primary::pharmacology::pharmacokinetics` |
| BT_GS 1.11 | Hepatic and non-hepatic metabolism: phase 1/2 reactions, hepatic extraction ratio, first-pass effect, enzyme induction/inhibition | `anzca::primary::pharmacology::pharmacokinetics` |
| BT_GS 1.12 | IV and infusion kinetics: effect-site and effect-site equilibration time, context-sensitive half-time, loading/maintenance dose calculation | `anzca::primary::pharmacology::pharmacokinetics` |
| BT_GS 1.13 | Clinical drug monitoring: peak/trough concentrations, minimum therapeutic concentration, toxicity | `anzca::primary::pharmacology::pharmacokinetics` |

#### 2c. Variability in Drug Response
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.14 | Variations in individual drug responses — applied to clinical situations | `anzca::primary::pharmacology::variability` |
| BT_GS 1.15 | Tachyphylaxis, tolerance, addiction, dependence, idiosyncrasy — mechanisms of tolerance | `anzca::primary::pharmacology::variability` |
| BT_GS 1.16 | Altered pharmacokinetics/pharmacodynamics due to physiological changes — elderly and obesity | `anzca::primary::pharmacology::variability` |
| BT_GS 1.17 | Altered pharmacokinetics/pharmacodynamics due to pathological disturbance — cardiac, respiratory, renal, hepatic disease | `anzca::primary::pharmacology::variability` |
| BT_GS 1.19 | Mechanisms of drug interactions | `anzca::primary::pharmacology::variability` |
| BT_GS 1.20 | Pharmacogenetic variation — atypical plasma cholinesterase, CYP450 variations | `anzca::primary::pharmacology::variability` |
| BT_GS 1.21 | Clinical importance of isomerism | `anzca::primary::pharmacology::variability` |

#### 2d. Pharmaceutics
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.22 | Mechanisms and adverse effects of buffers, anti-oxidants, antimicrobial and solubilising agents added to drugs | `anzca::primary::pharmacology::pharmaceutics` |

---

### 3. Cellular Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.82a | Basic cellular physiology: cell membrane structure and trans-membrane transport, intracellular fluid composition/regulation, trans-membrane potential generation, protein synthesis | `anzca::primary::physiology::cellular` |

---

### 4. General Anaesthetic Agents and Sedatives

#### 4a. Inhalational
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.23 | Physical properties of inhalational agents: vaporisation principles, ideal agent properties, structure-activity relationships | `anzca::primary::anaesthetic_agents::inhalational` |
| BT_GS 1.24 | Uptake, distribution and elimination of inhalational agents: partition coefficients, concentration effect, second gas effect, inhaled/alveolar concentration relationship, cardiac output and tissue partition effects | `anzca::primary::anaesthetic_agents::inhalational` |
| BT_GS 1.25 | Effects of inhalational agents on cardiovascular, respiratory and CNS | `anzca::primary::anaesthetic_agents::inhalational` |
| BT_GS 1.26 | Toxicity of inhalational agents | `anzca::primary::anaesthetic_agents::inhalational` |
| BT_GS 1.27 | Pharmacology of nitrous oxide | `anzca::primary::anaesthetic_agents::inhalational` |
| BT_GS 1.28 | Comparative pharmacology of nitrous oxide, sevoflurane, desflurane (describe); isoflurane, methoxyflurane, ether, halothane, xenon (outline) | `anzca::primary::anaesthetic_agents::inhalational` |
| BT_GS 1.50 | MAC — concept and clinical application | `anzca::primary::anaesthetic_agents::inhalational` |

#### 4b. Intravenous
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.29 | Physical properties of sedative/hypnotic agents: formulation, ideal agent properties, structure-activity relationships | `anzca::primary::anaesthetic_agents::intravenous` |
| BT_GS 1.30 | Pharmacokinetics of IV anaesthetic and sedative agents: onset/offset, clinical implications of differences | `anzca::primary::anaesthetic_agents::intravenous` |
| BT_GS 1.31 | Comparative pharmacology of IV anaesthetic and sedative agents — effects on CNS, respiratory and cardiovascular systems | `anzca::primary::anaesthetic_agents::intravenous` |
| BT_GS 1.32 | Adverse effects of individual induction, sedative and premedicant agents | `anzca::primary::anaesthetic_agents::intravenous` |
| BT_GS 1.34 | Pharmacology and clinical use of flumazenil | `anzca::primary::anaesthetic_agents::intravenous` |
| BT_GS 1.59 | TCI pharmacokinetics/pharmacodynamics: multi-compartment model and rate constants, effect site (biophase) and ke0, plasma-effect site relationship, altered response (age, obesity, cardiac output), sources of error | `anzca::primary::anaesthetic_agents::intravenous` |
| BT_GS 1.59a | Similarities and differences between commonly used TCI models | `anzca::primary::anaesthetic_agents::intravenous` |

#### 4c. Integrated
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.49 | Proposed mechanisms of anaesthesia and sites of action of anaesthetic agents | `anzca::primary::anaesthetic_agents::integrated` |
| BT_GS 1.51 | Depth of anaesthesia — concept and assessment | `anzca::primary::anaesthetic_agents::integrated` |
| BT_GS 1.51a | Aetiology of and measures to prevent intra-operative awareness | `anzca::primary::anaesthetic_agents::integrated` |
| BT_GS 1.53 | Synergism between anaesthetic agents, opioids and regional blockade — clinical use | `anzca::primary::anaesthetic_agents::integrated` |
| BT_GS 1.48 | Effects of anaesthetic agents on regional circulations | `anzca::primary::anaesthetic_agents::integrated` |
| BT_GS 1.60 | Physiological effects of anaesthesia on the respiratory system and its clinical management | `anzca::primary::anaesthetic_agents::integrated` |
| BT_GS 1.61 | Effects of anaesthesia on the immune, haematological and endocrine systems | `anzca::primary::anaesthetic_agents::integrated` |
| BT_GS 1.33 | Altered pharmacokinetics/pharmacodynamics of inhalational and IV anaesthetic agents in: elderly, obesity, cardiac/respiratory/renal/hepatic disease | `anzca::primary::anaesthetic_agents::integrated` |

---

### 5. Respiratory System

#### 5a. Anatomy
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.7 | Anatomy of lungs, tracheobronchial tree and alveoli | `anzca::primary::respiratory::anatomy` |

#### 5b-i. Control of Breathing
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.9 | Neural and chemical control of ventilation via central and peripheral chemoreceptors — altered by anaesthesia and abnormal clinical states | `anzca::primary::respiratory::physiology::control_of_breathing` |

#### 5b-ii. Mechanics of Breathing
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.6 | Structure of chest wall and diaphragm — implications for respiratory mechanics | `anzca::primary::respiratory::physiology::mechanics` |
| BT_PO 1.10 | Properties of surfactant and its role in respiratory mechanics | `anzca::primary::respiratory::physiology::mechanics` |
| BT_PO 1.11 | Compliance (static, dynamic, specific) — elastic properties of the lung | `anzca::primary::respiratory::physiology::mechanics` |
| BT_PO 1.12 | Fast and slow alveoli — concept of time constants | `anzca::primary::respiratory::physiology::mechanics` |
| BT_PO 1.13 | Elastic properties of chest wall; pressure-volume relationships of lung, chest wall and total respiratory system | `anzca::primary::respiratory::physiology::mechanics` |
| BT_PO 1.14 | Vertical gradient of pleural pressure and its significance | `anzca::primary::respiratory::physiology::mechanics` |
| BT_PO 1.15 | Physics of gas flow; relationship between resistance and flow in the respiratory tract | `anzca::primary::respiratory::physiology::mechanics` |
| BT_PO 1.16 | Factors affecting airway resistance and its measurement | `anzca::primary::respiratory::physiology::mechanics` |
| BT_PO 1.17 | Closing capacity — relationship to airway closure, clinical significance and measurement | `anzca::primary::respiratory::physiology::mechanics` |
| BT_PO 1.18 | Work of breathing | `anzca::primary::respiratory::physiology::mechanics` |
| BT_PO 1.19 | Altered lung mechanics in common disease states | `anzca::primary::respiratory::physiology::mechanics` |

#### 5b-iii. Pulmonary Gas Volumes
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.20 | Lung volumes and capacities — measurement and normal values | `anzca::primary::respiratory::physiology::gas_volumes` |
| BT_PO 1.21 | Dead space — measurement; Bohr equation and alveolar gas equation | `anzca::primary::respiratory::physiology::gas_volumes` |
| BT_PO 1.22 | Composition of ideal alveolar and mixed expired gases | `anzca::primary::respiratory::physiology::gas_volumes` |

#### 5b-iv. Pulmonary Circulation
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.8 | Anatomy of pulmonary and bronchial circulations | `anzca::primary::respiratory::physiology::pulmonary_circulation` |
| BT_PO 1.33 | Differences between pulmonary and systemic circulations | `anzca::primary::respiratory::physiology::pulmonary_circulation` |
| BT_PO 1.34 | Pulmonary vascular resistance and control of pulmonary vascular tone | `anzca::primary::respiratory::physiology::pulmonary_circulation` |

#### 5b-v. V/Q Relationships
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.26 | Normal ventilation-perfusion matching | `anzca::primary::respiratory::physiology::vq_relationships` |
| BT_PO 1.27 | West's zones of the lung | `anzca::primary::respiratory::physiology::vq_relationships` |
| BT_PO 1.28 | Shunt equation | `anzca::primary::respiratory::physiology::vq_relationships` |
| BT_PO 1.29 | Regional V/Q inequalities and abnormalities, venous admixture — effect on oxygenation and CO2 elimination | `anzca::primary::respiratory::physiology::vq_relationships` |

#### 5b-vi. Diffusive Transfer of Gases
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.23 | Oxygen cascade | `anzca::primary::respiratory::physiology::diffusion` |
| BT_PO 1.24 | Alveolar exchange of oxygen and carbon dioxide | `anzca::primary::respiratory::physiology::diffusion` |
| BT_PO 1.25 | Diffusion capacity and its measurement | `anzca::primary::respiratory::physiology::diffusion` |

#### 5b-vii. Gas Transport in Blood
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.31 | Carriage of oxygen in blood — oxyhaemoglobin dissociation curve, oxygen stores, clinical significance | `anzca::primary::respiratory::physiology::gas_transport` |
| BT_PO 1.32 | Carriage of carbon dioxide in blood — CO2 dissociation curve, clinical significance | `anzca::primary::respiratory::physiology::gas_transport` |

#### 5b-viii. Applied Respiratory Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_AM 1.2 | Physiology of the airway including airway reflexes | `anzca::primary::respiratory::physiology::applied` |
| BT_AM 1.4 | Physiological consequences of anaesthesia and patient positioning on the respiratory system | `anzca::primary::respiratory::physiology::applied` |
| BT_AM 1.19 | Different modes of mechanical ventilation and their physiological consequences | `anzca::primary::respiratory::physiology::applied` |
| BT_PO 1.35 | Physiological consequences of IPPV and PEEP | `anzca::primary::respiratory::physiology::applied` |
| BT_PO 1.35a | Preoxygenation — physiological basis | `anzca::primary::respiratory::physiology::applied` |
| BT_PO 1.36 | Physiological effects of hypoxaemia, hyper/hypocapnia and carbon monoxide poisoning | `anzca::primary::respiratory::physiology::applied` |
| BT_PO 1.37 | Effect of posture, exercise, altitude, anaesthesia, ageing and morbid obesity on ventilation | `anzca::primary::respiratory::physiology::applied` |
| BT_PO 1.38 | Humidity and the importance of humidification | `anzca::primary::respiratory::physiology::applied` |
| BT_PO 1.39 | Non-ventilatory functions of the lungs | `anzca::primary::respiratory::physiology::applied` |
| BT_RT 1.10 | Classification and causes of hypoxia and hypoxaemia | `anzca::primary::respiratory::physiology::applied` |
| BT_RT 1.11 | Physiological consequences of hypoxia and hypoxaemia | `anzca::primary::respiratory::physiology::applied` |
| BT_RT 1.38 | Respiratory failure — definition; type 1 vs type 2 | `anzca::primary::respiratory::physiology::applied` |
| BT_RT 1.39 | Interpretation of blood gas analysis in respiratory failure | `anzca::primary::respiratory::physiology::applied` |

#### 5c. Respiratory Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_AM 1.3 | Effect of anaesthetic agents and other drugs on airway reflexes | `anzca::primary::respiratory::pharmacology` |
| BT_PO 1.40 | Pharmacology of anti-asthma drugs | `anzca::primary::respiratory::pharmacology` |
| BT_PO 1.41 | Pharmacology of drugs used to treat pulmonary hypertension including nitric oxide | `anzca::primary::respiratory::pharmacology` |
| BT_PO 1.41a | Oxygen therapy — methods of delivery, indications/contraindications, physiological and pathophysiological effects | `anzca::primary::respiratory::pharmacology` |

---

### 6. Autonomic Nervous System

#### 6a. Anatomy and Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PM 1.2 | Anatomy of the autonomic nervous system | `anzca::primary::autonomic::anatomy_physiology` |
| BT_PO 1.51 | ANS physiological roles: autonomic receptors and cellular effects, autonomic transmitters — synthesis, release and fate | `anzca::primary::autonomic::anatomy_physiology` |

#### 6b. Pharmacology
*(See Cardiovascular Pharmacology — BT_PO 1.52, 1.53, 1.54, BT_RT 1.17, 1.18)*

---

### 7. Cardiovascular System

#### 7a. Anatomy
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.42 | Anatomy of the heart including coronary circulation and territories supplied | `anzca::primary::cardiovascular::anatomy` |

#### 7b-i. Electrical Properties of the Heart
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.43 | Electrical activity and mechanical events: ionic basis of automaticity, normal/abnormal cardiac excitation, physiological basis of ECG, factors influencing cardiac electrical activity, mechanical-electrical-ionic event correlation | `anzca::primary::cardiovascular::physiology::electrical` |

#### 7b-ii. Cardiac Output, Blood Pressure, and Regional Circulations
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.44 | Physiology of cardiac muscle and excitation-contraction coupling | `anzca::primary::cardiovascular::physiology::cardiac_output` |
| BT_PO 1.44a | Events of the cardiac cycle — Wiggers diagram and pressure-volume loop | `anzca::primary::cardiovascular::physiology::cardiac_output` |
| BT_PO 1.45 | Determinants and control of cardiac output: preload, afterload, contractility, Frank-Starling mechanism, cardiac output and vascular function curves, pressure-volume relationships | `anzca::primary::cardiovascular::physiology::cardiac_output` |
| BT_PO 1.46 | Myocardial oxygen supply and demand — determinants and clinical implications | `anzca::primary::cardiovascular::physiology::cardiac_output` |
| BT_PO 1.47 | Control of blood pressure and distribution of blood volume/flow: systemic BP regulation, total peripheral resistance, organ blood flow and autoregulation, coronary/cerebral/skin/muscle/renal/hepatic/splanchnic circulations, microcirculation and fluid exchange | `anzca::primary::cardiovascular::physiology::cardiac_output` |

#### 7b-iii. Applied Cardiovascular Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.48 | Cardiovascular responses to: posture, exercise, Valsalva, PPV/PEEP, pneumoperitoneum, haemorrhage/hypovolaemia, surgery/trauma | `anzca::primary::cardiovascular::physiology::applied` |
| BT_PO 1.49 | Cardiovascular changes with ageing | `anzca::primary::cardiovascular::physiology::applied` |
| BT_PO 1.50 | Cardiovascular changes with morbid obesity | `anzca::primary::cardiovascular::physiology::applied` |

#### 7b-iv. Shock
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_RT 1.1 | Definition, classification and causes of shock — pathophysiological mechanisms | `anzca::primary::cardiovascular::physiology::shock` |
| BT_RT 1.2 | Types of shock with reference to determinants of cardiac output | `anzca::primary::cardiovascular::physiology::shock` |
| BT_RT 1.3 | Physiological consequences of shock | `anzca::primary::cardiovascular::physiology::shock` |
| BT_RT 1.4 | Oxygen delivery; indicators of tissue oxygenation (base deficit, lactate, mixed venous O2 saturation) in resuscitation | `anzca::primary::cardiovascular::physiology::shock` |
| BT_RT 1.30 | Clinical signs of shock altered by age | `anzca::primary::cardiovascular::physiology::shock` |

#### 7c. Cardiovascular Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.52 | Mechanism of action and effects of sympathomimetic and anticholinergic drugs | `anzca::primary::cardiovascular::pharmacology` |
| BT_PO 1.53 | Pharmacology and clinical application of adrenergic agonists | `anzca::primary::cardiovascular::pharmacology` |
| BT_PO 1.54 | Pharmacology of alpha and beta receptor blocking agents | `anzca::primary::cardiovascular::pharmacology` |
| BT_PO 1.55 | Clinically important drug interactions with the ANS — TCAs, MAOIs | `anzca::primary::cardiovascular::pharmacology` |
| BT_PO 1.56 | Physiological and pharmacological basis of classifying antiarrhythmic agents | `anzca::primary::cardiovascular::pharmacology` |
| BT_PO 1.57 | Pharmacology of amiodarone (describe); other antiarrhythmic agents (outline) | `anzca::primary::cardiovascular::pharmacology` |
| BT_PO 1.58 | Pharmacology of GTN and sodium nitroprusside (describe); other antihypertensives (outline) | `anzca::primary::cardiovascular::pharmacology` |
| BT_PO 1.59 | Pharmacology of drugs for myocardial ischaemia/infarction | `anzca::primary::cardiovascular::pharmacology` |
| BT_PO 1.60 | Pharmacology of drugs for acute or chronic cardiac failure | `anzca::primary::cardiovascular::pharmacology` |
| BT_RT 1.17 | Pharmacology of vasopressors and inotropes — in management of shock | `anzca::primary::cardiovascular::pharmacology` |
| BT_RT 1.18 | Pharmacology of drugs in current ACLS guidelines — in context of CPR | `anzca::primary::cardiovascular::pharmacology` |

---

### 8. Renal System

#### 8a. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.61 | Functional anatomy of the nephron | `anzca::primary::renal::physiology` |
| BT_PO 1.62 | Physiology of renal blood flow | `anzca::primary::renal::physiology` |
| BT_PO 1.63 | Glomerular filtration and tubular function | `anzca::primary::renal::physiology` |
| BT_PO 1.64 | Counter-current mechanisms in the kidney | `anzca::primary::renal::physiology` |
| BT_PO 1.65 | Mechanisms involved in the regulation of renal function | `anzca::primary::renal::physiology` |
| BT_PO 1.66 | Endocrine functions of the kidney | `anzca::primary::renal::physiology` |
| BT_PO 1.67 | Role of the kidney in handling glucose, nitrogenous products and drugs | `anzca::primary::renal::physiology` |
| BT_PO 1.68 | Principles of measurement of GFR and renal blood flow | `anzca::primary::renal::physiology` |
| BT_PO 1.69 | Physiological effects and clinical assessment of renal dysfunction | `anzca::primary::renal::physiology` |
| BT_PO 1.70 | Renal responses to hypovolaemia | `anzca::primary::renal::physiology` |
| BT_PO 1.71 | Effects of anaesthesia on renal function | `anzca::primary::renal::physiology` |

#### 8b. Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.80 | Alterations to drug response due to renal disease | `anzca::primary::renal::pharmacology` |
| BT_PO 1.81 | Classification of diuretics by site of action | `anzca::primary::renal::pharmacology` |
| BT_PO 1.82 | Pharmacology of diuretics | `anzca::primary::renal::pharmacology` |

---

### 9. Fluids and Electrolytes
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.72 | Function, distribution and physiological importance of Na, Cl, K, Mg, Ca and phosphate ions | `anzca::primary::fluids_electrolytes` |
| BT_PO 1.73 | Mechanisms involved in maintenance of fluid and electrolyte balance | `anzca::primary::fluids_electrolytes` |
| BT_PO 1.74 | Constituents and functions of plasma | `anzca::primary::fluids_electrolytes` |
| BT_PO 1.75 | Osmotic pressure — definition and determining factors | `anzca::primary::fluids_electrolytes` |
| BT_PO 1.76 | Regulation of osmolality | `anzca::primary::fluids_electrolytes` |
| BT_PO 1.77 | Oncotic pressure, colloid osmotic pressure and reflection coefficients | `anzca::primary::fluids_electrolytes` |
| BT_PO 1.77a | Body fluid compartments and fluid movement between compartments | `anzca::primary::fluids_electrolytes` |
| BT_PO 1.77b | Chemical composition of crystalloids and colloids; use as volume replacement/maintenance fluid including adverse effects | `anzca::primary::fluids_electrolytes` |

---

### 10. Acid-Base
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.78 | Regulation of acid/base balance | `anzca::primary::acid_base` |
| BT_PO 1.79 | Acid-base chemistry — Henderson-Hasselbach equation and strong ion difference | `anzca::primary::acid_base` |
| BT_PO 1.79a | Interpretation of blood gases in clinical situations | `anzca::primary::acid_base` |

---

### 11. Nervous System

#### 11a. Anatomy
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_RT 1.23 | Anatomy of the cerebral and spinal cord circulation | `anzca::primary::nervous_system::anatomy` |

#### 11b. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_RA 1.1 / BT_PO 1.92 | Physiology of nerve conduction | `anzca::primary::nervous_system::physiology` |
| BT_PO 1.93 | Differences between normal sleep and anaesthesia, including the EEG | `anzca::primary::nervous_system::physiology` |
| BT_PO 1.94 | Basis of the electroencephalogram | `anzca::primary::nervous_system::physiology` |
| BT_PO 1.95 | Determinants and control of: ICP, intraspinal pressure, cerebral blood flow and autoregulation, cerebral perfusion pressure, spinal cord perfusion | `anzca::primary::nervous_system::physiology` |
| BT_PO 1.96 | Structure and function of the blood-brain barrier | `anzca::primary::nervous_system::physiology` |
| BT_PO 1.97 | Production, reabsorption and role of CSF | `anzca::primary::nervous_system::physiology` |
| BT_PO 1.98 | Cerebral and spinal cord metabolism: energy production, effects of temperature, factors leading to cell damage/death | `anzca::primary::nervous_system::physiology` |
| BT_RT 1.12 | Factors determining ICP and its regulation | `anzca::primary::nervous_system::physiology` |
| BT_RT 1.13 | Regulation of cerebral blood flow and factors leading to loss of autoregulation | `anzca::primary::nervous_system::physiology` |
| BT_RT 1.14 | Cerebral perfusion pressure | `anzca::primary::nervous_system::physiology` |
| BT_RT 1.15 | Blood supply to the spinal cord and regulation of spinal cord blood flow | `anzca::primary::nervous_system::physiology` |
| BT_RT 1.16 | Spinal cord perfusion pressure | `anzca::primary::nervous_system::physiology` |
| BT_RA 1.2 | Physiological consequences of a central neuraxial block | `anzca::primary::nervous_system::physiology` |

#### 11c. Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.98d | Pharmacology of hyperosmolar solutions used to decrease brain volume | `anzca::primary::nervous_system::pharmacology` |
| BT_PO 1.99 | Pharmacology of anti-depressant, anti-psychotic, anti-convulsant, anti-parkinsonian and anti-migraine medication | `anzca::primary::nervous_system::pharmacology` |
| BT_PO 1.101 | Pharmacology of drugs acting via serotonin or serotonin receptors | `anzca::primary::nervous_system::pharmacology` |
| BT_PO 1.102 | Clinical features and management of serotonin syndrome | `anzca::primary::nervous_system::pharmacology` |

---

### 12. Pain

#### 12a. Anatomy
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_RA 1.7 / BT_PM 1.1 | Anatomy of sensory pathways with particular reference to pain sensation | `anzca::primary::pain::anatomy` |
| BT_RA 1.5 | Dermatomal innervations | `anzca::primary::pain::anatomy` |
| BT_RA 1.6 | Myotomal innervations | `anzca::primary::pain::anatomy` |

#### 12b. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PM 1.3 | Physiological mechanisms of pain: peripheral nociception, conduction, spinal cord modulation, central processing, mediators/pathways/reflexes, peripheral and central sensitisation, pre-emptive and preventive analgesia | `anzca::primary::pain::physiology` |
| BT_PM 1.4 | Mechanisms of progression from acute to chronic pain | `anzca::primary::pain::physiology` |
| BT_PM 1.6 | Pathophysiology of neuropathic pain | `anzca::primary::pain::physiology` |
| BT_PM 1.8 | Altered physiology and perception of pain in the older patient | `anzca::primary::pain::physiology` |

#### 12c-i. Pharmacology — General
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PM 1.9 | Pharmacology of pain agents — opioids, tramadol, tapentadol, local anaesthetics, NSAIDs, paracetamol, NMDA antagonists, nitrous oxide, methoxyflurane (describe); anticonvulsants, antidepressants, corticosteroids (outline) | `anzca::primary::pain::pharmacology::general` |
| BT_PM 1.10 | Effect of physiological change and pathological disturbance on pharmacology of BT_PM 1.9 agents — special reference to elderly | `anzca::primary::pain::pharmacology::general` |

#### 12c-ii. Pharmacology — Opioids
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PM 1.12 | Opioid receptors | `anzca::primary::pain::pharmacology::opioids` |
| BT_PM 1.13 | Mechanisms of action of opioids including tramadol and tapentadol | `anzca::primary::pain::pharmacology::opioids` |
| BT_PM 1.14 | Actions of agonists, partial agonists, mixed agonist-antagonists and antagonists | `anzca::primary::pain::pharmacology::opioids` |
| BT_PM 1.15 | Pharmacokinetics and clinical implications of different routes of administration for commonly used opioids (oral, transdermal, SC, IM, IV, PCA) | `anzca::primary::pain::pharmacology::opioids` |
| BT_PM 1.16 | Dose conversions between commonly used opioids | `anzca::primary::pain::pharmacology::opioids` |
| BT_PM 1.17 | Pharmacokinetics and pharmacodynamics of IV opioids — clinical applications | `anzca::primary::pain::pharmacology::opioids` |
| BT_GS 1.41 | Clinical application of opioids to anaesthesia and sedation | `anzca::primary::pain::pharmacology::opioids` |
| BT_GS 1.42 | Pharmacokinetics of IV opioids | `anzca::primary::pain::pharmacology::opioids` |
| BT_PM 1.18 | Pharmacology of epidural and intrathecal opioids | `anzca::primary::pain::pharmacology::opioids` |
| BT_PM 1.19 | Adverse effects of opioids by systemic and neuraxial routes — prevention and management | `anzca::primary::pain::pharmacology::opioids` |
| BT_PM 1.20 | Adverse drug interactions between opioids and other agents | `anzca::primary::pain::pharmacology::opioids` |
| BT_PM 1.21 | Pharmacology of opioid antagonists | `anzca::primary::pain::pharmacology::opioids` |

#### 12c-iii. Pharmacology — Local Anaesthetics
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_RA 1.3 | Pharmacology of local anaesthetic agents: mechanism of action, comparative pharmacology, speed of onset, duration of action, toxicity and management, pharmacokinetics in epidural and subarachnoid space | `anzca::primary::pain::pharmacology::local_anaesthetics` |
| BT_RA 1.14 | Factors influencing dose and choice of agent for spinal and epidural anaesthesia/analgesia | `anzca::primary::pain::pharmacology::local_anaesthetics` |
| BT_RA 1.15 | Baricity of agents and patient positioning — effect on extent of block in spinal anaesthesia | `anzca::primary::pain::pharmacology::local_anaesthetics` |
| BT_RA 1.16 | Adjuvant agents with neuraxial and peripheral nerve blocks — risks and benefits | `anzca::primary::pain::pharmacology::local_anaesthetics` |

#### 12c-iv. Pharmacology — NSAIDs and Paracetamol
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PM 1.23 | Prostaglandin pathways and their physiological role in pain production | `anzca::primary::pain::pharmacology::nsaids_paracetamol` |
| BT_PM 1.24 | Classification and pharmacology of NSAIDs | `anzca::primary::pain::pharmacology::nsaids_paracetamol` |
| BT_PM 1.25 | Pharmacology of paracetamol including toxicity | `anzca::primary::pain::pharmacology::nsaids_paracetamol` |

#### 12c-v. Pharmacology — Other
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PM 1.26 | Location, structure and function of NMDA receptors | `anzca::primary::pain::pharmacology::other` |
| BT_PM 1.27 | Pharmacology of ketamine | `anzca::primary::pain::pharmacology::other` |
| BT_PM 1.28 | Pharmacology of gabapentinoids and other anticonvulsants relevant to pain medicine | `anzca::primary::pain::pharmacology::other` |

---

### 13. Muscular System

#### 13a. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.35 | Physiology of the neuromuscular junction | `anzca::primary::muscular::physiology` |
| BT_PO 1.98a | Physiology of skeletal muscle including excitation-contraction coupling | `anzca::primary::muscular::physiology` |
| BT_PO 1.98b | Physiology of smooth muscle | `anzca::primary::muscular::physiology` |
| BT_PO 1.98c | Similarities and differences between skeletal, cardiac and smooth muscle | `anzca::primary::muscular::physiology` |

#### 13b. Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.36 | Mechanism of action and pharmacokinetics of neuromuscular blocking agents | `anzca::primary::muscular::pharmacology` |
| BT_GS 1.37 | Pharmacological differences between NMBs and clinical importance of these differences | `anzca::primary::muscular::pharmacology` |
| BT_GS 1.37a | Onset and offset of neuromuscular blockade at different muscle groups | `anzca::primary::muscular::pharmacology` |
| BT_GS 1.38 | Adverse effects of NMBs and factors that modify responses to muscle relaxants | `anzca::primary::muscular::pharmacology` |
| BT_GS 1.39 | Pharmacology of drugs used to reverse neuromuscular blockade | `anzca::primary::muscular::pharmacology` |
| BT_GS 1.40 | Adverse effects of anticholinesterase agents | `anzca::primary::muscular::pharmacology` |
| BT_GS 1.47 | Indications for muscle relaxation in anaesthesia | `anzca::primary::muscular::pharmacology` |
| BT_GS 1.55 | Depth of neuromuscular blockade — concept and use of neuromuscular monitoring | `anzca::primary::muscular::pharmacology` |
| BT_GS 1.56 | Clinical features and management of inadequate reversal of neuromuscular blockade | `anzca::primary::muscular::pharmacology` |
| BT_RT 1.19 | Pharmacology of dantrolene in treatment of malignant hyperthermia | `anzca::primary::muscular::pharmacology` |

---

### 14. Liver

#### 14a. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.103 | Functions of the liver | `anzca::primary::liver::physiology` |
| BT_PO 1.104 | Determinants of liver blood flow | `anzca::primary::liver::physiology` |
| BT_PO 1.105 | Portal circulation and its significance | `anzca::primary::liver::physiology` |
| BT_PO 1.106 | Laboratory assessment of liver function and hepatic failure | `anzca::primary::liver::physiology` |

#### 14b. Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.108 | Alterations to drug response due to hepatic disease | `anzca::primary::liver::pharmacology` |

---

### 15. Gastrointestinal

#### 15a. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.43 | Physiological basis of vomiting | `anzca::primary::gastrointestinal::physiology` |
| BT_PO 1.107 | Physiology of nausea and vomiting (describe); physiology of swallowing, anti-reflux mechanisms, gastric motility/emptying, composition of gastric fluid (outline) | `anzca::primary::gastrointestinal::physiology` |

#### 15b. Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.44 | Pharmacology of anti-emetic and pro-kinetic agents | `anzca::primary::gastrointestinal::pharmacology` |
| BT_GS 1.62 | Prevention and management of PONV | `anzca::primary::gastrointestinal::pharmacology` |
| BT_PO 1.109 | Pharmacological treatment of peptic ulcer disease and reflux | `anzca::primary::gastrointestinal::pharmacology` |

---

### 16. Endocrine, Metabolism and Nutrition

#### 16a. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.82b | Energy production by metabolic processes in cells | `anzca::primary::endocrine::physiology` |
| BT_PO 1.83 | Physiological consequences of fasting and starvation | `anzca::primary::endocrine::physiology` |
| BT_PO 1.84 | Factors that influence metabolic rate | `anzca::primary::endocrine::physiology` |
| BT_PO 1.85 | Control of blood glucose | `anzca::primary::endocrine::physiology` |
| BT_PO 1.86 | Role of hypothalamus in integration of neuro-humoral responses | `anzca::primary::endocrine::physiology` |
| BT_PO 1.87 | Control of secretion and functions of: pituitary hormones, thyroid hormones, adrenocortical hormones, adrenomedullary hormones, renin and angiotensin, atrial natriuretic peptide | `anzca::primary::endocrine::physiology` |
| BT_PO 1.88 | Regulation of plasma calcium — vitamin D, PTH and calcitonin | `anzca::primary::endocrine::physiology` |
| BT_PO 1.89 | Role of prostaglandins and other autocoids | `anzca::primary::endocrine::physiology` |

#### 16b. Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.90 | Pharmacology of insulin preparations and oral hypoglycaemics | `anzca::primary::endocrine::pharmacology` |
| BT_PO 1.91 | Pharmacology of thyroid hormone replacement and anti-thyroid drugs, corticosteroids, glucagon, vasopressin and analogues | `anzca::primary::endocrine::pharmacology` |

---

### 17. Haematology and Transfusion

#### 17a. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.110 | Physiological consequences of acute and chronic anaemia including iron deficiency | `anzca::primary::haematology::physiology` |
| BT_PO 1.112 | Physiology of haemostasis: coagulation, role of platelets, fibrinolysis | `anzca::primary::haematology::physiology` |
| BT_PO 1.113 | Physiological mechanisms of limiting and preventing thrombosis | `anzca::primary::haematology::physiology` |
| BT_PO 1.114 | Methods for assessing coagulation, platelet function and fibrinolysis | `anzca::primary::haematology::physiology` |
| BT_PO 1.115 | Blood groups and methods of cross matching | `anzca::primary::haematology::physiology` |
| BT_RT 1.7 | Blood groups and physiological basis of transfusion reactions | `anzca::primary::haematology::physiology` |
| BT_PO 1.116 | Composition, indications and risks of blood components: packed red cells, FFP, cryoprecipitate, platelets, factor VIIa | `anzca::primary::haematology::physiology` |
| BT_PO 1.117 | Changes during blood storage and their clinical implications | `anzca::primary::haematology::physiology` |
| BT_RT 1.8 | Changes in stored blood | `anzca::primary::haematology::physiology` |
| BT_RT 1.9 | Physiological consequences of massive transfusion | `anzca::primary::haematology::physiology` |

#### 17b. Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.118 | Pharmacology of heparin and LMWH including side-effects | `anzca::primary::haematology::pharmacology` |
| BT_PO 1.119 | Pharmacology of protamine | `anzca::primary::haematology::pharmacology` |
| BT_PO 1.120 | Pharmacology of warfarin and other anticoagulant drugs | `anzca::primary::haematology::pharmacology` |
| BT_PO 1.121 | Methods to reverse warfarin and other anticoagulant drugs | `anzca::primary::haematology::pharmacology` |
| BT_PO 1.122 | Classification and pharmacology of anti-platelet drugs | `anzca::primary::haematology::pharmacology` |
| BT_PO 1.123 | Pharmacology of thrombolytic agents | `anzca::primary::haematology::pharmacology` |
| BT_PO 1.124 | Pharmacology of tranexamic acid | `anzca::primary::haematology::pharmacology` |
| BT_PO 1.124a | Pharmacology of iron replacement | `anzca::primary::haematology::pharmacology` |

---

### 18. Immunology and Infection

#### 18a. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.126 | How the body defends against infection | `anzca::primary::immunology::physiology` |
| BT_PO 1.127 | Effects of anaesthesia and surgery on immune function | `anzca::primary::immunology::physiology` |
| BT_PO 1.128 | Immunology and pathophysiology of hypersensitivity reactions | `anzca::primary::immunology::physiology` |
| BT_RT 1.5 | Systemic inflammatory response and its physiological effects | `anzca::primary::immunology::physiology` |
| BT_RT 1.6 | Immunology and pathophysiology of anaphylaxis | `anzca::primary::immunology::physiology` |

#### 18b. Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.3 | Adverse effects of antimicrobial agents | `anzca::primary::immunology::pharmacology` |
| BT_PO 1.130 | Pharmacology of antimicrobial drugs used perioperatively — spectrum of activity | `anzca::primary::immunology::pharmacology` |
| BT_PO 1.131 | Principles of antibiotic prophylaxis | `anzca::primary::immunology::pharmacology` |
| BT_PO 1.132 | Pharmacology of antiseptics and disinfectants — clinical use and risks | `anzca::primary::immunology::pharmacology` |

---

### 19. Thermoregulation
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_GS 1.65 | Mechanisms of heat production and transfer between body and environment | `anzca::primary::thermoregulation` |
| BT_GS 1.66 | Physiological effects of hypo- and hyperthermia | `anzca::primary::thermoregulation` |
| BT_GS 1.68 | Physiological responses to lowered and raised environmental temperature — effects of anaesthesia on these responses | `anzca::primary::thermoregulation` |
| BT_GS 1.69 | Methods of maintaining body temperature during anaesthesia and sedation including active warming | `anzca::primary::thermoregulation` |
| BT_SQ 1.17 | Safety of methods for maintaining body temperature during anaesthesia and sedation | `anzca::primary::thermoregulation` |

---

### 20. Obstetrics

#### 20a. Anatomy
| Code | Learning outcome | Section tag |
|---|---|---|
| SS_OB 1.6 | Changes in anatomy of maternal airway and impact on airway management | `anzca::primary::obstetrics::anatomy` |
| SS_OB 1.7 | Changes in anatomy of maternal vertebral column, spinal cord and meninges for central neuraxial block | `anzca::primary::obstetrics::anatomy` |
| SS_OB 1.8 | Anatomy of pain in labour and childbirth | `anzca::primary::obstetrics::anatomy` |

#### 20b. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| SS_OB 1.1 | Physiological changes during pregnancy, labour and delivery — respiratory, cardiovascular, haematological, GI changes and their implications for anaesthesia | `anzca::primary::obstetrics::physiology` |
| SS_OB 1.2 | Reference ranges for physiological and biochemical variables in pregnancy | `anzca::primary::obstetrics::physiology` |
| SS_OB 1.4 | Utero-placental circulation and principles of placental physiology — gas exchange and regulation of placental blood flow | `anzca::primary::obstetrics::physiology` |
| SS_OB 1.5 | Mechanism and consequences of aorto-caval compression in pregnancy | `anzca::primary::obstetrics::physiology` |

#### 20c. Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| SS_OB 1.9 | Influence of pregnancy on pharmacokinetics and pharmacodynamics of drugs used in anaesthesia and analgesia | `anzca::primary::obstetrics::pharmacology` |
| SS_OB 1.10 | Pharmacology of drugs which increase uterine tone | `anzca::primary::obstetrics::pharmacology` |
| SS_OB 1.11 | Pharmacology of tocolytic agents | `anzca::primary::obstetrics::pharmacology` |
| SS_OB 1.12 | Pharmacology of agents used for treatment of pre-eclampsia | `anzca::primary::obstetrics::pharmacology` |

---

### 21. Foetal, Neonatal and Paediatric

#### 21a. Anatomy
| Code | Learning outcome | Section tag |
|---|---|---|
| SS_PA 1.1 | Anatomy of the neonatal airway, changes with growth and development, implications for airway management | `anzca::primary::paediatrics::anatomy` |

#### 21b. Physiology
| Code | Learning outcome | Section tag |
|---|---|---|
| SS_PA 1.21 | Foetal circulation | `anzca::primary::paediatrics::physiology` |
| SS_OB 1.3 | Transition from foetal to neonatal circulation and establishment of ventilation | `anzca::primary::paediatrics::physiology` |
| SS_PA 1.22 | Circulatory and respiratory changes at birth | `anzca::primary::paediatrics::physiology` |
| SS_PA 1.23 | Thermoneutral zone; temperature regulation in neonate — physiological responses to temperature changes, effect of anaesthesia, changes with development | `anzca::primary::paediatrics::physiology` |
| SS_PA 1.24 | Physiology of cardiovascular, respiratory, renal and neurological systems in neonate — changes with development and implications for anaesthetic care | `anzca::primary::paediatrics::physiology` |
| SS_PA 1.25 | Composition of body fluids in neonate — changes with growth and development | `anzca::primary::paediatrics::physiology` |
| SS_PA 1.26 | Glucose homeostasis in neonate — changes with growth and development | `anzca::primary::paediatrics::physiology` |

#### 21c. Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| SS_OB 1.13 | Factors influencing transfer of drugs across the placenta to the foetus | `anzca::primary::paediatrics::pharmacology` |
| SS_OB 1.14 | Potential effects on foetus and neonate of drugs administered during pregnancy | `anzca::primary::paediatrics::pharmacology` |
| SS_OB 1.15 | Potential effects on neonate of drug administration during lactation | `anzca::primary::paediatrics::pharmacology` |
| SS_PA 1.52 | How pharmacokinetics of drugs commonly used in anaesthesia differ in neonates and children vs adults | `anzca::primary::paediatrics::pharmacology` |
| SS_PA 1.53 | How pharmacodynamics of drugs commonly used in anaesthesia differ in neonates and children vs adults | `anzca::primary::paediatrics::pharmacology` |
| SS_PA 1.54 | Pharmacology of agents used for premedication in children | `anzca::primary::paediatrics::pharmacology` |
| SS_PA 1.80 | Maximum safe doses of local anaesthetic agents in different age groups | `anzca::primary::paediatrics::pharmacology` |

---

### 22. Physics and Clinical Measurement
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_SQ 1.5 | Basic physics: fluid behaviour, electrical concepts, humidification principles, USS physics including Doppler | `anzca::primary::physics` |
| BT_SQ 1.6 | Methods of measurement in anaesthesia: SI units, volumes/flows/pressures, BP, cardiac output, temperature, ECG, oximetry, infrared gas analysis/capnography, O2 analysis, pulmonary function tests | `anzca::primary::physics` |
| BT_PO 1.94 | Basis of the EEG | `anzca::primary::physics` |
| BT_GS 1.52 | Electronic monitoring of depth of sedation and anaesthesia — principles including EEG analysis | `anzca::primary::physics` |
| BT_GS 1.55 | Depth of neuromuscular blockade and neuromuscular monitoring | `anzca::primary::physics` |

---

### 23. Equipment and Safety
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_SQ 1.3 | Mandatory safety requirements for anaesthetic machines | `anzca::primary::equipment` |
| BT_SQ 1.7 | Microshock and macroshock — mechanisms for prevention; compatibility of medical procedure, treatment area and equipment | `anzca::primary::equipment` |
| BT_SQ 1.9 | Hazards of anaesthetic gas pollution and methods of scavenging | `anzca::primary::equipment` |
| BT_SQ 1.10 | Supply of medical gases (bulk and cylinder) — safety features including pressure valves, regulators and connection systems | `anzca::primary::equipment` |
| BT_SQ 1.11 | Generation of medical suction; setting up and testing suction systems (fixed and portable) | `anzca::primary::equipment` |
| BT_SQ 1.12 | Principles and safe operation of vaporisers | `anzca::primary::equipment` |
| BT_SQ 1.13 | Classification and description of breathing systems — clinical utility and hazards | `anzca::primary::equipment` |
| BT_SQ 1.14 | Systems for supplemental oxygen delivery — advantages and disadvantages | `anzca::primary::equipment` |
| BT_SQ 1.15 | CO2 absorption in a circle system and associated hazards | `anzca::primary::equipment` |
| BT_SQ 1.18 | Principles of surgical diathermy, safe use and hazards | `anzca::primary::equipment` |
| BT_RA 1.8 | Principles of ultrasound imaging | `anzca::primary::equipment` |

---

### 24. Miscellaneous Pharmacology
| Code | Learning outcome | Section tag |
|---|---|---|
| BT_PO 1.3 | Adverse effects of antimicrobial agents | `anzca::primary::pharmacology::miscellaneous` |
| BT_PO 1.3a | Pharmacology of commonly encountered illicit drugs and their interactions with anaesthetic drugs | `anzca::primary::pharmacology::miscellaneous` |
| BT_PO 1.4a | Perioperative adverse effects and drug interactions of herbal medicines | `anzca::primary::pharmacology::miscellaneous` |
| BT_PO 1.100 | Pharmacology of histamine antagonists | `anzca::primary::pharmacology::miscellaneous` |
| BT_PO 1.125 | Major perioperative implications of cancer chemotherapy agents and immunotherapy | `anzca::primary::pharmacology::miscellaneous` |
| BT_SQ 1.20 | Potential perioperative effects of radiological contrast agents | `anzca::primary::pharmacology::miscellaneous` |

---

### 25. General / Overarching Principles
| Code | Learning outcome | Section tag |
|---|---|---|
| AR_ME 1.3 | Apply knowledge of clinical and biomedical sciences relevant to anaesthesia | `anzca::primary::general` |
| AR_ME 3.2 | Demonstrate knowledge of procedure: indications, contraindications, anatomy, technique, side-effects and complications | `anzca::primary::general` |

---

## Code Tag Format

Derive the code tag by removing the space in the code and replacing with an underscore:

| Curriculum code | Code tag |
|---|---|
| BT_GS 1.1 | `anzca::code::BT_GS_1.1` |
| BT_PO 1.82a | `anzca::code::BT_PO_1.82a` |
| SS_OB 1.1 | `anzca::code::SS_OB_1.1` |
| AR_ME 1.3 | `anzca::code::AR_ME_1.3` |

---

## When Content Does Not Map to a Specific Code

- Apply the section tag only — omit the `anzca::code::` tag
- Do not guess a code
- If content clearly spans more than one code, apply all applicable code tags
