# CORE AI Public

CORE is a new AI model architecture under private development, aimed at addressing core weaknesses in modern AI systems: unreliable outputs, hallucinations, limited working context, weak long-term retention, high memory cost, and difficulty transferring knowledge to new problems.

This repository is the public-facing evidence and documentation surface for CORE. It is intentionally documentation-first and does **not** contain the private implementation, training system, model internals, benchmark generators, weights, proprietary curriculum construction, or patent-sensitive mechanisms.

## Current Status

CORE is in active private development. Public materials in this repository are limited to non-enabling descriptions, sanitized benchmark/evaluation summaries, and investor-safe technical framing.

The private engineering repository remains the source of truth for implementation work. This repository exists to make the public evidence trail readable, disciplined, and shareable without disclosing the engine.

## What CORE Is Exploring

CORE investigates whether new model-architecture choices can improve reliability, reduce hallucination-like failure modes, support more durable knowledge retention, and make learned structure more reusable across tasks.

Publicly, the project is concerned with several well-known pressure points in LLMs, SLMs, SSMs, and adjacent model families:

- non-deterministic or unstable outputs
- hallucinations and unsupported assertions
- limited effective context
- weak durable memory or retention
- high memory and compute footprint
- shallow pattern matching instead of structured mastery
- brittle transfer to structurally related tasks

Primary public research themes:

- reliability and repeatability
- hallucination resistance
- memory and context efficiency
- durable retention
- structured mastery over surface memorization
- compositional reasoning under controlled pressure
- benchmark protocols that track learning progression
- transparent limits around what is and is not yet proven

## What "Controlled Benchmark" Means Here

A controlled benchmark is an evaluation where the task family, baseline, scoring method, comparison condition, run metadata, and limitations are recorded clearly enough that results can be interpreted honestly.

It does not mean the private benchmark generator, private tasks, scoring internals, or training mechanism are public.

## What This Repository Contains

- public project overview
- high-level problem framing
- public claims boundary
- evaluation philosophy
- benchmark result templates
- sanitized public benchmark area
- public disclosure and IP boundary
- investor-safe technical brief scaffold

## What This Repository Does Not Contain

- private CORE source code
- training implementation
- model weights or checkpoints
- proprietary data pipelines
- curriculum generation internals
- benchmark generator logic
- private evaluation traces
- implementation-level architecture diagrams
- patent-sensitive mechanisms

## Public Disclosure Boundary

This repository is a controlled public disclosure surface. It is designed to communicate evidence and direction without teaching reproduction of the underlying invention.

Before publishing any material here, classify it using the disclosure labels in [docs/04_ip_boundary.md](docs/04_ip_boundary.md):

- `PUBLIC_OK`
- `PUBLIC_SUMMARY_ONLY`
- `CONFIDENTIAL_CORE`
- `PATENT_REVIEW_REQUIRED`
- `TRADE_SECRET`

When in doubt, do not publish. Summarize at a higher level or hold for legal/IP review.

## Documentation Index

Start here:

- [Documentation Index](docs/INDEX.md)
- [Problem Statement](docs/01_problem.md)
- [Evaluation Philosophy](docs/02_evaluation_philosophy.md)
- [Public Claims](docs/03_public_claims.md)
- [IP Boundary and Disclosure Policy](docs/04_ip_boundary.md)
- [Results Template](docs/05_results_template.md)
- [Benchmark Area](benchmarks/README.md)
- [Public Technical Brief](reports/CORE_Public_Technical_Brief_v0.1.md)

## Public Communication Principle

Truthful excitement without enabling reproduction.

CORE should be presented with technical seriousness, sober claims, and clear limits. The goal is not hype. The goal is to make the project legible, promising, and evidence-driven while preserving the private engine.

## Contact

For serious technical, investment, or collaboration inquiries, contact AssetOverflow through GitHub or the official channels associated with this project.
