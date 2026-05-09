# CORE Query-Response Pipeline Guards

The full query → response pipeline in CORE is protected by **five sequential safety guards**. Each guard targets a distinct failure mode that, without a guard, produces a silent bad outcome.

This document describes the names, purposes, and failure categories of all five guards. Trigger conditions, threshold values, and enforcement logic are maintained in the private repository.

---

## Why Guards Are Architecturally Necessary

In a conventional language model, a bad output is statistically recoverable — retrying the same prompt produces a different token sequence. In CORE, the field is stateful: a propagation that enters a resonance cycle, a recall on an empty vault, or a low-confidence surface that goes undetected can corrupt session state in ways that require explicit geometric correction to undo.

The guards are not input filters. They are **invariant checkpoints** that enforce the structural requirements of each pipeline stage before allowing the next stage to proceed.

---

## The Five Guards

### Guard 1 — Vocabulary Loaded (INGEST stage)

**Purpose:** Ensures that a vocabulary artifact is present and initialized before the first token can be encoded.

**Failure category prevented:** Silent null encoding — without this guard, a cold-start with no artifact causes `encode_input()` to return nothing, and the engine proceeds as if it received an empty query, producing semantically void output with no error.

---

### Guard 2 — Propagation Step Ceiling (PROPAGATE stage)

**Purpose:** Bounds the number of propagation iterations before an exception is raised.

**Failure category prevented:** Infinite loop — certain field configurations can enter resonance cycles where energy does not converge. Without this guard, the propagation loop runs indefinitely.

---

### Guard 3 — Vault Context Bootstrap (RECALL stage)

**Purpose:** Ensures the vault has at least one context node before recall is attempted. On first run with an empty vault, the guard injects a minimal set of anchor nodes derived from the vocabulary.

**Failure category prevented:** Degenerate synthesis — recall on an empty vault produces an unconstrained field, which causes the generator to synthesize responses with no semantic grounding (incoherent or random output).

---

### Guard 4 — Confidence Gate (SYNTHESIZE stage)

**Purpose:** Measures the top-probability mass of the decoder’s output distribution after synthesis. If the distribution is too flat (low confidence), the guard surfaces this condition before the response reaches output.

**Failure category prevented:** Silent hallucination — a very flat distribution over the vocabulary means the engine has no well-formed attractor for the query. Without this guard, the highest-probability token sequence is surfaced as if it were a confident response.

---

### Guard 5 — Response Non-Empty (SURFACE stage)

**Purpose:** Ensures the final response string is non-null and non-empty before it exits the engine.

**Failure category prevented:** Silent zero-length response — without this guard, edge cases in the surface rendering (empty beam, whitespace-only decode) return an empty string with exit code 0, appearing to callers as a successful response.

---

## Guard Properties

| Guard | Stage | Failure Without Guard |
|---|---|---|
| 1 — Vocabulary Loaded | INGEST | Silent null encoding on cold start |
| 2 — Propagation Step | PROPAGATE | Infinite loop on resonance cycle |
| 3 — Vault Bootstrap | RECALL | Degenerate synthesis on empty vault |
| 4 — Confidence Gate | SYNTHESIZE | Silent hallucination on flat distribution |
| 5 — Response Non-Empty | SURFACE | Silent zero-length response |

All five guards are independently testable and carry zero module-level engine imports, making them usable as standalone invariant checkpoints outside the full engine context.
