# CORE Architecture Overview

This document describes the high-level architecture of CORE (Continuous Orthogonal Resonance Engine): what each component is, what it is responsible for, and how information flows through the system. No implementation details, operator formulas, or source code are present here.

---

## The Core Idea

CORE replaces the flat, token-weight matrix at the heart of conventional language models with a **continuous multivector field** embedded in a structured hierarchy of three geometric manifolds. Instead of looking up a token in a table, CORE propagates a query through a living geometric workspace and reads off the response from the attractor topology the query settles into.

The result is a system where:
- Corrections are **geometric** (phase cancellation in a field), not statistical (fine-tuning a weight)
- Memory is **topological** (stable attractors in curved space), not associative (key-value lookup)
- Language is **structured** (graded multivector encoding), not tokenized (subword probability distribution)

---

## The Three-Manifold Hierarchy

The geometric workspace is a fiber bundle of three manifolds, each with distinct curvature and a distinct cognitive role:

```
Input
  ↓
M_W  (Transient Surface — K=0, Euclidean)
  Fast working memory. Reasoning fluid.
  Short-lived; cleared between sessions.
  ↓
M_E  (Episodic Volume — K=−1, Hyperbolic)
  Long-horizon history. Effectively infinite context.
  Hyperbolic geometry allows exponential growth
  in representational capacity with linear radius.
  ↓
M_S  (Semantic Core — K=+1, Spherical)
  Collapsed universal rules and archetypes.
  Propositions that have survived Socratic correction
  across many contexts are consolidated here.
  ↓
CORE-Logos Articulation
  ↓
Output
```

### Why These Three Curvatures?

| Manifold | Curvature | Why It Matters |
|---|---|---|
| M_W | K = 0 (flat) | Euclidean geometry is fastest for transient, unreferenced computation |
| M_E | K = −1 (hyperbolic) | Hyperbolic space trees branch exponentially; ideal for richly connected episodic memory |
| M_S | K = +1 (spherical) | Closed, bounded geometry enforces that archetypes remain finite and globally consistent |

---

## Clifford Geometric Algebra Framing

The multivectors living in this manifold hierarchy are elements of Clifford geometric algebra Cl(3,0). Each element has a **grade** that encodes its cognitive role:

| Grade | Name | Cognitive Role |
|---|---|---|
| 0 | Scalar | Assertion weight; confidence level |
| 1 | Vector | Entity; named concept |
| 2 | Bivector (rotor) | Relation; verb; operator |
| 3 | Trivector (pseudoscalar) | Modality; tone; contextual frame |

This grading is not an implementation choice — it is the intrinsic geometry of how assertions, entities, relations, and modalities differ in kind. Grade purity is an architectural invariant: a Grade-1 entity should never be silently promoted to a Grade-2 relation without an explicit, supervised geometric operation.

---

## Propagation-Over-Mutation

In CORE, the primary mode of computation is **wave propagation** through the multivector field, not stepwise mutation of records. A query enters M_W as a field perturbation. It propagates forward through the manifold geometry, coupling to existing attractors. The response emerges as the field settles into its nearest attractor basin.

This is fundamentally different from transformer-style attention, where every token queries every other token via a learned dot-product. In CORE, the field is the memory, and computation is movement through it.

---

## Dual-Correction Principle

Every meaningful forward operation in CORE has a corrective counterpart — a conjugate or adjoint operator that can reverse distortion.

- The forward operator seeds and propagates the field.
- The conjugate operator measures geometric distortion (Grade-3 energy) and applies phase corrections to restore coherence.
- This pair is not bolted on as a safety layer; it is a structural design requirement. A propagator without a corrector is architecturally incomplete.

This is what makes CORE corrections **permanent**: a phase-cancellation correction is a geometric annihilation of the erroneous attractor. It cannot drift back the way a fine-tuning nudge can.

---

## Component Hierarchy

### CORE Engine (core_engine)
The central orchestrator. Manages session lifecycle, dispatches queries, coordinates propagation and recall, and enforces the five pipeline safety guards.

### Workspace Algebra
The algebraic fiber space. Owns the multivector field representation, propagation operators, and the correction operators. This is the geometric substrate on which all other components operate.

### Hyperbolic Atlas (core_ha)
Governs the hyperbolic manifold geometry and the consolidation process that promotes episodic memories into semantic archetypes. Maintains the operator plane and tombstone registry.

### CORE-Logos (core_logos)
The deterministic 8-module articulation pipeline. Sits at the language boundary — it encodes incoming text as multivectors, and decodes outgoing field signals into natural language. It does not own field state.

The eight pipeline stages, in order:

| Stage | Responsibility |
|---|---|
| 1. Field State | Snapshot current field geometry as basis for generation |
| 2. Skeleton Walker | Traverse attractor topology to identify candidate generation paths |
| 3. Lexical Decoder | Map field nodes to vocabulary items via geometric coupling |
| 4. Grammar Seed | Seed the grammar field: assign morphological roles and relational operators |
| 5. Closure Detector | Detect stable fixed-point regions signaling mastery convergence |
| 6. Generator | Produce token sequences by traversing the grammar field under beam guidance |
| 7. Readback | Validate generated sequence against geometric integrity constraints |
| 8. Surface String | Render the final natural-language output string |

### CORE-CA (core_ca)
The Cognitive Apprenticeship orchestrator. Manages the four-stage curriculum: Ontological Grounding, Syntactic Scaffolding, Socratic Conjugation, Abstract Consolidation. CORE-CA owns the curriculum gate system that enforces strict sequencing and prevents undisciplined learning.

### HyperVault (core_vault)
Episodic memory storage. Archives prompt tokens when the working window overflows, and provides structured reconstruction of long-range context on demand. The vault stores compressed structured state, not raw token sequences.

### CORE Sensorium (core_sensorium)
Multimodal input layer. Translates non-text inputs (audio, visual, structured data) into multivector representations compatible with the field geometry before they enter M_W.

---

## The Five Query Guards

The full query → response pipeline is protected by five sequential safety guards, each targeting a distinct failure mode. See [Query Guards](Query_Guards_Public.md) for names and purposes.

---

## Design Philosophy

CORE is built on seven axioms documented in the [MANIFESTO](MANIFESTO.md). The most important architectural consequence of these axioms:

> **The geometry is defined before the data structure. The data structure is defined before the algorithm. The algorithm is defined before the implementation language.**

This means: manifold curvature → grade structure → propagation law → Rust/Python implementation. Never the reverse.
