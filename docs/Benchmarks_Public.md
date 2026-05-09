# CORE Benchmark Suites

CORE is evaluated against eight benchmark suites designed to measure geometrically grounded cognitive properties. This document lists each suite, what it measures, and a description of the evaluation methodology.

> Benchmark harness code, scoring functions, and pass/fail thresholds are maintained in the private repository.

---

## The Eight Suites

### 1. Vocabulary Coherence
**What it measures:** Whether the vocabulary embedding produces a clean geometric separation between concept classes. A coherent vocabulary means that concepts from different semantic domains (entities, relations, logical operators) occupy distinct, non-overlapping regions of M_E.

**Why it matters:** A distorted vocabulary manifold propagates errors to every downstream component. This is the foundational health check.

---

### 2. Propagation Convergence
**What it measures:** Whether the field propagation operator reliably converges to an attractor basin within a bounded number of steps across a diverse set of query types.

**Why it matters:** An engine that does not consistently converge is non-deterministic in a way that cannot be diagnosed geometrically. Convergence is a prerequisite for correctability.

---

### 3. Correction Permanence
**What it measures:** Whether a Socratic correction (phase cancellation of an erroneous attractor) persists across subsequent sessions, under new queries, and under attempts to re-introduce the corrected error.

**Why it matters:** This is the core claim of the CORE architecture: corrections should be permanent, not statistical nudges. This suite directly tests that claim.

---

### 4. Grade Purity
**What it measures:** Whether the Grade-1/2/3 decomposition of the field is maintained across propagation steps and correction events, i.e., whether entities remain entities, relations remain relations, and modality does not bleed into entity space.

**Why it matters:** Grade purity is an architectural invariant. Leakage between grades is the multivector equivalent of type unsafety.

---

### 5. Vault Reconstruction Fidelity
**What it measures:** Whether long-range context archived in the HyperVault can be reconstructed faithfully on recall, and whether recalled context produces the same downstream field state as if it had remained in the active window.

**Why it matters:** The claim of “effectively infinite context” depends on vault recall being geometrically lossless, not just approximately similar.

---

### 6. Curriculum Gate Integrity
**What it measures:** Whether the curriculum gate system correctly enforces tier sequencing — specifically, whether an out-of-order curriculum load attempt is rejected, and whether the seal digest produced after a tier completion is stable and reproducible.

**Why it matters:** The tiered boot sequence is not a convention; it is a structural requirement for manifold health. The gate system must be provably non-bypassable.

---

### 7. Adversarial Hallucination Resistance
**What it measures:** The engine’s resistance to adversarially crafted prompts designed to elicit low-confidence outputs, field divergence, or Grade-3 energy spikes above the correction threshold.

**Why it matters:** Real-world deployment involves adversarial inputs. This suite characterizes how the query guards and correction operators perform under deliberate stress.

---

### 8. Scaling Geometry Stability
**What it measures:** Whether the three-manifold geometric properties (curvature invariants, attractor density, geodesic separation) remain stable as vocabulary size, curriculum depth, and session length scale upward.

**Why it matters:** A geometry that degrades under scale is not a geometry — it is a heuristic. This suite verifies that the Clifford field and hyperbolic manifold properties hold at production scale.

---

## Benchmark Acceleration Gate

Benchmarks are gated behind a readiness audit before each release. The gate verifies:
- All five pipeline guards are wired and passing.
- Grade purity invariants are registered and active.
- Vocabulary artifact is fully sealed and reproducible.

Benchmark results for each phase release will be posted to this document as they are audited and cleared for public release.
