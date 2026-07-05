# Gate 0 Depth Registry

The implementation path determines the default depth of Gate 0 orientation.

Industry, compliance, business type, locus, boundary topology, and completion horizon can only maintain or increase required orientation depth. They cannot reduce it.

---

## Registry Summary

| Track | Default Depth | Escalation Logic |
|---|---|---|
| T1 AI Core / Optimization | Single | Multi when measurement affects people, authority, systems, money, compliance, or external commitments |
| T2 Production / Manufacturing | Multiple | Physical-world process, safety, machine, quality, worker, and material-flow concerns are default |
| T3 Scientific Discovery | Conditional | Single for explanation; multi for experiment, evidence, ethics, safety, claim, or lab/simulation movement |
| T4 Medical / Healthcare | Multiple | Patient-subject, care authority, acuity, privacy, and action tier require separate orientation |
| T5 Education / Human Capability | Conditional | Single for adult self-learning; multi for minors, learner-subject separation, grading, institutions, accommodations, or capability judgments |

---

## T1 — AI Core / Optimization

### Default

```text
single
```

### Purpose

Measure, compare, benchmark, improve, or optimize work.

### Typical Objects

- time to completion
- error rate
- throughput
- quality
- drift
- rework
- AI vs human comparison
- baseline performance
- workflow efficiency
- stamina across workflow duration

### Required Base Islands

```text
G0 Universal Orientation
G0 Work Object Orientation
G0 Metric / Baseline Orientation
G0 Comparison Condition Orientation
G0 Work Bridge
```

### Multi-Gate Triggers

- human worker data
- named employee comparison
- HR consequence
- live system change
- customer-facing effect
- money movement
- legal/compliance exposure
- external dependency
- irreversible action

### Rule

> Optimization is single-Gate-0 when it measures work. It becomes multi-Gate-0 when the measurement affects people, authority, live systems, money, compliance, or external commitments.

---

## T2 — Production / Manufacturing

### Default

```text
multiple
```

### Purpose

Orient to physical production, material flow, machinery, safety, quality, and throughput.

### Required Islands

```text
G0 Universal Orientation
G0 Physical Process Orientation
G0 Machine / Tooling Orientation
G0 Human Worker Safety Orientation
G0 Material / Product Quality Orientation
G0 Authority / Control Boundary
G0 Completion Horizon
G0 Work Bridge
```

### Core Risk Surfaces

- physical harm
- machine control
- material loss
- defects
- downtime
- worker safety
- product safety
- quality escapes
- recall or warranty exposure
- environmental exposure

### Rule

> Production and manufacturing usually require multiple Gate 0 orientation passes because physical-world consequences exist before the exact work object is defined.

---

## T3 — Scientific Discovery

### Default

```text
conditional
```

### Single-Gate Cases

- explain a paper
- summarize a concept
- compare theories
- teach background knowledge
- literature overview without claim generation

### Multi-Gate Cases

- design an experiment
- interpret data
- evaluate a novel hypothesis
- make causal claims
- move from simulation to lab
- handle human-subject data
- handle animal-subject data
- work with biological, chemical, or physical safety risks
- produce claim-strength recommendations

### Required Islands When Complex

```text
G0 Universal Orientation
G0 Research Object Orientation
G0 Hypothesis / Claim Orientation
G0 Evidence / Method Orientation
G0 Model-vs-Reality Boundary
G0 Ethics / Safety Orientation
G0 Claim Strength Orientation
G0 Work Bridge
```

### Rule

> Scientific discovery is single-Gate-0 for explanation and multi-Gate-0 when the work touches method, evidence, experiment, ethics, safety, or claim generation.

---

## T4 — Medical / Healthcare

### Default

```text
multiple
```

### Purpose

Orient to patient-subject, user relation, care authority, clinical risk, data privacy, acuity, and allowed action tier.

### Required Islands

```text
G0 Universal Orientation
G0 Patient-Subject Orientation
G0 User-Relation Orientation
G0 Care Setting Orientation
G0 Authority Chain Orientation
G0 Data / PHI / Provenance Orientation
G0 Risk / Acuity Orientation
G0 Allowed Action Tier Orientation
G0 Work Bridge
```

### User Loci

- patient
- caregiver
- advocate
- doctor
- nurse
- care team member
- hospital administrator
- payer
- researcher

### Patient-Subject Possibilities

- the user
- someone else
- a child
- a vulnerable adult
- a population
- unknown

### Rule

> Medical almost always requires multiple Gate 0 orientation passes because patient-subject, user relation, care authority, risk, privacy, and action tier must be resolved before work can be safely defined.

---

## T5 — Education / Human Capability

### Default

```text
conditional
```

### Single-Gate Cases

- teach me a concept
- quiz me
- help me study
- explain class material
- adult self-learning
- low-stakes practice

### Multi-Gate Cases

- minor learner
- learner is not the user
- grading
- credentialing
- institutional assessment
- disability accommodation
- behavioral evaluation
- human capability judgment
- career qualification

### Required Islands When Complex

```text
G0 Universal Orientation
G0 Learner-Subject Orientation
G0 User-Relation Orientation
G0 Teacher / Institution Authority Orientation
G0 Assessment Stakes Orientation
G0 Developmental / Accommodation Orientation
G0 Work Bridge
```

### Rule

> Education is single-Gate-0 for personal self-learning and multi-Gate-0 when learner-subject separation, institutional authority, grading, minors, accommodations, or capability evaluation appear.

---

## General Escalation Formula

```text
Required Gate 0 Depth =
Implementation Path Default
+ Industry Risk Escalators
+ Compliance Shell Requirements
+ Business Type Modifiers
+ Locus / Boundary Modifiers
+ Completion Horizon Modifiers
```

---

## Invariant

```text
Implementation path sets the default.
Industry and compliance can escalate.
Business type can refine or escalate.
Locus, boundary, and completion horizon can escalate.
No lower layer can reduce required controls.
```
