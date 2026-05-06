# Public Benchmark Methodology

This document describes the high-level public methodology used for sanitized CORE benchmark summaries.

Private benchmark generators, scoring internals, task corpora, and implementation details are intentionally withheld.

## Philosophy

The goal of benchmarking is not merely to produce impressive numbers.

The goal is to evaluate:

- reliability
- repeatability
- retention
- transfer
- long-horizon behavior
- memory/context efficiency
- resistance to hallucination-like failure modes

## Public Evaluation Principles

### 1. Controlled Conditions

Public benchmark summaries should clearly define:

- task family
- evaluation category
- metric direction
- baseline condition
- comparison condition
- limitations

### 2. Negative Controls

Where appropriate, evaluations should include conditions that are not expected to improve.

### 3. Repeatability

Repeated evaluations are preferred over isolated examples.

### 4. Public Integrity

Public summaries should avoid:

- benchmark leakage
- generator disclosure
- hidden cherry-picking
- misleading metrics
- implementation leakage

## Public Benchmark Categories

Potential public benchmark categories include:

- semantic drift
- repeatability
- hallucination stress tests
- retention
- transfer
- long-context behavior
- memory efficiency
- quality-per-compute

## Important Boundary

This document intentionally avoids disclosing:

- private benchmark generators
- private prompts
- private datasets
- scoring internals
- architectural mechanisms
- hidden evaluation logic
