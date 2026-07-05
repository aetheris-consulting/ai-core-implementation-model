# Gate 0 Examples

This file shows how the Orientation Gate behaves across implementation tracks, industries, business types, and boundary conditions.

---

## Example 1 — Standalone Optimization Benchmark

### Request

```text
Compare how long a human worker takes to complete ticket triage versus an AI agent.
```

### Gate 0 Orientation

```yaml
implementation_track: optimization
default_depth: single
industry_group: IT service / customer support
business_type: service
boundary_level: L0_or_L1
completion_horizon: measurable_if_data_available
```

### Escalation Check

If anonymized process data is used:

```text
Proceed with single-plus-light privacy orientation.
```

If named employees are compared:

```text
Escalate to multi-Gate-0 because human worker data and HR consequence risk exist.
```

### Work Bridge

```yaml
target_work_object: ticket_triage_benchmark
allowed_actions:
  - define metrics
  - compare anonymized performance
  - identify workflow bottlenecks
forbidden_actions:
  - rank named employees without HR/legal authority
  - make employment recommendations from ungoverned benchmark data
```

---

## Example 2 — Medical Patient-Self Question

### Request

```text
My chest feels tight. What should I do?
```

### Gate 0 Orientation

```yaml
implementation_track: medical_healthcare
default_depth: multiple
required_islands:
  - patient_subject_orientation
  - user_relation_orientation
  - care_setting_orientation
  - risk_acuity_orientation
  - allowed_action_tier_orientation
business_type: service
boundary_level: L0
completion_horizon: education_and_safety_routing_only
```

### Gate 0 Decision

```yaml
decision: escalate
reason: potential acute symptom / emergency risk
allowed_actions:
  - provide safety-oriented triage guidance
  - identify red flags
  - recommend urgent/emergency care where appropriate
forbidden_actions:
  - definitive diagnosis
  - reassurance that delays care
  - treatment substitution for clinician evaluation
```

---

## Example 3 — Hospital AI Workflow

### Request

```text
Use AI to reduce discharge delays in a hospital.
```

### Gate 0 Orientation

```yaml
implementation_track: medical_healthcare
secondary_track: optimization
industry_group: healthcare
jurisdiction: US
compliance_shells:
  - health data privacy
  - institutional clinical governance
  - audit/provenance
business_type: service
boundary_level: L4_federated_multi_system
completion_horizon: segmented_completion
```

### Required Islands

```text
G0 Patient/Population Subject
G0 Care Team Authority
G0 PHI/Provenance
G0 Operational Workflow
G0 External Dependency
G0 Completion Horizon
```

### Work Bridge

```yaml
target_work_object: discharge_delay_workflow_analysis
allowed_actions:
  - map discharge workflow
  - identify bottlenecks
  - summarize non-diagnostic operational delays
  - recommend governance-reviewed interventions
forbidden_actions:
  - hidden prioritization of patient discharge
  - unauthorized PHI exposure
  - autonomous care-plan changes
```

---

## Example 4 — Manufacturing Process Optimization

### Request

```text
Optimize this assembly line process.
```

### Gate 0 Orientation

```yaml
implementation_track: production_manufacturing
secondary_track: optimization
default_depth: multiple
industry_group: manufacturing
business_type: manufacturing
boundary_level: depends_on_tooling
completion_horizon: depends_on_simulation_vs_live_control
```

### Required Islands

```text
G0 Physical Process
G0 Machine / Tooling
G0 Worker Safety
G0 Material / Product Quality
G0 Authority / Control Boundary
G0 Completion Horizon
```

### Work Bridge

```yaml
target_work_object: assembly_line_process_optimization
allowed_actions:
  - analyze process map
  - identify bottlenecks
  - recommend simulation-only improvements
  - flag safety/quality risks
forbidden_actions:
  - live machine control without explicit authority
  - bypass safety interlocks
  - alter quality specs without approval
```

---

## Example 5 — Scientific Discovery / Paper Explanation

### Request

```text
Explain this paper to me.
```

### Gate 0 Orientation

```yaml
implementation_track: scientific_discovery
default_depth: conditional
simple_case: true
industry_group: research / academic / domain-specific if known
business_type: service_or_unknown
boundary_level: L0
completion_horizon: fully_completable_now
```

### Gate 0 Decision

```yaml
decision: pass_to_gate_1
reason: explanation only, no experiment design or high-risk claim generation requested
```

---

## Example 6 — Scientific Discovery / Experiment Design

### Request

```text
Design an experiment to test this biological pathway.
```

### Gate 0 Orientation

```yaml
implementation_track: scientific_discovery
default_depth: multiple
industry_group: biotech / academic research / life sciences
jurisdiction: unknown
business_type: service_or_hybrid
boundary_level: L0_to_L3
completion_horizon: design_only_unless_external_lab_authorized
```

### Required Islands

```text
G0 Research Object
G0 Hypothesis / Claim
G0 Evidence / Method
G0 Model-vs-Reality Boundary
G0 Ethics / Safety
G0 Claim Strength
```

### Work Bridge

```yaml
target_work_object: experiment_design_support
allowed_actions:
  - frame hypothesis
  - identify variables
  - propose safe, high-level method categories
  - flag ethics/safety/IRB needs
forbidden_actions:
  - unsafe procedural optimization
  - bypassing IRB or biosafety controls
  - overstating claim strength
```

---

## Example 7 — Education / Adult Self-Learning

### Request

```text
Teach me accounting for my WGU course.
```

### Gate 0 Orientation

```yaml
implementation_track: education_human_capability
default_depth: single
industry_group: education
business_type: service
boundary_level: L0
completion_horizon: fully_completable_now_for_instruction
```

### Work Bridge

```yaml
target_work_object: adult_self_learning_support
allowed_actions:
  - explain concepts
  - quiz the learner
  - build study plans
  - generate examples
forbidden_actions:
  - impersonate student
  - complete graded work dishonestly
```

---

## Example 8 — Education / Institutional Grading

### Request

```text
Grade these students and recommend who should pass.
```

### Gate 0 Orientation

```yaml
implementation_track: education_human_capability
default_depth: multiple
industry_group: education
jurisdiction: depends_on_institution
business_type: service
boundary_level: L1_or_L4
completion_horizon: recommendation_only_unless_authorized
```

### Required Islands

```text
G0 Learner-Subject
G0 User-Relation
G0 Teacher / Institution Authority
G0 Assessment Stakes
G0 Accommodation / Developmental Context
```

### Gate 0 Decision

```yaml
decision: escalate
reason: institutional assessment and learner consequences require authority and governance
```

---

## Example 9 — Email With External Dependency

### Request

```text
Email the landlord and let me know if they approved my application.
```

### Gate 0 Orientation

```yaml
implementation_track: optimization_or_service_coordination
industry_group: housing / property management
business_type: service
boundary_level: L3_external_dependency
completion_horizon: partial_completion_only
```

### Work Objects

```yaml
work_objects:
  W1_send_email:
    type: external_side_effect
    completion: possible_now
    proof: sent_message_record

  W2_get_reply:
    type: external_dependency
    actor: landlord
    completion: not_possible_now
    proof: future_received_reply
    state: waiting_external
```

### Truthful User Report

```text
I sent the email. The approval answer is still pending because it depends on the landlord replying.
```

---

## Example 10 — Finance Industry Escalates Optimization

### Request

```text
Optimize customer-support workflows for a financial services company.
```

### Gate 0 Orientation

```yaml
implementation_track: optimization
default_depth: single
industry_group: finance
jurisdiction: US
compliance_shells:
  - financial privacy
  - audit
  - fraud risk
  - identity verification
business_type: service
boundary_level: L1_to_L4
```

### Escalation

Although optimization is single by default, finance industry constraints escalate the orientation depth.

```yaml
decision: multi_gate_orientation_required
reason:
  - financial data possible
  - customer identity risk possible
  - audit/provenance required
  - regulated customer communications possible
```
