# Aetheris Governed AI Benchmark Architecture v1.1

**Five-Track Governed-State Evaluation Suite**  
**Status:** Canonical working architecture; not a validated benchmark release  
**Date:** 2026-07-10  
**Owner:** Thomas Giza / Aetheris Consulting  
**Parent architecture:** ACIM-E v1.0

---

## 1. Executive definition

The Aetheris Governed AI Benchmark Architecture evaluates whether an AI-enabled system can move an operational, scientific, clinical, organizational, or cognitive state forward correctly while remaining inside evidence, authority, safety, compliance, and human-outcome boundaries.

The architecture does not replace capability benchmarks. Capability tests establish whether a model can reason, retrieve, generate, code, classify, or use tools. The Aetheris suite addresses a different question:

> Can the complete AI-enabled workflow create a valid state transition, through the correct organizational path, without unauthorized action, hidden harm, or benchmark-to-reality divergence?

The evaluated unit is therefore not only the base model. It may include prompts, retrieval, tools, agents, humans, policies, data, connectors, workflow controls, telemetry, and commit authority.

The unified killer metric is:

> Did the AI-enabled system move the state forward correctly, within authority boundaries, without introducing a material error or protected-outcome degradation that the approved baseline and review process should have prevented?

---

## 2. Currentness audit

The June 2026 **Aetheris Benchmark Suite v1.0** contained the durable core of this architecture, but it predates ACIM-E v1.0 and Benchmark VOC integration. The following corrections define v1.1.

| Area | June v1.0 position | v1.1 current position |
|---|---|---|
| Core suite | Five domain benchmarks | Retained: GPO, SciDisc, Medical, Optimization, Education |
| AI Core | Implicit in governance | Explicit cross-cutting implementation spine, not a sixth benchmark track |
| Gate sequence | Universal Gate 0–9 sequence | ACIM-E Gates 0–8; continuous monitoring occurs after commit rather than as Gate 9 |
| Optimization scope | Industrial operations optimization | Organizational and operational optimization, including industrial, service, merchandising, administrative, and enterprise functions |
| Human baseline | Presented as available and primary across all tracks | Contextual comparator requiring source, scope, date, competence definition, confidence, and local calibration |
| Readiness delta | Negative time or error delta implied automatic failure | Multi-objective readiness; slower performance may be acceptable when safety, quality, resilience, or authority performance materially improves |
| Hard gates | Authority and selected safety failures | Retained and expanded; no composite score can offset a hard-gate failure |
| Benchmark layers | Primarily five core tracks | Adds cross-cutting, relational, meta, UTSS, VOC, and production-observation layers |
| Reality calibration | Not integrated into the suite | Benchmark VOC and Outcome Validation Score are mandatory calibration mechanisms for deployed systems |
| Public status | Confidential working document | Public MIT-licensed repository specification; still a working architecture |
| Evidence claims | Some uncited domain-wide baseline claims | Removed or reframed as evidence requirements; no unsupported universal performance claims |

This v1.1 publication supersedes the June v1.0 document for repository use while preserving the source document as architecture lineage.

---

## 3. Governing doctrine

1. **Governed state change, not answer scoring.** Correct text is insufficient when the workflow, action, routing, or commit state is wrong.
2. **Authority is independently scored.** A technically correct result produced or committed outside permitted authority is a failed case.
3. **Safety-critical failure is non-compensable.** A composite average cannot erase patient harm, unsafe product release, prohibited research operationalization, hard-constraint violation, or comparable protected failure.
4. **Evidence states remain typed.** Hypothesized, simulated, validated, authorized, executed, observed, reconciled, and committed states cannot be silently collapsed.
5. **The baseline is contextual.** Human or current-process performance is useful only when the comparator represents the same role, task, conditions, population, and authority level.
6. **Optimization is multi-objective.** Time and cost gains cannot override quality, safety, rights, access, workload sustainability, privacy, compliance, resilience, or served-entity outcomes.
7. **Independent observation outranks self-report.** Model or agent claims are compared with actual tool use, workflow state, human review, and system telemetry.
8. **Scores remain provisional until reality-calibrated.** Benchmark VOC and observed outcomes determine whether the suite is measuring what matters.
9. **Benchmark specifications are versioned controls.** Cases, weights, thresholds, evidence sources, and retirement decisions require provenance and change governance.
10. **Commit authority remains outside the evaluated agent.** Gate 8, not the execution agent, promotes validated learning into governed organizational state.

---

## 4. Benchmark architecture stack

```text
Layer 0 — External capability prerequisites
    Model and system competence required for the intended task

Layer 1 — Five-Track Core Benchmarks
    GPO-Bench
    SciDisc-Bench
    Medical-Bench
    Optimization-Bench
    Education-Bench

Layer 2 — Cross-Cutting Benchmarks
    TSC | SecOps | RevT | RegComp | OrgComm | WTT

Layer 3 — Relational Benchmarks
    IPeer | FedComp | Maturity

Layer 4 — Meta-Benchmark
    CCIB

Layer 5 — UTSS Scenario Stress Tests
    Matrix | Batdog | Apollo 13 CO₂ | Groundhog Day

Layer 6 — Benchmark VOC
    Served-entity and operator outcome calibration
    Gap taxonomy
    Outcome Validation Score

Layer 7 — Production Observation
    Telemetry, incidents, exceptions, drift, forecast variance,
    subgroup outcomes, and Gate 8 learning
```

The canonical acronyms in Layers 2–4 are preserved because their long-form names have not yet been formally frozen. A registry release must define each expansion, scope, owner, scoring method, and version before claiming those benchmarks are operational.

---

## 5. Unified benchmark object

Every benchmark case uses a common governed-state object.

```text
Oriented Context
+ Triggering Event or Question
+ Evidence Corpus
+ Starting State
+ Constraint Set
+ Authority Boundary
+ Allowed Tools and Actions
+ Protected Countermetrics
+ Expected State Transition
+ Independent Observation Plan
→ Candidate Output or Action
→ Gate Evaluation
→ Domain Evaluation
→ Outcome Observation
→ Reconciliation and Learning
```

### 5.1 Required case fields

Every case must define:

- benchmark and sub-benchmark identifier;
- version and case status;
- implementation track;
- industry, domain, jurisdiction, and organization type;
- business function and workflow scope;
- affected and served populations;
- starting state and trigger;
- evidence corpus and data provenance;
- allowed tools, connectors, and actions;
- authority, review, and commit boundaries;
- expected behavior and prohibited behavior;
- primary metrics and protected countermetrics;
- hard gates;
- domain scoring rubric;
- baseline or comparator protocol;
- uncertainty and confidence treatment;
- subgroup and distribution-shift requirements;
- observability and telemetry requirements;
- VOC plan where the case represents a deployed workflow;
- pass, conditional-pass, fail, pause, rollback, and escalation rules;
- case owner, reviewers, change history, and retirement criteria.

### 5.2 Evidence typing

Case evidence must distinguish:

- fact;
- reported observation;
- retrieved source;
- assumption;
- hypothesis;
- simulation output;
- model output;
- human judgment;
- validated result;
- authorized action;
- observed outcome;
- committed organizational state.

An output cannot inherit a stronger evidence state merely because it is fluent, repeated, or produced by a higher-capability model.

---

## 6. ACIM-E gate integration

The benchmark suite uses the current ACIM-E organizational gate profile.

| Gate | Benchmark function |
|---|---|
| Gate 0 — Organizational orientation | Confirm actor locus, track, industry, jurisdiction, workflow, data, authority, constraints, and reasoning mode. |
| Gate 1 — Target workflow orientation | Confirm the bounded task, affected entities, intended outcome, dependencies, and review owner. |
| Gate 2 — Baseline and evidence sufficiency | Determine whether the comparator, evidence corpus, case specification, and expected state are adequate. |
| Gate 3 — Candidate design authorization | Approve the candidate output, workflow, or system configuration for simulation or controlled evaluation. |
| Gate 4 — Forecast and simulation validation | Test normal, adverse, authority, security, safety, subgroup, drift, and recovery scenarios. |
| Gate 5 — Pilot authorization | Approve the smallest bounded real-world test capable of generating decision-quality evidence. |
| Gate 6 — Operational evaluation | Compare observed performance with the baseline, benchmark thresholds, countermetrics, incidents, and VOC. |
| Gate 7 — Reconciliation | Resolve contradictions, score-outcome gaps, residual risk, and ownership before recommendation. |
| Gate 8 — Organizational commit | Promote approved changes to benchmark cases, thresholds, workflow baselines, policy, or production authority. |

Continuous monitoring, recalibration, and reorientation follow Gate 8. They are lifecycle functions, not a separate Gate 9.

### 6.1 Gate verdicts

Each gate records:

- pass;
- conditional pass;
- pause;
- fail;
- rollback;
- blocked pending evidence;
- blocked pending authority;
- not applicable with justification.

A gate verdict must include evidence, owner, conditions, expiry, and provenance.

---

## 7. Baseline and comparator protocol

### 7.1 Baseline doctrine

The human or current-process baseline is not a theoretical optimum and is not presumed safe, fair, efficient, or correct. It represents the approved comparator for the evaluated workflow.

A valid baseline packet includes:

- comparator role and competence standard;
- task and workflow equivalence;
- operating conditions and workload;
- population and subgroup coverage;
- sample size and collection period;
- error taxonomy;
- timing definition;
- authority level;
- data and tool access;
- quality and safety controls;
- source and provenance;
- confidence interval or uncertainty statement;
- known bias and measurement limitations;
- date and refresh condition.

Published data may inform a baseline, but local workflow calibration is required when the organization, population, authority structure, tools, or task distribution materially differs.

### 7.2 Comparator hierarchy

Use the strongest available comparator appropriate to the case:

1. validated domain ground truth;
2. verified physical, mathematical, or programmatic outcome;
3. adjudicated expert consensus;
4. qualified-human performance under equivalent conditions;
5. current organizational process performance;
6. historical benchmark or external dataset;
7. simulation proxy;
8. declared provisional comparator.

Lower-confidence comparators require stronger uncertainty reporting and narrower readiness claims.

### 7.3 No single universal efficiency delta

The suite does not use a rule that every negative time or error delta automatically fails readiness. Readiness is evaluated across a vector:

```text
technical validity
+ authority compliance
+ safety and protected outcomes
+ quality
+ time
+ cost
+ resilience
+ human workload
+ accessibility and fairness
+ compliance evidence
+ reversibility
+ confidence
```

A system may be slower than the current process and still be valuable when it materially improves safety, auditability, access, quality, or resilience. Conversely, a faster system fails when protected outcomes deteriorate beyond tolerance.

---

## 8. Scoring and readiness protocol

### 8.1 Score classes

Each case produces:

1. **Hard-gate verdicts** — pass/fail controls that cannot be averaged away.
2. **Domain scores** — track-specific quality dimensions.
3. **Operational scores** — time, cost, availability, workload, and recovery.
4. **Authority scores** — routing, escalation, tool permissions, and commit behavior.
5. **Outcome scores** — observed effects on operators and served entities.
6. **Confidence statement** — evidence quality, sample limits, and uncertainty.

### 8.2 Readiness expression

```text
Readiness =
    all_required_hard_gates_pass
    AND minimum_domain_thresholds_met
    AND protected_countermetrics_within_tolerance
    AND authority_behavior_valid
    AND evidence_sufficient_for_claim
    AND rollback_and_observation_controls_ready
```

A weighted composite may summarize domain performance, but it may not override any failed hard gate.

### 8.3 Case verdicts

- **Pass:** required gates and thresholds met within the validated envelope.
- **Conditional pass:** acceptable only under stated constraints, monitoring, or human review.
- **Fail:** required threshold or hard gate not met.
- **Pause:** insufficient evidence, stale orientation, or unresolved contradiction.
- **Rollback:** deployed behavior exceeded approved tolerances or authority.
- **Retire:** case no longer represents current technology, workflow, law, population, or risk.

### 8.4 Required reporting

Every reported score must state:

- benchmark and case version;
- evaluated system configuration;
- model, prompt, retrieval, tools, agents, and human-review configuration;
- data window and environment;
- sample count;
- failed and excluded cases;
- subgroup results;
- hard-gate failures;
- confidence and limitations;
- comparison method;
- whether results are simulated, piloted, or production-observed;
- whether VOC and OVS are available.

---

## 9. Benchmark hierarchy

### 9.1 Five-Track Core Benchmarks

- **GPO-Bench:** production, manufacturing, quality, controlled change, business operations, and cross-layer incident response.
- **SciDisc-Bench:** literature synthesis, hypothesis generation, experimental design, simulation, causal inference, rediscovery, replication, and prospective discovery.
- **Medical-Bench:** clinical reasoning, treatment-planning support, documentation, high-liability routing, and clinical-research design under specialty and authority constraints.
- **Optimization-Bench:** organizational and operational optimization across industrial, service, merchandising, administrative, financial, logistical, technical, public-sector, and other constrained systems.
- **Education-Bench:** content accuracy, pedagogical design, adaptive tutoring, assessment, curriculum, durable learning, and learner protection.

Detailed profiles are published in [Five-Track Core Benchmarks](./01-five-track-core-benchmarks.md).

### 9.2 Cross-Cutting Benchmarks

The current registry retains:

```text
TSC | SecOps | RevT | RegComp | OrgComm | WTT
```

These benchmarks evaluate concerns that recur across multiple tracks, including technical/system controls, security operations, business or mission value, regulatory and compliance performance, organizational communication, and workflow/tool transfer behavior. These descriptions are functional orientation only; the acronym expansions and formal scoring specifications remain unfrozen.

### 9.3 Relational Benchmarks

The current registry retains:

```text
IPeer | FedComp | Maturity
```

Relational benchmarks evaluate performance across peers, federated or multi-organization contexts, and organizational capability maturity. Formal definitions, cases, and scoring are required before operational use.

### 9.4 Meta-Benchmark

```text
CCIB
```

CCIB evaluates the integrity and usefulness of the benchmark system itself. At minimum, the meta-benchmark should test calibration, coverage, case diversity, anti-gaming controls, inter-rater reliability, benchmark-to-outcome alignment, version governance, and retirement discipline. The long-form name remains unfrozen.

---

## 10. UTSS scenario stress tests

UTSS tests structural behavior under pressure rather than ordinary task accuracy.

### Matrix Test

Tests hidden-state deception, conflicting control layers, apparent reality, and whether the system mistakes presented content for authorized truth.

### Batdog Protocol

Tests multimodal or cross-domain reconstruction, relational inference, fragmented evidence integration, and resistance to invented authority.

### Apollo 13 CO₂ Test

Tests resource-constrained emergency reasoning, prioritization, improvised solution design, communication, and safe operation under time and material limits.

### Groundhog Day Test

Tests repeated-loop learning. The system must incorporate previous failure evidence, update strategy, and demonstrate correction rather than produce a merely different fluent answer.

UTSS results supplement track-specific cases; they do not replace domain validation, production telemetry, or protected outcome measurement.

---

## 11. Benchmark VOC and outcome validation

Benchmark VOC is the external reality-calibration layer for the suite. It compares benchmark movement with operator and served-entity outcomes, generates new case candidates, and identifies benchmark defects.

The canonical cycle is:

```text
Stakeholder population
+ collection timeframe
+ benchmark score context
+ real outcome experience
+ identified gap
→ calibration signal
+ new benchmark cases
+ Outcome Validation Score
```

Gap classes are:

- calibration gap;
- coverage gap;
- case-library gap;
- authority-boundary gap;
- human-baseline gap;
- unknown gap.

The OVS is a provisional correlation diagnostic:

```text
OVS = corr(
  normalized change in benchmark score,
  normalized change in protected served-entity outcomes
)
```

OVS ranges from −1.0 to +1.0 but does not prove causation. Sample sufficiency, delayed outcomes, population shifts, confounding changes, aggregation rules, and confidence intervals must be reported.

If safety-critical outcome failures repeatedly pass the benchmark suite, benchmark-driven optimization authority is suspended pending recalibration.

See [Benchmark VOC and Outcome Validation](./02-benchmark-voc-and-outcome-validation.md).

---

## 12. Benchmark governance

### 12.1 Registry requirements

Each benchmark and sub-benchmark must maintain:

- canonical identifier and long-form name;
- owner and review body;
- purpose and non-goals;
- applicable tracks and domains;
- case schema;
- scoring and hard gates;
- baseline requirements;
- protected countermetrics;
- case-library provenance;
- development, validation, and holdout partitions;
- anti-memorization controls;
- release version;
- known limitations;
- production calibration status;
- retirement and replacement rules.

### 12.2 Anti-gaming controls

Benchmark governance must:

- separate development from holdout cases;
- rotate or refresh cases;
- preserve failed cases;
- test prompt-specific tuning and memorization;
- compare self-report with independent observation;
- include distribution shifts and rare adverse cases;
- track subgroup performance;
- prevent test leakage;
- version datasets, rubrics, tools, and judges;
- monitor benchmark-to-outcome correlation;
- suspend optimization authority when scores improve while protected outcomes deteriorate.

### 12.3 Judge governance

Human, model, and automated judges must be treated as measurement instruments. Reports must identify:

- judge type and version;
- rubric;
- calibration set;
- disagreement rate;
- adjudication process;
- conflicts of interest;
- known biases;
- inter-rater or repeatability evidence where applicable.

A model may assist evaluation but cannot be the sole unvalidated judge of its own outputs.

---

## 13. Open research and implementation priorities

The following remain unresolved before the suite can be represented as a validated public benchmark product:

1. Freeze long-form names and formal definitions for all cross-cutting, relational, and meta identifiers.
2. Publish track-specific scoring rubrics and automated-versus-expert measurement rules.
3. Build representative, rights-cleared case libraries with development and holdout partitions.
4. Establish inter-rater reliability and adjudication protocols.
5. Define human/current-process baseline collection methods by track and sub-domain.
6. Validate thresholds using pilot and production evidence.
7. Specify OVS sample-size, confidence, lag, aggregation, and causal-inference limits.
8. Define novelty-versus-groundedness treatment for SciDisc-Bench.
9. Build safe prospective-discovery infrastructure and time-deferred scoring.
10. Define durable learning measurement for Education-Bench.
11. Build adversarial authority-escalation case libraries across all tracks.
12. Establish benchmark security, leakage detection, and case retirement operations.
13. Validate benchmark portability across industries, jurisdictions, organizations, populations, and model architectures.
14. Produce regulated-sector control mappings and domain-review procedures.

Until these are complete, scores should be described as results from an **Aetheris benchmark architecture implementation**, not as universally validated measures of AI safety or readiness.

---

## 14. Source lineage and change log

### Source lineage

- *Aetheris Unified Governed-State Benchmark Architecture*, June 2026.
- *Aetheris Benchmark Suite v1.0*, June 2026.
- *Aetheris VOC Architecture v0.2.1 Corrected*, June 2026.
- *Organizational / Enterprise AI Core Implementation Model — ACIM-E v1.0*, July 2026.
- Existing Gate 0 and WEOF repository specifications.

### v1.1 — 2026-07-10

- Reconciled the benchmark suite with ACIM-E.
- Replaced Gate 0–9 with Gates 0–8 plus continuous operations.
- Clarified AI Core as the cross-cutting implementation spine.
- Broadened Optimization-Bench to organizational and operational optimization.
- Replaced the universal efficiency-delta rule with multi-objective readiness.
- Corrected unsupported claims about universal human-baseline availability.
- Added cross-cutting, relational, meta, UTSS, VOC, and production-observation layers.
- Added baseline, judge, anti-gaming, case-versioning, and reporting requirements.
- Preserved unfrozen benchmark acronyms without inventing expansions.
- Declared the architecture’s current non-validated working status.

---

## 15. Document control

**Canonical owner:** Thomas Giza / Aetheris Consulting  
**Change authority:** Document owner or explicitly delegated benchmark governance authority  
**Commit rule:** Material changes require a version increment, change-log entry, evidence annotation, and registry update  
**Repository license:** MIT