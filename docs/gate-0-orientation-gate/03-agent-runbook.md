# Gate 0 Agent Runbook

This runbook tells an AI agent how to execute Gate 0 before entering Gate 1.

---

## Prime Directive

Do not start the work until Gate 0 has oriented the system enough to define the correct work object.

If orientation is incomplete, the agent may proceed only when the missing information is non-blocking and explicitly carried forward as a declared unknown.

---

## Operating Sequence

### 1. Build the Universal Orientation Packet

Capture:

- request summary
- user intent
- desired output
- known context
- unknown context
- initial risk
- initial locus

Output:

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

### 2. Select the Implementation Track

Choose the primary track:

```text
optimization
production_manufacturing
scientific_discovery
medical_healthcare
education_human_capability
multi_track
unknown
```

If more than one track applies, select the highest-risk primary track and carry the others as secondary tracks.

Examples:

- Medical scheduling workflow optimization → primary `medical_healthcare`, secondary `optimization`
- Factory quality improvement → primary `production_manufacturing`, secondary `optimization`
- Clinical trial protocol design → primary `scientific_discovery`, secondary `medical_healthcare`

---

### 3. Apply the Gate Depth Registry

Use the selected implementation track to set default depth.

- `single`: one main orientation pass may be enough.
- `conditional`: check escalation triggers.
- `multiple`: load required orientation islands by default.

Escalate if the task touches:

- safety
- health
- money movement
- protected data
- human worker data
- live systems
- legal/compliance exposure
- professional duty
- minors/vulnerable subjects
- irreversible external effects

---

### 4. Classify Industry

Determine whether the domain is:

```text
US_NAICS
international_ISIC
region_specific
multi_region
unknown
```

Remember:

> Industry classification gives the field of vision. It is not the compliance engine.

For US context, use NAICS-oriented industry orientation. For international context, use ISIC or region-specific classification where appropriate.

---

### 5. Load Jurisdiction and Compliance Shell

Ask:

- What jurisdiction governs this work?
- Is the work US, international, multi-region, or unknown?
- What regulated activities are present?
- What protected data classes are present?
- What professional duties or licensed roles exist?
- What safety, privacy, financial, educational, medical, or employment risks exist?

Compliance is triggered by:

```text
jurisdiction
industry group
implementation track
data classes
entity type
regulated activities
professional roles
customer/patient/student/employee impact
external systems
safety exposure
money movement
```

---

### 6. Reconcile Final Industry Orientation

Create the final industry operating shell:

```text
Implementation Track
+ Industry Classification
+ Jurisdiction
+ Compliance Shell
+ Risk Escalators
```

Carry forward:

- loaded compliance shells
- forbidden actions
- human review requirements
- audit requirements
- risk escalators
- required orientation islands

---

### 7. Orient Business Type / Value Flow

Choose:

```text
manufacturing
merchandising
service
hybrid
unknown
```

Map value-flow mechanics:

- Manufacturing: inputs → production → quality → finished goods
- Merchandising: buy inventory → price/display/sell → fulfill/return
- Service: capability → customer interaction → delivered outcome
- Hybrid: multiple value-flow models operating together

Carry forward operational objects and quality model.

---

### 8. Resolve Locus and Boundary Topology

Classify boundary level:

```text
L0 = internal cognitive / answer-only
L1 = internal controlled system
L2 = external side effect through controlled connector
L3 = external dependency / waiting-state workflow
L4 = federated / multi-system workflow
```

Ask:

- Is the AI only answering?
- Is the AI accessing a user-authorized system?
- Is the AI creating an external side effect?
- Does final completion depend on an outside actor or system?
- Are multiple systems, agents, institutions, or connectors involved?

---

### 9. Determine Completion Horizon

Separate action completion from outcome completion.

The agent may truthfully say:

```text
I sent the email.
I created the draft.
I searched the records.
I submitted the form.
```

The agent may not truthfully say:

```text
They approved it.
They read it.
The doctor confirmed it.
The agency accepted it.
```

unless that external outcome has been received and verified.

Set final state:

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

---

### 10. Emit the Work Bridge

The Work Bridge is the final Gate 0 output. It must include:

- target work object
- work object type
- governing context
- allowed actions
- forbidden actions
- required reviews
- assumptions
- declared unknowns
- open dependencies
- gate decision

---

## Default Decision Policy

### Pass to Gate 1

Use when orientation is sufficient and constraints are known.

### Pass with Declared Unknowns

Use when unknowns are low-risk and non-blocking.

### Request Context

Use when missing context materially changes meaning, risk, authority, compliance, or completion.

### Escalate

Use when professional, legal, safety, medical, financial, HR, or authority review is needed.

### Block

Use when requested work is forbidden, unsafe, unauthorized, or policy-prohibited.

### Quarantine

Use when source, provenance, or instruction context is contaminated.

---

## High-Risk Shortcut Rule

If the task involves any of the following, do not use a lightweight Gate 0:

- medical diagnosis/treatment action
- physical-world machinery/process change
- financial transaction or advice affecting user funds
- legal advice/action or compliance filing
- HR/employment consequence
- minor or vulnerable learner/person
- protected data handling
- external irreversible effect
- live-system write action

Spawn the required local orientation islands.

---

## Agent Output Pattern

When Gate 0 completes, the agent should be able to produce this summary:

```text
Gate 0 Decision: pass_to_gate_1 | pass_with_declared_unknowns | request_context | escalate | block | quarantine
Implementation Track: ...
Industry / Jurisdiction: ...
Compliance Shell: ...
Business Type: ...
Boundary Level: ...
Completion Horizon: ...
Allowed Actions: ...
Forbidden Actions: ...
Open Dependencies: ...
Next Gate: Gate 1 Target Work Definition
```
