# Gate 0 / Orientation Gate Canonical Spec

**Version:** v0.1  
**Mode:** Markdown-first / AI-first  
**Scope:** Organization orientation before governed work definition

---

## 1. Core Doctrine

Gate 0 is the first step before any work.

It is not intake.  
It is not task execution.  
It is not Gate 1 workflow mapping.

Gate 0 is the orientation architecture that determines what world the AI is in before it is allowed to define or perform work.

Gate 0 answers:

> What is being requested, which implementation path governs it, what industry world applies, what jurisdiction/compliance shell is active, what business type/value-flow applies, where the AI stands relative to the user and external systems, and how far the work can truthfully be completed?

---

## 2. Full Formula

```text
Gate 0 =
Universal Orientation
+ Implementation Track
+ Industry Classification
+ Jurisdiction / Compliance Shell
+ Final Industry Orientation
+ Business Type / Value Flow
+ Locus / Boundary Topology
+ Completion Horizon
+ Work Bridge to Gate 1
```

---

## 3. Gate 0 Purpose

Gate 0 exists to prevent premature work.

It transforms an ambiguous request into a bounded, governed, oriented work-object candidate.

It moves the system from:

```text
unknown request
```

to:

```text
Gate 1-ready work object
```

The system may not enter Gate 1 until the required orientation layers are resolved or explicitly carried forward as declared unknowns.

---

## 4. Gate 0 Is a Chained Orientation System

Gate 0 is not one flat checkpoint. It is a chained orientation bridge made of orientation passes.

Each pass refines the standing payload.

```text
G0 Universal
-> G0 Implementation Track
-> G0 Industry Classification
-> G0 Jurisdiction / Compliance
-> G0 Final Industry Orientation
-> G0 Business Type
-> G0 Locus / Boundary / Completion
-> G0 Work Bridge
-> Gate 1
```

Each pass may add:

- constraints
- required orientation islands
- legal/compliance shells
- authority boundaries
- risk escalators
- data handling rules
- external dependencies
- completion limits

No lower layer may remove a constraint created by a higher-risk upper layer.

---

## 5. Gate 0.0 — Universal Orientation

### Purpose

Determine the basic request frame.

### Core Questions

- What is being asked?
- Who is asking?
- What output is expected?
- What is known?
- What is unknown?
- Is this informational, operational, external, high-risk, or ambiguous?

### Output

```yaml
g0_universal_orientation:
  request_summary: ""
  actor: ""
  user_intent: ""
  desired_output: ""
  known_context: []
  unknown_context: []
  initial_risk: low | medium | high | unknown
  initial_locus: internal | external | mixed | unknown
```

Universal Gate 0 does not yet decide the full workflow. It creates the first orientation packet.

---

## 6. Gate 0.1 — Implementation Track Orientation

### Purpose

Select the implementation path.

The implementation path is the first major umbrella because it determines the default depth of orientation.

### Five Implementation Tracks

```text
T1 — AI Core / Optimization
T2 — Production / Manufacturing
T3 — Scientific Discovery
T4 — Medical / Healthcare
T5 — Education / Human Capability
```

### Core Question

> Which implementation path governs the work?

### Output

```yaml
implementation_track_orientation:
  selected_track: optimization | production_manufacturing | scientific_discovery | medical_healthcare | education_human_capability | multi_track | unknown
  primary_track: ""
  secondary_tracks: []
  default_gate_0_depth: single | conditional | multiple
  required_orientation_islands: []
  escalation_triggers: []
```

---

## 7. Gate 0.2 — Gate Depth Decision

Each implementation track has a default Gate 0 depth.

The implementation path does not finish orientation. It decides how deep orientation must become before the system can move forward.

### Track Defaults

| Track | Default Gate 0 Depth | Rule |
|---|---|---|
| AI Core / Optimization | Single by default | Multi when measurement affects people, authority, live systems, money, compliance, or external commitments |
| Production / Manufacturing | Multiple by default | Physical processes create safety, quality, machine, worker, and material-flow concerns |
| Scientific Discovery | Conditional | Single for explanation; multiple for experiment, evidence, method, ethics, safety, or claim generation |
| Medical / Healthcare | Multiple by default | Patient-subject, user relation, care authority, clinical risk, privacy, and action tier must be resolved |
| Education / Human Capability | Conditional | Single for adult self-learning; multiple when learner, institution, minor, grading, assessment, or accommodation stakes appear |

---

## 8. Gate 0.3 — Industry Classification Branch

### Purpose

Identify the operating industry world.

This is not yet compliance. This is industry orientation.

### Core Question

> What industry classification system should orient the organization?

### Primary Branches

```text
United States / North America -> NAICS-oriented classification
International -> ISIC-oriented or region-specific classification
Multi-region -> multiple classification/compliance shells
Unknown -> mark unknown and escalate if risk requires
```

### Critical Rule

Industry classification is not the compliance engine.

```text
Industry classification = field of vision
Compliance shell = legal / regulatory / activity / data / authority controls
```

### Output

```yaml
industry_classification_orientation:
  classification_branch: US_NAICS | international_ISIC | region_specific | multi_region | unknown
  industry_group: ""
  sector: ""
  subsector_or_division: ""
  industry_group_detail: ""
  classification_confidence: low | medium | high
  likely_regulators_or_standards: []
  likely_data_classes: []
  likely_risk_domains: []
```

---

## 9. Gate 0.4 — Jurisdiction / Compliance Branch

### Purpose

Determine the legal and compliance shell.

This is where the industry classification branches into jurisdiction.

### Branch Logic

```text
If US:
    Load US federal / state / local / agency compliance frame.
    Check whether state, regulator, or special entity status matters.

If International:
    Identify region/country.
    Load regional legal/compliance shell.
    Check cross-border data, trade, privacy, professional, safety, or sector obligations.

If Multi-region:
    Load multiple compliance shells.
    Reconcile conflicts.
    Use the stricter shell where needed.

If Unknown:
    Mark jurisdiction unknown.
    Allow only low-risk general work or request more context.
```

### Compliance Inputs

- jurisdiction
- industry group
- implementation track
- data classes
- entity type
- regulated activities
- professional roles
- customer/patient/student/employee impact
- external systems
- safety exposure
- money movement

### Output

```yaml
compliance_shell:
  jurisdiction:
    country_or_region: ""
    state_or_local: ""
    multi_region: true | false

  legal_regulatory:
    statutes: []
    regulations: []
    regulators: []
    reporting_obligations: []

  privacy_data:
    personal_data: true | false
    sensitive_data: true | false
    health_data: true | false
    financial_data: true | false
    student_data: true | false
    classified_or_export_controlled_data: true | false
    retention_or_deletion_rules: []

  authority_professional_duty:
    licensed_professional_required: true | false
    human_review_required: true | false
    fiduciary_duty_possible: true | false
    standard_of_care_possible: true | false
    institutional_approval_required: true | false

  safety_liability:
    physical_harm_possible: true | false
    clinical_harm_possible: true | false
    product_defect_possible: true | false
    workplace_safety_possible: true | false
    public_safety_possible: true | false
    environmental_harm_possible: true | false

  audit_provenance:
    source_traceability_required: true | false
    decision_log_required: true | false
    approval_record_required: true | false
    rollback_path_required: true | false

  forbidden_actions: []
  required_controls: []
  escalation_conditions: []
```

### Rule

> Compliance modifies industry grouping through jurisdiction, then feeds back into final industry orientation.

---

## 10. Gate 0.5 — Final Industry Orientation

### Purpose

Reconcile implementation track, industry grouping, jurisdiction, and compliance.

This produces the final industry operating shell.

### Formula

```text
Final Industry Orientation =
Implementation Track
+ Industry Classification
+ Jurisdiction
+ Compliance Shell
+ Risk Escalators
```

### Output

```yaml
final_industry_orientation:
  implementation_track: ""
  industry_group: ""
  jurisdiction_shell: ""
  compliance_shells_loaded: []
  industry_operating_shell: ""
  risk_escalators: []
  required_orientation_islands_for_next_layer: []
  forbidden_actions: []
  human_review_requirements: []
  audit_requirements: []
```

### Rule

> Industry compliance is the hard shell. Business type is the value-flow shell.

---

## 11. Gate 0.6 — Business Type / Value-Flow Orientation

### Purpose

Determine how the organization creates and delivers value.

Business type is not primarily the legal layer. It is the operational value-flow layer.

### Business Types

```text
Manufacturing
Merchandising
Service
Hybrid
```

### Manufacturing

Core value flow:

```text
Inputs -> production process -> quality control -> finished goods
```

Core objects:

- raw materials
- machines
- workers
- process steps
- batches
- defects
- finished goods
- quality standards
- downtime
- warranty / recall

Gate additions:

- safety check
- quality check
- traceability check
- machine/tool boundary
- defect/rework risk
- downtime risk
- recall/warranty risk

### Merchandising

Core value flow:

```text
Buy inventory -> price/display/sell -> fulfill/return
```

Core objects:

- supplier
- inventory
- SKU
- price
- margin
- customer order
- return
- refund
- chargeback
- forecast

Gate additions:

- inventory accuracy
- pricing authority
- supplier dependency
- customer claims
- fraud/chargeback risk
- return/refund policy
- margin impact

### Service

Core value flow:

```text
Human/system capability -> customer interaction -> delivered outcome
```

Core objects:

- client/customer/patient/student
- service request
- case/ticket
- appointment
- provider
- SLA
- deliverable
- outcome
- communication

Gate additions:

- service quality
- professional authority
- customer expectation
- case lifecycle
- communication boundary
- outcome verification
- SLA/reliability

### Hybrid

Core value flow:

```text
Multiple value-flow models operating together.
```

Example:

```text
A hospital is primarily service, but may include merchandising-like pharmacy operations and manufacturing-like lab/process workflows.
```

Gate additions:

- split value-flow map
- primary business type
- secondary business types
- cross-flow dependencies
- conflict resolution

### Output

```yaml
business_type_orientation:
  business_type: manufacturing | merchandising | service | hybrid | unknown
  primary_value_flow: ""
  secondary_value_flows: []
  operational_objects: []
  customer_touchpoints: []
  fulfillment_model: ""
  quality_model: ""
  business_type_risks: []
  additional_orientation_islands: []
```

---

## 12. Gate 0.7 — Locus / Boundary Topology Orientation

### Purpose

Determine where the AI stands relative to the user, system, organization, external parties, tools, connectors, and agents.

### Core Question

> Is this work internal, connector-mediated, external-facing, dependent on outside response, or federated across systems?

### Boundary Levels

| Level | Name | Definition | Completion |
|---|---|---|---|
| L0 | Internal Cognitive / Answer-Only | AI completes work inside the conversation | Fully completable now |
| L1 | Internal Controlled System | AI acts inside a user-authorized system | Completable if connector access works |
| L2 | External Side Effect Through Controlled Connector | AI creates an external-facing action | Action can complete; outcome may remain pending |
| L3 | External Dependency / Waiting-State Workflow | Completion depends on external actor/system | Partial completion only; waiting_external required |
| L4 | Federated / Multi-System Workflow | AI coordinates across systems, agents, institutions, or connectors | Segmented completion |

### Output

```yaml
locus_boundary_orientation:
  boundary_level: L0_internal_cognitive | L1_internal_controlled_system | L2_external_side_effect | L3_external_dependency | L4_federated_multi_system
  user_to_ai_relation: ""
  ai_to_system_relation: ""
  ai_to_external_party_relation: ""
  connectors_or_agents: []
  third_parties: []
  external_dependencies: []
  authority_boundary: ""
  data_boundary: ""
  system_boundary: ""
```

---

## 13. Gate 0.8 — Completion Horizon Orientation

### Purpose

Determine how far the AI can truthfully carry the workflow.

This prevents false completion.

### Core Rule

> The AI may close an action it performed, but it may not close an outcome that depends on an external actor unless that actor’s response has been received and verified.

### Action Completion vs Outcome Completion

**Action completion:**

- I sent the email.
- I created the event.
- I searched the document.
- I drafted the message.
- I submitted the form.

**Outcome completion:**

- They replied.
- They approved it.
- The doctor confirmed it.
- The application was accepted.
- The vendor completed the repair.

### Workflow States

```text
complete
partial_complete
initiated
waiting_external
blocked_authority
blocked_missing_context
blocked_tool_access
blocked_policy
failed_execution
quarantined
```

### Output

```yaml
completion_horizon_orientation:
  requested_outcome: ""
  controllable_scope: []
  non_controllable_scope: []
  executable_actions:
    - action: ""
      controlled_by_ai: true | false
      requires_connector: true | false
      requires_user_approval: true | false
      can_verify_completion: true | false

  external_dependencies:
    - dependency: ""
      actor_or_system: ""
      required_response: ""
      ai_can_force_response: false
      ai_can_monitor_response: true | false
      expected_state: pending | received | failed | unknown

  completion_state_possible:
    full_completion_now: true | false
    partial_completion_only: true | false
    initiation_only: true | false
    waiting_state_required: true | false

  truthful_user_report:
    allowed_to_say: []
    not_allowed_to_say: []
```

---

## 14. Gate 0.9 — Work Bridge

### Purpose

Convert all Gate 0 orientation outputs into a Gate 1-ready work object.

Gate 0 does not do the work. It prepares the system to define the work.

### Work Bridge Questions

- What exact work object should enter Gate 1?
- What implementation track governs it?
- What industry/compliance/business type context must carry forward?
- What locus and boundary constraints apply?
- What can be completed now?
- What must remain open?
- What actions are allowed?
- What actions are forbidden?
- What assumptions are declared?
- What unknowns remain?

### Output

```yaml
gate_0_work_bridge:
  target_work_object: ""
  work_object_type: informational | analytical | operational | external_action | coordination | high_risk | unknown

  governing_context:
    implementation_track: ""
    industry_group: ""
    jurisdiction_shell: ""
    compliance_shells: []
    business_type: ""
    boundary_level: ""
    completion_horizon: ""

  allowed_actions: []
  forbidden_actions: []
  required_human_review: true | false
  required_clinician_or_professional_review: true | false
  required_audit: true | false

  assumptions: []
  declared_unknowns: []
  open_dependencies: []

  gate_decision:
    decision: pass_to_gate_1 | pass_with_declared_unknowns | request_context | escalate | block | quarantine
    reason: ""
    next_gate: gate_1_target_work_definition
```

---

## 15. Recursive Orientation Rule

Gate 0 must spawn a local orientation island when a newly discovered relation changes the work.

```text
If a discovered actor, subject, system, authority source, data source, physical process, institution, jurisdiction, or external dependency materially changes the meaning, risk, authority, compliance, or completion horizon of the work, spawn a local Gate 0 orientation island before proceeding.
```

Examples:

- New patient discovered -> spawn Medical Patient-Subject G0.
- Doctor/care team involved -> spawn Medical Authority G0.
- Machine/tool involved -> spawn Manufacturing Safety G0.
- Minor/student discovered -> spawn Education Learner-Protection G0.
- Human-subject dataset discovered -> spawn Scientific Ethics/Privacy G0.
- External connector discovered -> spawn Boundary/Completion G0.
- International region discovered -> spawn Jurisdiction/Compliance G0.

---

## 16. Precedence Rule

No lower layer may weaken a higher-risk constraint.

```text
Law / regulation
> safety
> human authority
> professional duty
> compliance shell
> industry operating shell
> implementation track
> business type
> workflow convenience
> optimization goal
> model recommendation
```

Invariants:

- Optimization cannot override safety.
- Business type cannot override compliance.
- Workflow convenience cannot override authority.
- Model output cannot override law.

---

## 17. Gate 0 Decision States

| Decision | Meaning |
|---|---|
| `pass_to_gate_1` | Orientation is sufficient and work can be defined |
| `pass_with_declared_unknowns` | Unknowns are non-blocking and carried forward |
| `request_context` | Missing context materially affects meaning, risk, authority, or compliance |
| `escalate` | Human, professional, legal, safety, or authority review is required |
| `block` | Requested work is forbidden or lacks authority |
| `quarantine` | Source, provenance, or instruction context is contaminated |

---

## 18. Final One-Line Doctrine

> Gate 0 tells the AI what world it is in, what rules bind that world, where the AI stands inside it, and how far the AI can responsibly carry the work before Gate 1 begins.
