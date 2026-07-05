# Gate 0 Standing Payload Template

Use this template as the final output of Gate 0 before entering Gate 1.

---

## Gate 0 Decision

```yaml
gate_0_decision:
  decision: pass_to_gate_1 | pass_with_declared_unknowns | request_context | escalate | block | quarantine
  reason: ""
  next_gate: gate_1_target_work_definition
```

---

## 0.0 Universal Orientation

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

---

## 0.1 Implementation Track Orientation

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

## 0.2 Industry Classification Orientation

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

## 0.3 Compliance Shell

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

---

## 0.4 Final Industry Orientation

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

---

## 0.5 Business Type / Value Flow

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

## 0.6 Locus / Boundary Topology

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

## 0.7 Completion Horizon

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

## 0.8 Work Bridge

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
