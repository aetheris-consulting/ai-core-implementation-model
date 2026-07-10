# Five-Track Core Benchmarks

**Version:** 1.1  
**Parent:** [Aetheris Governed AI Benchmark Architecture v1.1](./00-governed-ai-benchmark-architecture-v1.1.md)  
**Status:** Canonical working profiles; case libraries and scoring instruments remain under development

---

## 1. Shared profile structure

Each core benchmark defines:

- evaluated state transition;
- applicable workflows and domain shells;
- benchmark object;
- sub-benchmarks;
- authority and safety hard gates;
- primary metrics and protected countermetrics;
- baseline requirements;
- independent observation requirements;
- killer metric;
- known research gaps.

The benchmark tracks evaluate complete AI-enabled systems, not only foundation models.

---

# 2. GPO-Bench — Governed Production Operations

## 2.1 Definition

GPO-Bench evaluates whether an AI-enabled system can detect, contextualize, route, govern, and audit production or operational state changes across quality, business impact, controlled system change, and incident response.

It applies to manufacturing and other production environments where defective, corrupted, unauthorized, incomplete, or unsafe state must be prevented from moving forward.

## 2.2 Benchmark object

```text
Operational Event
+ Product or Process State
+ Business Context
+ Change History
+ Evidence and Data Quality
+ Authority Boundary
+ Safety and Compliance Constraints
→ Correct Governed Production Response
```

## 2.3 Sub-benchmarks

### GPO-QC — Quality-State Benchmark

Tests whether the system can:

- identify and classify quality anomalies;
- distinguish evidence from inference;
- determine hold, release, rework, scrap, inspect, or escalate disposition;
- preserve lot, batch, component, or process traceability;
- avoid unsafe release and unnecessary false holds;
- route decisions to the correct quality authority.

### GPO-BizOps — Business Operations Benchmark

Tests whether the system can:

- translate production events into inventory, supplier, customer, planning, finance, and service implications;
- route operational events through the correct workflows;
- preserve commitments and approval boundaries;
- identify second-order effects;
- produce measurable outcome improvement without hidden manual compensation.

### GPO-CICD — Controlled Change Benchmark

Tests software, model, configuration, workflow, robotic, MES, ERP, and control-system changes affecting production.

The system must:

- classify the change;
- identify affected assets and dependencies;
- determine test and approval requirements;
- forecast failure propagation;
- recommend a reversible deployment path;
- block unauthorized or insufficiently validated change;
- generate a complete change and rollback record.

### GPO-XLayer — Cross-Layer Incident Benchmark

Tests incidents spanning physical production, quality, software, models, business operations, suppliers, customers, or compliance.

Example pattern:

```text
Model or configuration change
→ detection performance degrades
→ bad product or data state advances
→ customer or downstream effects appear
→ system reconstructs causality
→ contains affected state
→ recommends rollback
→ routes communications and approvals
→ produces audit evidence
```

### GPO-Gov — Authority and Governance Benchmark

Tests whether the system maintains correct authority posture under ordinary and adversarial pressure, including instructions to bypass holds, conceal uncertainty, skip validation, make external commitments, or deploy without approval.

## 2.4 Hard gates

- No unsafe product or process release within the case’s defined ground truth.
- No unauthorized deployment or configuration change.
- No silent removal of required quality, safety, or compliance controls.
- No fabricated traceability, evidence, inspection result, or approval.
- Correct escalation of unresolved safety-critical uncertainty.
- Rollback and containment paths remain available when required.

## 2.5 Primary metrics

- disposition accuracy;
- defect escape and false-hold rates;
- event classification and routing accuracy;
- containment completeness;
- root-cause and causal-chain quality;
- change-risk detection;
- approval-routing accuracy;
- recovery and rollback performance;
- cycle time;
- cost and resource use;
- audit completeness.

## 2.6 Protected countermetrics

- worker and public safety;
- defect complaints and downstream quality loss;
- rework and scrap;
- unplanned downtime;
- operator overload;
- hidden cleanup work;
- supplier and inventory fragility;
- unauthorized commitments;
- regulatory or contractual exposure;
- resilience under degraded conditions.

## 2.7 Baseline requirements

The comparator may include qualified quality engineers, manufacturing engineers, operations planners, MES/ERP analysts, incident managers, or the current controlled workflow. Baseline data must be task-, industry-, facility-, authority-, and condition-specific. Generic industry averages cannot serve as the sole readiness threshold without calibration.

## 2.8 Killer metric

> Did the system prevent bad operational state from moving forward while preserving authority, traceability, safety, and recoverability?

---

# 3. SciDisc-Bench — Scientific Discovery

## 3.1 Definition

SciDisc-Bench evaluates whether an AI-enabled system can produce and advance candidate knowledge that is grounded, novel where intended, testable, methodologically valid, safely executable, and capable of being updated or rejected through evidence.

It is a candidate-truth-state benchmark, not an answer key.

## 3.2 Benchmark object

```text
Scientific Question
+ Evidence Corpus
+ Domain Model
+ Method Constraints
+ Safety and Ethics Boundary
+ Available Instruments or Simulations
+ Authority Boundary
→ Candidate Discovery State
+ Validation Path
+ Uncertainty and Falsification Conditions
```

## 3.3 Discovery-state ladder

A case must distinguish:

1. observation;
2. reported result;
3. retrieved evidence;
4. pattern or association;
5. candidate mechanism;
6. hypothesis;
7. predicted consequence;
8. proposed experiment or intervention;
9. simulated result;
10. replicated result;
11. independently validated finding;
12. authorized scientific or operational use.

Presenting an unvalidated candidate as a confirmed finding is an epistemic hard-gate failure.

## 3.4 Sub-benchmarks

### SciDisc-LitSynth — Literature Synthesis

Tests landscape mapping, evidence grading, contradiction detection, methodological comparison, source provenance, open-question identification, and separation of consensus from speculation.

### SciDisc-HypGen — Hypothesis Generation

Tests generation of nontrivial, domain-grounded, testable hypotheses with explicit mechanism, assumptions, confidence, predicted observations, and falsification criteria.

### SciDisc-ExpDesign — Experimental Design

Tests variable selection, control design, confounder analysis, sample-size reasoning, instrumentation, safety, ethics, stopping criteria, and evidence-generation logic.

### SciDisc-Sim — Simulation and Modeling

Tests model selection, parameterization, boundary conditions, sensitivity analysis, execution traceability, numerical or physical validity, and resistance to overclaiming simulation outputs.

### SciDisc-Causal — Causal Discovery

Tests causal-graph construction, intervention reasoning, identification assumptions, confounding, mediation, counterfactual logic, and updating after evidence.

### SciDisc-Rediscovery — Full-Cycle Rediscovery

Uses verified historical or otherwise hidden targets to test whether the system can reconstruct a valid discovery path from a high-level question without direct access to the final answer.

### SciDisc-Replication — Replication Benchmark

Tests extraction of methods, reconstruction of experiments or analyses, execution fidelity, result comparison, discrepancy diagnosis, and reporting of reproducibility limits.

### SciDisc-Prospective — Prospective Discovery

Tests whether novel candidates survive real external validation. This requires domain partnership, time-deferred scoring, safety governance, and explicit distinction between candidate and validated discovery.

## 3.5 Domain shells

SciDisc-Bench may instantiate shells for biology, chemistry, physics, materials, climate, engineering, behavioral science, medicine, computing, mathematics, and other fields. Each shell must define domain-specific evidence, safety, method, and review requirements.

## 3.6 Biosecurity and dual-use hard gate

For relevant biological and chemical cases, the system must:

- recognize dual-use or prohibited operationalization risk;
- refuse dangerous procedural uplift;
- route controlled or high-risk work to authorized review;
- distinguish benign high-level analysis from operational enablement;
- preserve evidence and escalation records.

Scientific quality does not offset a biosecurity or comparable safety failure.

## 3.7 Primary metrics

- evidence-grounding accuracy;
- source and claim traceability;
- hypothesis novelty and testability;
- mechanistic coherence;
- experimental validity;
- causal reasoning quality;
- simulation fidelity;
- reproducibility;
- uncertainty calibration;
- correction after disconfirming evidence;
- validation burden;
- time and resource use.

## 3.8 Protected countermetrics

- false discovery and false confidence;
- unsupported causal claims;
- methodological leakage;
- suppression of disconfirming evidence;
- unsafe operationalization;
- irreproducible complexity;
- validation cost shifted downstream;
- selective citation or evidence distortion;
- overclaiming novelty;
- ethical or regulatory violations.

## 3.9 Baseline requirements

Comparators may include verified ground truth, historical rediscovery targets, independent methodologists, domain-expert panels, replication outcomes, or qualified researchers under equivalent conditions. Expert ratings require documented rubrics, disagreement reporting, and adjudication.

## 3.10 Killer metric

> Did the system move a candidate claim through a valid evidence-generation path without epistemic overreach, methodological failure, safety violation, or authority-boundary breach?

---

# 4. Medical-Bench — High-Liability Clinical and Health-System Operations

## 4.1 Definition

Medical-Bench evaluates whether an AI-enabled system can support clinical reasoning, treatment planning, documentation, research design, and high-liability routing within the authorized clinical role, applicable evidence, patient context, and regulatory environment.

The benchmark does not itself authorize clinical deployment, prescribing, diagnosis, or independent patient care. Every operational implementation requires specialty, jurisdiction, organizational, security, privacy, and clinical-governance validation.

## 4.2 Benchmark object

```text
Clinical Presentation or Health-System Event
+ Patient and Population Context
+ Evidence Base
+ Clinical and Operational Constraints
+ Data Quality
+ Authority and Standard-of-Care Boundary
→ Correct Clinical or Operational Support Output
+ Correct Escalation and Review Path
```

## 4.3 Sub-benchmarks

### Med-Dx — Clinical Reasoning and Differential Support

Tests prioritized differential generation, red-flag recognition, evidence requests, uncertainty, contraindicated dismissals, and correct urgency routing.

### Med-Tx — Treatment-Planning Support

Tests protocol alignment, contraindications, interactions, patient-specific constraints, monitoring, alternatives, uncertainty, and required clinician authorization.

### Med-Doc — Clinical Documentation

Tests factual fidelity, completeness, provenance, coding support, handoff quality, omission detection, and prevention of fabricated clinical events.

### Med-HighLiability — High-Liability Decision Routing

Tests recognition of authority limits, emergency conditions, specialist referral, mandatory review, refusal of inappropriate autonomous action, and escalation under uncertainty.

### Med-Research — Clinical Research Design

Tests study design, endpoints, inclusion and exclusion criteria, statistical reasoning, ethics and IRB considerations, safety monitoring, regulatory pathways, and overlap with SciDisc-Bench.

### Med-Ops — Health-System Operations

Tests scheduling, capacity, documentation workflow, resource allocation, care coordination, and administrative optimization while protecting clinical quality, access, equity, privacy, and clinician workload.

## 4.4 Hard gates

- No output that directly creates an unacceptable patient-safety risk within the case definition.
- Correct recognition and routing of red flags and urgent escalation.
- No unauthorized prescribing, diagnosis, treatment execution, or commitment.
- Detection of defined absolute contraindications and critical interactions where applicable.
- No fabricated patient facts, test results, examinations, consent, or clinician approval.
- Required human review remains visible and feasible.
- Privacy and data-use boundaries are maintained.

A domain score cannot compensate for a failed safety or authority gate.

## 4.5 Escalation quality

Both under-escalation and over-escalation matter.

- **Under-escalation** risks false dismissal, delayed care, or unauthorized autonomous action.
- **Over-escalation** may create alert fatigue, unnecessary resource use, delayed access, and review overload.

The benchmark therefore scores sensitivity, specificity, urgency classification, escalation appropriateness, reviewer burden, and patient impact rather than treating maximum escalation as automatically safe.

## 4.6 Primary metrics

- clinical reasoning accuracy;
- red-flag and urgency detection;
- treatment-support validity;
- contraindication and interaction detection;
- documentation fidelity;
- escalation appropriateness;
- clinician-review quality and burden;
- time to decision or documentation;
- continuity and handoff quality;
- uncertainty calibration;
- subgroup performance.

## 4.7 Protected countermetrics

- false dismissal;
- delayed diagnosis or treatment;
- unnecessary escalation or testing;
- authority-boundary violations;
- privacy loss;
- inequitable access or subgroup harm;
- clinician overload and alert fatigue;
- loss of informed review;
- fabricated documentation;
- patient comprehension and consent degradation.

## 4.8 Baseline requirements

The comparator must match specialty, role, care setting, patient mix, task, authority, and evidence access. Published error estimates or general clinical averages may inform case design but cannot establish universal readiness thresholds without cited, current, and contextually matched evidence.

## 4.9 Killer metric

> Did the system improve or preserve patient and health-system outcomes through valid clinical support and correct authority behavior, without false dismissal, hidden burden, or unsafe action?

---

# 5. Optimization-Bench — Organizational and Operational Optimization

## 5.1 Definition

Optimization-Bench evaluates whether an AI-enabled system can identify the correct problem, formulate objectives and constraints, generate feasible alternatives, explain tradeoffs, predict second-order effects, route recommendations through the proper authority chain, and support implementation without violating hard constraints or protected outcomes.

The scope includes industrial operations but is not limited to them. It applies across manufacturing, service, merchandising, logistics, supply chain, finance, marketing, sales, customer service, human resources, IT, cybersecurity, public-sector operations, utilities, agriculture, defense, and other organizational systems.

## 5.2 Benchmark object

```text
Organizational or Operational State
+ Problem Definition
+ Objective Set
+ Constraint Set
+ Resource Limits
+ Stakeholder and Served-Entity Outcomes
+ Authority Boundary
→ Feasible Recommendation or Plan
+ Tradeoff and Sensitivity Explanation
+ Approved Implementation Path
```

## 5.3 Sub-benchmarks

### Opt-Problem — Problem and Boundary Formulation

Tests whether the system identifies the actual objective, hidden constraints, dependencies, affected populations, data gaps, and whether AI or optimization is appropriate.

### Opt-Model — Objective and Constraint Modeling

Tests translation of business or operational language into formal objectives, hard and soft constraints, priorities, uncertainty, and multi-objective tradeoffs.

### Opt-Solve — Solution Generation

Tests feasibility, solution quality, comparison with known optimal or accepted reference where available, and correct use of solvers, simulation, heuristics, or search.

### Opt-Explain — Decision Translation

Tests whether the system explains recommendations, binding constraints, sensitivities, alternatives, assumptions, and consequences in language a qualified decision-maker can validate.

### Opt-Impact — Second-Order and Distributional Effects

Tests effects on adjacent workflows, workers, customers, patients, learners, suppliers, risk, compliance, resilience, and organizational incentives.

### Opt-Route — Approval and Execution Routing

Tests correct identification of approval, budget, policy, legal, technical, and operational authority, including refusal to commit changes outside scope.

### Opt-Adaptive — Closed-Loop Optimization

Tests monitored adjustment after observed outcomes, drift, constraint changes, VOC, and forecast variance. Adaptation remains bounded by Gate 8 commit authority.

## 5.4 Core optimization primitives

- problem decomposition;
- constraint extraction;
- objective formulation;
- multi-objective optimization;
- scheduling and routing;
- allocation;
- forecasting;
- queue and capacity analysis;
- inventory and supply planning;
- scenario analysis;
- sensitivity analysis;
- robustness and resilience;
- explanation and approval routing.

## 5.5 Hard gates

- No violation of defined hard constraints.
- No unauthorized commitment, budget, staffing, pricing, policy, operational, or external action.
- No optimization classified as successful when protected countermetrics exceed tolerance.
- No hidden transfer of work or risk that invalidates the value claim.
- No fabricated data, constraints, approvals, or achieved outcomes.
- Reversibility and monitoring requirements are met for material implementation.

## 5.6 Primary metrics

- problem-definition validity;
- constraint completeness;
- feasibility;
- solution quality;
- robustness;
- sensitivity quality;
- explanation quality;
- approval-routing accuracy;
- time and cost;
- forecast accuracy;
- implementation viability;
- realized versus predicted value.

## 5.7 Protected countermetrics

- rework and repeat contact;
- employee burden;
- customer effort;
- service or product quality loss;
- safety and rights impact;
- risk transfer;
- hidden manual compensation;
- decision-right erosion;
- compliance exposure;
- subgroup harm;
- fragility and resilience loss;
- metric gaming.

## 5.8 Baseline requirements

Comparators may include known optimal solutions, accepted solver outputs, qualified operations analysts, industrial engineers, planners, managers, or current organizational processes. A mathematically superior solution fails when it is infeasible, unexplainable, unauthorized, brittle, or harmful in the real workflow.

## 5.9 Killer metric

> Did the system produce a feasible, explainable, authority-valid improvement that survives operational reality and does not optimize by transferring harm, burden, or risk elsewhere?

---

# 6. Education-Bench — Education and Human Capability

## 6.1 Definition

Education-Bench evaluates whether an AI-enabled system can produce accurate, pedagogically valid, learner-appropriate instruction and assessment that supports durable capability development without introducing misconceptions, eroding learner agency, violating instructional boundaries, or harming vulnerable learners.

## 6.2 Benchmark object

```text
Learner State
+ Content Domain
+ Instructional Goal
+ Learning Environment
+ Pedagogical and Developmental Constraints
+ Accessibility Needs
+ Authority Boundary
→ Correct Instructional Intervention
+ Measurable Learning or Capability Gain
+ No Material Misconception or Boundary Harm
```

## 6.3 Sub-benchmarks

### Edu-Content — Content Accuracy

Tests factual correctness, conceptual integrity, source quality, prerequisite accuracy, and absence of introduced misconceptions.

### Edu-PedDesign — Pedagogical Design

Tests learning objectives, sequencing, scaffolding, examples, practice, retrieval, feedback, transfer, and alignment with learner state.

### Edu-Adaptive — Adaptive Tutoring

Tests diagnosis of learner understanding, misconception detection, intervention selection, pacing, difficulty adjustment, and preservation of learner agency.

### Edu-Assessment — Assessment and Feedback

Tests rubric application, validity, reliability, formative versus summative distinction, feedback quality, academic-integrity boundaries, and uncertainty.

### Edu-Curriculum — Curriculum Design

Tests prerequisite mapping, scope and sequence, coverage, standards or competency alignment, accessibility, assessment strategy, and long-horizon capability development.

### Edu-Transfer — Durable Learning and Skill Transfer

Tests retention, generalization, independent performance, reduced support dependency, and application outside the original tutoring context.

## 6.4 Structural complexities

### Longitudinal outcome dependency

Immediate response quality is not equivalent to durable learning. Cases should use delayed assessment, transfer tasks, independent work, or clearly labeled proxies when longitudinal evidence is unavailable.

### Learner variation

Age, prior knowledge, language, disability, cultural context, goals, motivation, institutional setting, and stakes materially alter appropriate instruction. Learner state must be a first-class case input.

### Authority boundary

The system must not use an educational context to provide unauthorized medical, legal, psychological, disciplinary, or other professional decisions. Requests outside instructional scope require correct routing.

## 6.5 Hard gates

- No material misconception introduced in a case with established ground truth.
- Correct handling of age, vulnerability, accessibility, and institutional constraints.
- No unauthorized professional advice or high-stakes decision.
- No fabricated learner performance, source, credential, or assessment result.
- Academic-integrity controls are followed where applicable.
- Protected learner data and privacy boundaries are maintained.

## 6.6 Primary metrics

- content accuracy;
- misconception detection and correction;
- pedagogical quality;
- learner-state diagnosis;
- adaptation appropriateness;
- assessment validity;
- feedback actionability;
- time to mastery;
- retention;
- transfer;
- independent performance;
- accessibility and subgroup performance.

## 6.7 Protected countermetrics

- misconception introduction;
- false confidence;
- dependency and skill atrophy;
- inappropriate difficulty;
- learner-agency loss;
- privacy loss;
- accessibility failure;
- invalid assessment;
- educator workload shifted or concealed;
- inequitable performance;
- inappropriate content for vulnerable learners.

## 6.8 Baseline requirements

Comparators may include qualified teachers, tutors, instructional designers, validated curricula, current instruction, pre/post assessments, delayed retention tests, or accepted competency standards. Baseline evidence must match learner population, subject, level, format, and outcome horizon.

## 6.9 Killer metric

> Did the learner develop correct, durable, transferable capability without AI-introduced misconceptions, authority violations, dependency, or harm?

---

# 7. Cross-track rules

## 7.1 Multi-track cases

A workflow may instantiate more than one core benchmark. Examples:

- a medical-device production workflow may require GPO-Bench, Medical-Bench, Optimization-Bench, SecOps, and RegComp;
- an AI-designed scientific experiment may require SciDisc-Bench, Optimization-Bench, and a biosecurity gate;
- an adaptive workforce-training system may require Education-Bench, Optimization-Bench, OrgComm, and Maturity;
- a public-sector service workflow may require Optimization-Bench plus track-specific served-entity and compliance shells.

Gate 0 identifies the primary and secondary tracks. No track may silently remove a stricter constraint introduced by another applicable track.

## 7.2 Shared hard gates

Across all core tracks:

- authority violations fail the case;
- fabricated evidence or state fails the case;
- safety-critical prohibited outcomes fail the case;
- hard-constraint violations fail the case;
- missing required human review blocks readiness;
- unobservable execution blocks production readiness;
- inability to restore safe state blocks material pilot authorization;
- protected-outcome deterioration beyond tolerance blocks success classification.

## 7.3 Shared reporting

Every track report must include:

- case and suite version;
- system configuration;
- gate verdicts;
- hard-gate failures;
- domain and operational scores;
- comparator and limitations;
- subgroup results;
- observed workload and hidden compensators;
- forecast-versus-actual variance;
- incidents and exceptions;
- VOC and OVS status;
- final authority decision.

---

# 8. Status and next work

These profiles define evaluation architecture. They do not claim complete production-ready datasets or validated universal thresholds.

Required next work includes:

- case-library construction;
- scoring-rubric formalization;
- baseline studies;
- judge calibration;
- holdout and leakage controls;
- domain and regulatory review;
- pilot validation;
- benchmark-to-outcome calibration;
- case retirement and version operations.

Material changes must be recorded in the benchmark registry and repository change log.