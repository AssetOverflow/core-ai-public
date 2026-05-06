# Evaluation Philosophy

CORE evaluation is oriented around learning progression, structured mastery, and compositional pressure.

The purpose of evaluation is not to produce a flattering number. The purpose is to expose whether a system can acquire, retain, compose, and apply knowledge under conditions that reduce trivial shortcuts.

## Principles

### 1. Measure progression, not only static performance

A useful learning system should show measurable improvement across controlled exposure, retention, and transfer conditions.

### 2. Separate public evidence from private machinery

Public results may report protocol, summary metrics, and sanitized examples. They must not reveal proprietary training logic, benchmark generators, private traces, curriculum construction, or implementation-level mechanisms.

### 3. Prefer adversarially boring evidence

The most credible evidence is plain, repeatable, and difficult to dismiss. Results should include limitations, run metadata, and failure cases where possible.

### 4. Track negative controls

A result is stronger when compared against controls that should not improve. CORE public summaries should identify whether negative controls were used, without exposing private control implementation.

### 5. Preserve benchmark integrity

Do not publish enough benchmark detail to train against the benchmark, leak task generators, or create incentives for shallow overfitting.

## Public Evaluation Categories

Public summaries may describe results across categories such as:

- baseline response quality
- post-learning response quality
- retention after delay or process boundary
- transfer to structurally related tasks
- resistance to irrelevant or misleading context
- negative-control behavior
- traceability of run metadata

## Public Reporting Standard

A public result should include:

- date of run
- internal build or commit reference where safe
- evaluation category
- high-level task family
- metric name and definition
- baseline score
- post-condition score
- confidence notes
- limitations
- disclosure classification

## What Public Evaluation Must Not Include

- private benchmark generator code
- full private task sets
- proprietary scoring internals
- training traces
- prompts that reveal hidden mechanisms
- model memory artifacts
- implementation-level diagrams

## Standard of Evidence

CORE should be communicated through evidence that is clear, sober, and falsifiable. Extraordinary claims require extraordinary proof, and public proof must be designed without surrendering the private engine.
