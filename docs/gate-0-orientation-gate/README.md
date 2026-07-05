# Gate 0 / Orientation Gate

**Status:** Draft v0.1  
**Architecture family:** AI Core Implementation Model  
**Primary role:** Organization orientation before work definition

Gate 0 is the first step before any AI-governed work. It is not intake, execution, or workflow mapping. It is the orientation architecture that determines what world the AI is in before the system is allowed to define or perform work.

## Core Doctrine

> Gate 0 tells the AI what world it is in, what rules bind that world, where the AI stands inside it, and how far the AI can responsibly carry the work before Gate 1 begins.

Compact formula:

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

## Why Gate 0 Exists

Gate 0 prevents premature execution.

Without Gate 0, an AI system can jump from:

```text
User asked something -> start working
```

to unsafe or poorly bounded work.

Gate 0 forces a governed transition:

```text
User asked something
-> orient to implementation path
-> orient to industry
-> orient to jurisdiction/compliance
-> orient to business type
-> orient to locus/boundary/completion
-> define the correct work object
-> enter Gate 1
```

## Canonical Chain

```text
G0 Universal Orientation
    ↓
G0 Implementation Track Orientation
    ↓
G0 Gate Depth Decision
    ↓
G0 Industry Classification Branch
    ↓
G0 Jurisdiction / Compliance Branch
    ↓
G0 Final Industry Orientation
    ↓
G0 Business Type / Value-Flow Orientation
    ↓
G0 Locus / Boundary Topology Orientation
    ↓
G0 Completion Horizon Orientation
    ↓
G0 Work Bridge
    ↓
Gate 1: Target Work Definition
```

## Navigation

| File | Purpose |
|---|---|
| [`00-canonical-spec.md`](./00-canonical-spec.md) | Full Gate 0 doctrine and orientation chain |
| [`01-decision-tree.md`](./01-decision-tree.md) | Agent-executable decision path |
| [`02-gate-depth-registry.md`](./02-gate-depth-registry.md) | Default Gate 0 depth by implementation track |
| [`03-agent-runbook.md`](./03-agent-runbook.md) | Operational instructions for AI agents |
| [`04-examples.md`](./04-examples.md) | Applied examples across tracks and industries |
| [`templates/gate-0-standing-payload.md`](./templates/gate-0-standing-payload.md) | Reusable Markdown payload template |

## Key Design Rules

1. **Implementation path determines default orientation depth.**
2. **Industry classification provides the operating field of vision.**
3. **Jurisdiction and compliance load the hard external shell.**
4. **Business type orients value-flow mechanics.**
5. **Locus and boundary topology determine where the AI stands.**
6. **Completion horizon determines what can truthfully be completed.**
7. **The Work Bridge emits the Gate 1-ready work object.**
8. **No lower layer may weaken a higher-risk constraint.**

## Relationship to Gate 1

Gate 0 asks:

> What world am I in, where do I stand, and am I allowed to enter the work?

Gate 1 asks:

> Now that I am admitted, what is the exact target workflow and how is it structured?

Gate 0 is orientation and admission. Gate 1 is work definition.
