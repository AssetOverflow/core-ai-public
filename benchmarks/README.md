# Public Benchmark Area

This directory is reserved for public benchmark summaries and sanitized evaluation artifacts.

It must not contain private benchmark generators, hidden task sets, private prompts, private scoring code, training traces, model internals, or implementation details.

## Allowed Content

- aggregate result summaries
- public-safe CSV or JSON summaries
- sanitized charts
- high-level protocol notes
- small public examples that do not reveal private generation logic
- limitations and status notes

## Disallowed Content

- benchmark generator source code
- full private task corpora
- hidden rubrics
- private scoring implementations
- proprietary task construction logic
- training traces
- model memory artifacts
- source code copied from the private repo

## Suggested Layout

```text
benchmarks/
  README.md
  public_results/
    results_summary.csv
    results_summary.json
    charts/
```

## Result Template

Use [docs/05_results_template.md](../docs/05_results_template.md) before publishing any result.

## Disclosure Classification

Most benchmark outputs should be treated as `PUBLIC_SUMMARY_ONLY` unless explicitly reviewed and marked `PUBLIC_OK`.
