# Aetheris Governed AI Benchmark Architecture

## Benchmark Architecture v1.1

**Status:** Canonical working architecture; not yet a validated public benchmark release  
**Alignment:** ACIM-E v1.0  
**Date:** 2026-07-10  
**Owner:** Thomas Giza / Aetheris Consulting

This module publishes the current Aetheris benchmark architecture for evaluating governed AI systems in operational, scientific, medical, organizational-optimization, and educational environments.

It is derived from the June 2026 Google Drive documents **Aetheris Benchmark Suite v1.0**, **Aetheris Unified Governed-State Benchmark Architecture**, and **Aetheris VOC Architecture v0.2.1**, then reconciled against the July 2026 ACIM-E enterprise model.

The v1.1 publication preserves the original five-track governed-state evaluation theory while correcting architecture drift:

- Gate 0–9 is replaced by the current ACIM-E Gate 0–8 profile plus continuous operations.
- AI Core is clarified as the cross-cutting implementation spine, not a competing benchmark track.
- Optimization-Bench is broadened from industrial optimization to organizational and operational optimization.
- Human/current-process baselines are treated as contextual comparators, not automatically valid gold standards.
- Unsupported universal baseline and performance claims are removed.
- Cross-cutting, relational, and meta-benchmark layers are added.
- UTSS scenario tests, Benchmark VOC, and the Outcome Validation Score are integrated.
- Public status and MIT repository licensing replace the source document’s confidential-working-document label.

## Module map

- **[Governed AI Benchmark Architecture v1.1](./00-governed-ai-benchmark-architecture-v1.1.md)** — common object model, scoring, gates, benchmark hierarchy, governance, and currentness audit.
- **[Five-Track Core Benchmarks](./01-five-track-core-benchmarks.md)** — GPO-Bench, SciDisc-Bench, Medical-Bench, Optimization-Bench, and Education-Bench.
- **[Benchmark VOC and Outcome Validation](./02-benchmark-voc-and-outcome-validation.md)** — anti-Goodhart calibration, gap taxonomy, OVS, privacy, and authority suspension rules.
- **[Benchmark Case schema](./schemas/benchmark-case.yaml)** — machine-readable case object.
- **[Benchmark Registry schema](./schemas/benchmark-registry.yaml)** — machine-readable suite registry.

## Architecture stack

```text
External capability prerequisites
        ↓
Five-Track Core Benchmarks
        ↓
Cross-Cutting Benchmarks
        ↓
Relational Benchmarks
        ↓
CCIB Meta-Benchmark
        ↓
UTSS Scenario Stress Tests
        ↓
Benchmark VOC + Outcome Validation Score
        ↓
Production telemetry, incidents, and Gate 8 learning
```

## Core doctrine

- Evaluate governed state change, not answer accuracy alone.
- Authority compliance is a hard gate.
- Safety-critical failure cannot be averaged away by a composite score.
- Human performance is a contextual comparator, not a presumption of correctness.
- Every primary metric requires protected countermetrics.
- A benchmark score is provisional until correlated with real operational outcomes.
- Benchmark-driven optimization authority may be suspended when scores and outcomes diverge.

## Publication status

This repository contains a **benchmark architecture and specification**, not a claim that complete benchmark datasets, validated scoring instruments, human-baseline studies, inter-rater reliability results, or prospective outcome evidence already exist for every track. Those remain implementation and research work.

The source Drive documents remain part of the architecture lineage. This repository-native v1.1 module is the current public specification.

## License

Published under the repository’s [MIT License](../../LICENSE).