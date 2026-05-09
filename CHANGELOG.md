# CHANGELOG

All significant engineering phases to the CORE architecture are recorded here in reverse chronological order.

---

## 2026-05 — Batch 15: Documentation Pass — CORE-Logos Module Docs

**Scope:** First dedicated documentation pass for the core-logos articulation layer. Four reference documents written covering every module added in Batches 13–15. Each doc covers: Purpose, Design Contract, key responsibilities, data flow, and integration points.

| Doc | Module Covered |
|---|---|
| `CORPUS_DIGEST` | Per-course hash audit: SHA-512 + BLAKE3 hybrid integrity verification |
| `CURRICULUM_GATE` | All three gate types (entry, completeness, seal) and the seal format |
| `CURRICULUM_SEQUENCE` | Schema reference, status lifecycle, seal integrity contract |
| `GRAMMAR_OPERATORS` | Dual-correction grammar pair and trilingual axis system |

---

## 2026-05 — Batch 15a: Hypervault ↔ CORE-Logos Integration

**Scope:** The hypervault memory system was wired into the CORE-Logos pipeline as the long-range context reconstruction layer. Vault entries accumulated on prompt-window overflow are now accessible to field operators for reconstruction-on-demand. Consistent with the Reconstruction-over-storage axiom: the vault stores compressed structured state, not raw token sequences.

---

## 2026-05 — Batch 14: Grammar Operators — Seed, Conjugate, Closure Detector

**Scope:** The dual-correction grammar operator pair and the closure detector that signals mastery convergence.

- **Grammar Seed (forward operator):** Seeds the grammar field — the geometric structure of grammatical relations — from corpus data. Operates across three Tier 0 languages, mapping surface morphology onto a shared axis space.
- **Grammar Conjugate (corrective operator):** Detects coherence violations in the grammar field and propagates adjoint corrections to restore geometric consistency.
- **Closure Detector:** Monitors the grammar field for stable fixed-point regions that signal mastery convergence. Output consumed by the curriculum gate system.
- **Axes:** Defines the shared axis coordinate system (person, number, gender, tense, mood, voice, case) across all three languages.

**Axiom alignment:** Geometry-first, Field-state, Propagation-over-mutation, Dual-Correction, Reconstruction-over-storage.

---

## 2026-05 — Batch 13: Curriculum Gate — Curriculum Enforcement Runtime

**Scope:** The curriculum enforcement layer that turns the curriculum sequence specification from a planning document into a hard gate system. Nothing in the CORE-Logos curriculum advances on the honor system from this point forward.

**Three gate types:** TierEntryGate (prior tier sealed), TierCompletenessGate (all courses manifested and mastery passed), TierSeal (writes a cryptographic seal).

**Axiom alignment:** Reality-over-inheritance — the gate re-reads every manifest and mastery file on every run; status fields in the sequence are metadata, not shortcuts.

---

## 2026-04 — Gap Closure Series (Gaps 1–8): Async, Beam, Correction, Vault Recall

**Scope:** Eight targeted architectural gap closures identified by a full stack audit:

| Gap | Area | What Was Achieved |
|---|---|---|
| Gap 1 | Prompt encoding | Replaced centroid with sequential geometric-product walk preserving word order |
| Gap 1 (Orchestrator) | Output reflection | Model's own output now conditions the discourse field (previously invisible) |
| Gap 2 | Generation node | Replaced fixed-slot constant with live field traversal following semantic trajectory |
| Gap 3 | Vault recall | `recall_from_vault()` re-conditions the live field on archived vault entries on demand |
| Gap 4 | Mid-generation correction | Every N tokens, Grade-3 energy measured; dual-correction operator fires if threshold exceeded |
| Gap 5 | G3 energy logging | Post-turn Grade-3 energy logged; drifting turns visible in production logs |
| Gap 6 | Beam trajectory | Per-beam trajectory-following node selection; mid-beam correction loop closed |
| Gap 7 | Async correctness | Parallel beam expansion, async-safe conditioning, batch generation surface added |
| Gap 8 | Attractor mask | ManifoldState now caches attractor mask at snapshot boundaries; per-query scan eliminated |

---

## 2026-04 — Clifford Reverse Operator: Cross-Layer Wiring

**Scope:** The Clifford reverse operator (the Grade-2/3 sign flip in Cl(3,0)) wired through all three architectural layers: Rust kernel → Python reconstruction → CA probes. This is the foundational Dual-Correction operator. Without it, mid-generation correction and beam correction have no corrective operator to call.

---

## 2026-04 — Documentation Overhaul (Production Readiness)

**Scope:** All documentation gaps identified in the Phase 6 audit closed. Navigation Hub expanded to a full indexed map of all docs. Query Guards reference written. AGENTS.md rewritten from stub to production agent context document. README updated with Phase 1–6 status table and new-contributor onboarding.

---

## 2026-04 — Phase 6: Query-Response Pipeline Guards

**Scope:** Five typed safety guards added to protect the full query → response pipeline:

1. **Guard 1 — Vocabulary Loaded:** Prevents silent failures when no vocabulary artifact is present at startup.
2. **Guard 2 — Propagation Step:** Prevents infinite loops when the field enters a resonance cycle.
3. **Guard 3 — Vault Context:** Bootstraps an empty vault with anchor nodes on first run; prevents degenerate synthesis.
4. **Guard 4 — Confidence Gate:** Detects and surfaces low-confidence hallucinations before they reach the output surface.
5. **Guard 5 — Response Non-Empty:** Rejects silent zero-length responses before they exit the engine.

All five guards are independently testable with zero module-level engine imports.

---

## 2026-04 — Phase 5–6 Transition: Makefile Integration and Scripts Layer

**Scope:** A complete local CI harness mirroring what a production CI pipeline runs. All entry points wired as `make` targets. Five-stage CI-parity runner (lint, typecheck, tests, adversarial suite, benchmark gauntlet). Vocabulary artifact generator supporting stub mode (fast) and live mode.

---

## Pre-2026 — Phase 6 (Logos Readiness)

**Scope:** Transitioned to a Logos-complete deterministic architecture. Legacy probabilistic abstractions purged. Replaced with the deterministic 8-module pipeline: field state → skeleton walker → lexical decoder → grammar seed → closure detector → generator → readback → surface string. Zero-copy basis injection. Geometric invariant registry established.

---

## Pre-2026 — Phase 5 (Autonomous Learning Loop)

**Scope:** Response classification, attractor reinforcement, and JIT recall wired into the closed cognitive loop. The engine can now accumulate knowledge persistently without external intervention.

---

## Pre-2026 — Phase 4 (MLX Bridge and Scaling)

**Scope:** Dynamic rotor generation, MLX-LM embedding bridge, Poincaré visualisation, and scaling benchmarks. Apple Silicon GPU acceleration via MLX.

---

## Pre-2026 — Phase 3 (Grade Safety and OS Integration)

**Scope:** Bifurcation engine, conjugate unlearning mechanism, grade safety enforcement, full OS integration layer.

---

## Pre-2026 — Phase 2 (Attractor Dynamics and Topology)

**Scope:** Attractor dynamics and temperature, topological coordinates with exponential map, grade decomposition and promotion, JIT memory, ingestion pipeline.

---

## Pre-2026 — Phase 1 (Foundation)

**Scope:** Conjugate operator, hyperbolic routing, initial closed cognitive loop wiring.
