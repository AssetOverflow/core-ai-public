# CORE-Bench Built Evidence

This document summarizes public-safe evidence from the private CORE-Bench implementation.

It intentionally avoids publishing benchmark generators, private prompts, hidden task corpora, scoring internals, or implementation-level runtime details.

## What Exists Internally

CORE-Bench already includes a real benchmark harness with:

- suite loading from structured benchmark definitions
- benchmark runner execution
- adapter-based runtime boundaries
- deterministic stub and null-control adapters
- real CORE runtime adapter path
- JSON report generation
- Markdown report generation
- CLI adapter selection
- replay determinism checks
- retrieval improvement checks
- convergence-with-feedback checks
- articulation-mode checks
- starter suite validation

## Why This Matters

This is meaningful because CORE-Bench is not merely a presentation layer.

It already has testing surfaces that check whether benchmark behavior is:

- measurable
- repeatable
- reportable
- adapter-scoped
- resistant to false positives through negative controls

## Public-Safe Evidence Categories

### Retrieval Improvement

The benchmark harness can evaluate whether a runtime condition improves retrieval behavior compared with a before condition.

Public-safe claim:

> CORE-Bench includes tests for retrieval-improvement behavior under controlled benchmark cases.

Not public-safe without sanitized result release:

> CORE has solved memory or retrieval.

---

### Null Negative Control

The benchmark harness includes a null adapter that is expected to fail learned-memory improvement checks.

Public-safe claim:

> CORE-Bench includes negative-control behavior that can fail when memory/retrieval improvement is absent.

Why this matters:

- negative controls reduce false confidence
- failure cases are part of credible evaluation
- this is stronger than only showing successful demos

---

### Replay Determinism Checks

The benchmark harness can detect nondeterministic replay behavior.

Public-safe claim:

> CORE-Bench includes replay-determinism checks that flag unstable repeated responses.

Why this matters:

- repeatability is a major AI reliability problem
- deterministic replay checks are useful for regression detection

---

### Convergence with Feedback

The benchmark harness includes checks for whether feedback can move a settling response toward a stable response under a defined evaluation.

Public-safe claim:

> CORE-Bench includes convergence-with-feedback evaluation patterns.

Boundary:

- public docs may describe the existence of this evaluation category
- private mechanics and hidden benchmark details remain withheld

---

### Report Generation

The benchmark harness can write JSON and Markdown reports.

Public-safe claim:

> CORE-Bench already supports structured report export suitable for sanitized public summaries.

Why this matters:

- public evidence can be generated systematically
- reporting infrastructure is already present
- future public benchmark dashboards can be fed by sanitized exports

---

### Real Runtime Adapter Execution

The benchmark harness includes an adapter path that executes a real CORE runtime minimal turn.

Public-safe claim:

> CORE-Bench includes an adapter path for executing the real CORE runtime rather than only stubbed responses.

Boundary:

- this does not claim production readiness
- this does not expose runtime implementation details
- this does not imply all benchmark goals are complete

## Summary

CORE-Bench already provides credible evidence infrastructure in areas that matter deeply:

- retrieval improvement
- negative controls
- replay determinism
- convergence evaluation
- report generation
- adapter-based runtime boundaries
- real-runtime execution path

The next public step is to export sanitized benchmark reports and charts derived from these internal surfaces.
