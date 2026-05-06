# CORE Public Technical Brief v0.1

Status: Draft public scaffold  
Disclosure classification: `PUBLIC_SUMMARY_ONLY`  
Repository: `AssetOverflow/core-ai-public`

## Executive Summary

CORE is a private AI research and engineering project focused on measuring and improving model mastery, retention, and transfer under controlled benchmark conditions.

This brief intentionally avoids implementation-level disclosure. It summarizes the public problem, project direction, evaluation posture, and evidence strategy.

## Problem

AI systems can achieve strong performance on static benchmarks while still leaving open questions about durable understanding, controlled transfer, retention, and mastery of fundamentals.

CORE is designed around the hypothesis that learning systems should be evaluated by progression toward structured mastery, not only by isolated answer quality.

## CORE Direction

At a public level, CORE investigates:

- learning progression under controlled exposure
- compositional reasoning from structured primitives
- retention and transfer behavior
- negative-control evaluation
- benchmark evidence that resists shallow interpretation

Private implementation details are withheld.

## Evaluation Strategy

Public evaluation summaries should report:

- task family at a high level
- metric and direction
- baseline condition
- CORE condition
- negative controls where applicable
- limitations
- disclosure classification

Private benchmark generators, task corpora, scoring internals, and learning traces are not published.

## Current Public Status

The public repository is currently a documentation and evidence scaffold. Public benchmark summaries will be added only after disclosure review and sanitization.

## What Is Withheld

The following are intentionally withheld:

- private source code
- training logic
- model internals
- benchmark generators
- curriculum construction details
- proprietary schemas
- private traces
- model weights/checkpoints
- implementation-level architecture diagrams

## Near-Term Public Milestones

- publish the first sanitized benchmark result summary
- add a public progress log
- add a public glossary with non-sensitive terminology
- prepare an investor-safe one-page overview
- define an independent-review path that does not compromise private IP

## Communication Standard

CORE should be presented through sober, testable claims. Public materials should make clear what is proven, what is preliminary, and what is withheld.

Public credibility without enabling reproduction.
