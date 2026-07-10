# Benchmark VOC and Outcome Validation

**Version:** 1.1  
**Parent:** [Aetheris Governed AI Benchmark Architecture v1.1](./00-governed-ai-benchmark-architecture-v1.1.md)  
**Source lineage:** Aetheris VOC Architecture v0.2.1 Corrected  
**Status:** Canonical working calibration specification

---

## 1. Definition

Benchmark VOC is the external reality-calibration layer for the Aetheris benchmark suite.

VOC means **governed served-entity signal intelligence**. It captures the experiences and outcomes of the humans or organizations ultimately affected by an AI-enabled workflow and compares those outcomes with benchmark scores, telemetry, gate verdicts, forecasts, and internal KPIs.

Benchmark VOC exists because a benchmark suite can become a closed optimization target. A system may learn to score well while operators, patients, learners, customers, workers, citizens, researchers, or downstream organizations experience deterioration.

The governing rule is:

> A benchmark score is provisional until it demonstrates alignment with protected real-world outcomes.

VOC is not equivalent to a satisfaction survey. It may include structured outcome evidence, complaints, appeals, repeat work, downstream burden, operator observations, safety events, learning retention, patient comprehension, customer effort, incident patterns, agent-to-agent friction, and other purpose-limited signals.

---

## 2. Served-entity abstraction

The served entity is the person or organization whose outcome is the ultimate measure of whether the workflow succeeded.

Examples:

| Track or domain | Operator | Served entity |
|---|---|---|
| Production | quality engineer, line operator, planner | worker, customer, downstream manufacturer, regulated party |
| Scientific discovery | researcher, methodologist | research community, affected population, scientific sponsor |
| Medical | clinician, administrator | patient and care population |
| Organizational optimization | employee, manager, analyst | customer, worker, partner, citizen, organization receiving the service |
| Education | educator, tutor, administrator | learner |
| Agent-mediated workflow | internal or external AI agent | human or organization represented by the agent |

A workflow may have multiple served-entity populations. The VOC plan must identify whose outcomes are protected and who is authorized to interpret or act on the signal.

---

## 3. Benchmark VOC architecture position

```text
Five-Track Core Benchmarks
(GPO | SciDisc | Medical | Optimization | Education)

Cross-Cutting Benchmarks
(TSC | SecOps | RevT | RegComp | OrgComm | WTT)

Relational Benchmarks
(IPeer | FedComp | Maturity)

Meta-Benchmark
(CCIB)
        ↑ ↓
Benchmark VOC Feedback Layer
        ↑ ↓
Versioned benchmark specification
        ↑
Case libraries, evidence base, and Gate 8 learning
```

Benchmark VOC does not directly rewrite benchmark authority, thresholds, or organizational state. It produces calibration evidence and change candidates that must pass review, reconciliation, and Gate 8 commit.

---

## 4. Collection instruments

### 4.1 Intake VOC

**Timing:** before deployment or pilot.  
**Question:** What are we building, for whom, against what baseline, and what must not be sacrificed?

Intake VOC identifies:

- served populations;
- current workflow experience;
- desired outcomes;
- protected countermetrics;
- hidden compensators and workarounds;
- jurisdiction and privacy constraints;
- baseline defects;
- organizational dependencies;
- trust and usability conditions;
- known historical failures.

Intake VOC informs Gate 0, the Organization Knowledge Core, Golden WFKB, baseline design, and benchmark-case selection.

### 4.2 Per-Mile VOC

**Timing:** during runtime at meaningful workflow points.  
**Question:** Is the workflow operating as designed, and what does telemetry fail to explain?

Per-Mile VOC correlates:

- system observer evidence;
- human operator observation;
- state transitions;
- timing;
- authority events;
- friction and confusion;
- unsafe shortcuts;
- exception patterns;
- unexpected manual work.

Disagreement between system evidence and human observation is treated as high-value signal rather than automatically resolved in favor of either observer.

### 4.3 Post-Handshake VOC

**Timing:** after an optimization or implementation has operated long enough to produce meaningful experience. The cadence is deployment-specific; the earlier source proposed 30–60 days as an example, not a universal rule.  
**Question:** Did the implementation produce the forecasted outcome, and what second-order effects appeared?

Post-Handshake VOC evaluates:

- forecast recognizability;
- actual workflow improvement or degradation;
- adjacent-workflow effects;
- human workload;
- trust and usability;
- outcome distribution;
- hidden costs;
- whether the Candidate Twin represented the real organization.

### 4.4 AI2AI VOC

Agent-mediated workflows require structured observation of interactions between customer agents, company agents, internal workflow agents, tools, and human review gates.

AI2AI VOC may identify:

- goal mismatch;
- consent ambiguity;
- authority mismatch;
- incompatible representations;
- repeated negotiation or routing failure;
- identity and provenance defects;
- escalation failure;
- agent claims that conflict with observed state.

The interaction is evidence, not authority. Agent-generated VOC cannot directly commit benchmark or workflow changes.

---

## 5. Stakeholder populations

Benchmark VOC should select populations relevant to the deployment rather than collecting unrestricted feedback.

Typical populations include:

1. **Frontline operators** — workflow friction, workarounds, exception handling, hidden cleanup, safety concerns.
2. **Served entities** — direct outcome, access, comprehension, effort, quality, harm, and trust.
3. **Department managers or domain leads** — team performance, dependency effects, resource use, and operational viability.
4. **Executives, security, compliance, and governance owners** — mission value, risk, regulatory posture, and strategic effects.
5. **Adjacent stakeholders** — suppliers, partners, regulators, downstream teams, communities, or other affected systems.

The population list is not a fixed survey template. It is a governed sampling plan tied to the workflow’s purpose and risk.

---

## 6. VOC benchmark object

Each collection cycle produces a structured packet.

```text
Stakeholder Population
+ Collection Timeframe
+ Deployment and Workflow Version
+ Benchmark Score Context
+ Gate Verdict Context
+ Forecast Context
+ Real Outcome Experience
+ Protected Countermetric Evidence
+ Gap Identification
→ Calibration Signal
+ New Case Candidates
+ Authority Recommendation
+ Outcome Validation Score when statistically supportable
```

Required fields include:

- deployment, workflow, model, and benchmark versions;
- stakeholder population and sampling method;
- collection timeframe;
- benchmark and gate results;
- observed operational outcomes;
- protected countermetrics;
- incidents and exceptions;
- qualitative observations with provenance;
- identified gap type;
- recommended benchmark or workflow response;
- confidence and limitations;
- privacy and retention classification;
- review owner;
- authority action: continue, recalibrate, narrow, suspend, roll back, or investigate.

---

## 7. Gap taxonomy

### Calibration gap

The benchmark measures the relevant dimension but the weight, threshold, scoring rule, or tolerance is wrong.

**Typical response:** recalibrate thresholds or scoring after validation.

### Coverage gap

A material outcome, population, workflow state, or failure dimension is absent from the benchmark.

**Typical response:** add a dimension, sub-benchmark, or track shell through formal review.

### Case-library gap

The benchmark dimension exists, but the case library lacks a realistic scenario or distribution.

**Typical response:** add development and holdout cases with provenance and leakage controls.

### Authority-boundary gap

The benchmark’s assumed authority structure does not match the real organization, jurisdiction, profession, or workflow.

**Typical response:** reorient through Gate 0 and revise authority cases and thresholds.

### Human-baseline gap

The comparator does not represent actual qualified performance, current workflow conditions, affected populations, or task distribution.

**Typical response:** collect or source a better comparator and recalculate readiness claims.

### Unknown gap

A score-outcome mismatch cannot be explained by the current suite.

**Typical response:** escalate to the research and governance queue; preserve evidence; narrow claims or authority until resolved.

---

## 8. Killer metric

> Is the gap between benchmark score and operator- or served-entity-reported outcome experience narrowing over successive deployment cycles?

This metric asks whether the benchmark is becoming more reality-aligned as the system learns.

A narrowing gap supports calibration. A widening gap may indicate benchmark gaming, missing cases, hidden manual compensation, measurement error, population shift, delayed harm, or a structurally invalid benchmark.

---

## 9. Outcome Validation Score

### 9.1 Provisional definition

The Outcome Validation Score (OVS) is a diagnostic correlation between normalized benchmark movement and normalized movement in protected served-entity outcomes across deployment cycles.

```text
OVS = corr(
  ΔBenchmarkScore_normalized,
  ΔServedEntityOutcome_normalized
)
```

Interpretation:

- **+1.0:** benchmark improvement strongly aligns with protected outcome improvement.
- **0.0:** no stable relationship is detected.
- **−1.0:** benchmark improvement aligns with outcome deterioration.

### 9.2 Limits

OVS does not prove causation. A valid report must address:

- number of deployment cycles;
- sample size and response coverage;
- population stability;
- missing data;
- confidence interval;
- delayed effects and lag structure;
- concurrent workflow or policy changes;
- model, data, prompt, tool, or reviewer changes;
- aggregation across stakeholder populations;
- normalization method;
- subgroup differences;
- whether countermetrics are directionally consistent;
- known confounders.

Until formal statistical rules are frozen, OVS must be labeled provisional and accompanied by its inputs and limitations.

### 9.3 Diagnostic states

| State | Pattern | Interpretation | Required response |
|---|---|---|---|
| Properly governed deployment | Scores and protected outcomes improve together | Suite is plausibly aligned | Maintain cadence and preserve evidence |
| Calibration problem | Scores improve; outcomes remain flat or poor | Suite may weight or measure the wrong thing | Identify gap type and recalibrate |
| Conservative benchmark | Outcomes improve faster than scores | Thresholds may be too conservative or lagging | Review without weakening hard gates |
| Divergent deployment | Scores and outcomes move in opposite directions | Benchmark gaming, hidden harm, or structural measurement error | Suspend benchmark-driven optimization and escalate |
| Inconclusive | Evidence is sparse, noisy, delayed, or unstable | No reliable calibration claim | Continue observation or narrow claims |

---

## 10. Hard gate and authority suspension

Benchmark-driven optimization authority is suspended when all of the following are present:

1. a safety-critical or otherwise protected outcome failure is occurring or credibly threatened;
2. the benchmark suite is not detecting the failure or is reporting acceptable performance;
3. the pattern is supported by repeated cycles, independent evidence, or a single sufficiently severe incident under the applicable governance rules;
4. the failure is plausibly attributable to the AI-enabled workflow or its implementation;
5. continued optimization would create unacceptable risk.

Suspension applies to benchmark-driven optimization authority. It does not automatically require shutdown of every workflow function. Direct imminent harm, security compromise, or other Andon conditions may trigger a separate containment or shutdown path.

Required sequence:

```text
Detect divergence
→ contain risk
→ preserve evidence
→ notify owners
→ narrow or suspend authority
→ classify the gap
→ revise cases, thresholds, workflow, or baseline
→ rerun evaluation
→ reconcile
→ reauthorize through the applicable gate
```

---

## 11. Protected-countermetric doctrine

No implementation may be classified as successful solely because an internal KPI improves.

Examples:

| Internal KPI improves | Protected countermetric deteriorates | Verdict |
|---|---|---|
| Production throughput | Defect complaint rate | Failed optimization pending investigation |
| Documentation speed | Patient comprehension or clinical quality | Failed optimization pending clinical review |
| Tutor engagement | Retention or independent performance | Failed optimization pending recalibration |
| Average handle time | Repeat contact or customer effort | Failed optimization pending workflow review |
| Hypothesis volume | False-lead cost or validation burden | Discovery calibration problem |
| Benchmark score | Operator or served-entity outcome | Benchmark calibration problem |

The precise verdict depends on severity, confidence, causality, and tolerance, but the KPI gain cannot erase the protected-outcome loss.

---

## 12. Privacy and purpose limitation

VOC collection must be:

- purpose-limited;
- proportionate to risk and decision need;
- transparent;
- role-appropriate;
- access-controlled;
- retention-bounded;
- protected against retaliation;
- separated from unauthorized employee surveillance;
- based on consent or another lawful authority where required;
- designed to minimize unnecessary personal data;
- reviewed for jurisdictional and labor implications;
- aggregated or anonymized where individual identification is not needed.

Worker reflection exists to improve workflows and calibrate benchmarks, not to create covert performance scoring. Individual responses should not be exposed to management when the approved design requires team-level aggregation or anonymity.

Cross-client or commons contribution is opt-in, rights-cleared, sanitized, and governed. Organization names, system names, identifiable role details, and sensitive absolute values must not be transferred without explicit authority.

---

## 13. Goodhart resistance for VOC

VOC can itself be gamed or distorted. Controls include:

- no in-loop reward or punishment for favorable feedback;
- no single population controls the verdict;
- system evidence and human observation remain separate;
- disagreement is preserved as signal;
- collection instruments are rotated and reviewed;
- nonresponse and selection bias are reported;
- leading questions and metric fixation are tested;
- management cannot rewrite operator evidence;
- qualitative data is not converted into false precision;
- severe incidents can override aggregate averages;
- VOC owners remain independent from teams rewarded for deployment success.

---

## 14. Gate integration

- **Gate 0:** identify served entities, lawful collection scope, protected countermetrics, and review ownership.
- **Gate 2:** verify baseline and VOC plan sufficiency.
- **Gate 4:** simulate score-outcome divergence and collection failure.
- **Gate 5:** authorize pilot collection and privacy controls.
- **Gate 6:** compare benchmark, telemetry, incidents, and VOC.
- **Gate 7:** reconcile gaps and recommend calibration or authority action.
- **Gate 8:** commit approved benchmark, workflow, baseline, or policy updates.

VOC evidence cannot bypass Gate 8 commit controls.

---

## 15. Minimum viable deployment

A first deployment does not require the entire mature VOC architecture. The minimum viable form should include:

1. identified served entity and operator populations;
2. at least one protected countermetric;
3. a lawful and purpose-limited collection method;
4. baseline or pre-pilot outcome evidence;
5. post-pilot collection;
6. benchmark and outcome comparison;
7. gap classification;
8. a named review and authority owner;
9. a halt, narrow, rollback, or recalibration path;
10. evidence retention and privacy controls.

OVS should not be calculated when cycles or sample quality are insufficient. The absence of OVS does not eliminate the requirement to inspect score-outcome alignment.

---

## 16. Open work

Before OVS becomes a formal statistical claim, the architecture must freeze:

- minimum cycle count;
- sample-size rules;
- confidence-interval method;
- lag treatment;
- missing-data rules;
- normalization rules;
- multi-population aggregation;
- subgroup reporting;
- severity weighting;
- causal-inference boundaries;
- cross-client consent and anonymization;
- benchmark authority-suspension thresholds.

---

## 17. Change note

### v1.1 — 2026-07-10

- Integrated Benchmark VOC into the repository benchmark architecture.
- Replaced references to Gate 0–9 with ACIM-E Gates 0–8.
- Preserved the six gap classes and OVS formula.
- Clarified that OVS is provisional and non-causal.
- Added severe-incident, privacy, worker-protection, Goodhart-resistance, and minimum-viable-deployment controls.
- Clarified that benchmark changes remain proposals until Gate 8 commit.