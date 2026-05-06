# IP Boundary and Public Disclosure Policy

This repository is public. Treat every committed word as a public disclosure.

This document defines the boundary between safe public communication and private CORE material.

## Purpose

The purpose of this repository is to provide a public evidence and communication surface for CORE without disclosing enabling details of the private invention, implementation, training system, benchmark generators, data pipelines, or commercialization strategy.

## Not Legal Advice

This document is an internal operating policy for public disclosure discipline. It is not legal advice. Patent, trade-secret, export-control, securities, and investment-related questions should be reviewed by qualified counsel.

## Non-Negotiable Rule

Do not publish anything that would allow a skilled practitioner to reproduce the private CORE mechanism.

When in doubt, do not publish.

## Disclosure Labels

All candidate materials should be classified before publication.

| Label | Meaning | Public handling |
|---|---|---|
| `PUBLIC_OK` | Safe to publish directly | May be committed after normal review |
| `PUBLIC_SUMMARY_ONLY` | May be described at a high level but not copied | Rewrite as non-enabling summary |
| `CONFIDENTIAL_CORE` | Private project material | Do not publish |
| `PATENT_REVIEW_REQUIRED` | May affect patentability or claim strategy | Hold until reviewed by qualified counsel |
| `TRADE_SECRET` | Private mechanism, data, process, or strategy | Keep private indefinitely unless strategy changes |

## Presumptive Classifications

| Material | Default label |
|---|---|
| Private source code | `CONFIDENTIAL_CORE` |
| Training loops | `PATENT_REVIEW_REQUIRED` / `TRADE_SECRET` |
| Model internals | `PATENT_REVIEW_REQUIRED` / `TRADE_SECRET` |
| Curriculum construction details | `PATENT_REVIEW_REQUIRED` / `TRADE_SECRET` |
| KAU/KAC/KAE-style internal schemas or equivalents | `PATENT_REVIEW_REQUIRED` / `TRADE_SECRET` |
| Benchmark generator logic | `TRADE_SECRET` |
| Private benchmark task sets | `CONFIDENTIAL_CORE` |
| Sanitized aggregate results | `PUBLIC_SUMMARY_ONLY` |
| Public technical framing | `PUBLIC_OK` if non-enabling |
| Investor-safe technical brief | `PUBLIC_SUMMARY_ONLY` until reviewed |
| Implementation-level diagrams | `PATENT_REVIEW_REQUIRED` |
| High-level conceptual diagrams | `PUBLIC_SUMMARY_ONLY` |
| Model weights/checkpoints | `TRADE_SECRET` |
| Private evaluation traces | `CONFIDENTIAL_CORE` |
| Commit history from private repo | `CONFIDENTIAL_CORE` |

## Publicly Acceptable Content

The following can usually be public if written carefully:

- high-level problem statements
- high-level project goals
- non-enabling architecture descriptions
- sanitized benchmark summaries
- aggregate metrics
- public limitations
- run metadata that does not reveal private internals
- contact and collaboration information
- public milestones

## Prohibited Content

Do not publish:

- private implementation source
- exact algorithms
- training procedures
- benchmark generators
- private prompts or traces
- model weights
- private datasets
- proprietary schemas
- detailed memory formats
- internal state-transition logic
- implementation-level diagrams
- private repo commit history
- ablations that reveal the mechanism
- anything copied from confidential planning docs without review

## Benchmark Disclosure Rules

Public benchmark summaries may include:

- benchmark family name
- high-level purpose
- date
- aggregate score
- baseline comparison
- qualitative interpretation
- limitations
- disclosure classification

Public benchmark summaries must not include:

- generator source
- full private task corpus
- private scoring code
- hidden rubrics
- training traces
- task variants that expose construction logic
- enough examples to reconstruct the benchmark distribution

## Patent-Sensitive Warning

Public disclosure can affect patent rights. Some jurisdictions may treat public disclosure before filing as novelty-destroying. The United States has limited grace-period rules for some inventor disclosures, but international protection can be stricter.

Therefore, this repository should remain non-enabling unless and until an explicit IP strategy says otherwise.

## Publication Checklist

Before committing new material here, ask:

1. Does this reveal how CORE works internally?
2. Could a skilled ML engineer reproduce a key mechanism from this?
3. Does this expose training logic, schemas, benchmark generation, or memory internals?
4. Does this include private source, traces, prompts, or data?
5. Does this make a claim that needs evidence?
6. Does this need legal/IP review?
7. Is the material summarized rather than copied from the private repo?

If any answer creates doubt, hold the material.

## Public Communication Principle

Public credibility without enabling reproduction.
