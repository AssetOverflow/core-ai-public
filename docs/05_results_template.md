# Results Template

Use this template for public benchmark summaries.

The template is designed to expose evidence without revealing private benchmark generators, training mechanisms, or implementation details.

## Result Summary

| Field | Value |
|---|---|
| Result ID | `CORE-PUBLIC-YYYYMMDD-001` |
| Date | `YYYY-MM-DD` |
| Public release version | `v0.0.0` |
| Internal reference | Redacted or safe internal build tag |
| Benchmark family | High-level family name |
| Evaluation category | Baseline / learning progression / retention / transfer / negative control |
| Disclosure label | `PUBLIC_SUMMARY_ONLY` |
| Status | Preliminary / verified / superseded |

## Task Family

Describe the task family at a high level.

Do not include private task generation logic, full hidden prompts, hidden rubrics, or enough examples to reconstruct the benchmark distribution.

## Metric

| Metric | Definition | Direction |
|---|---|---|
| Example metric | High-level definition | Higher is better / lower is better |

## Results

| Condition | Score | Notes |
|---|---:|---|
| Baseline | TBD | Public-safe summary only |
| CORE condition | TBD | Public-safe summary only |
| Negative control | TBD | If applicable |

## Interpretation

Summarize what the result suggests and what it does not prove.

Good public interpretation should include:

- what improved
- what did not improve
- whether controls behaved as expected
- whether the result was repeated
- the main limitation

## Limitations

List limitations plainly.

Examples:

- small public slice
- private benchmark generator withheld
- not yet independently reproduced
- metric under refinement
- result superseded by later protocol

## Disclosure Notes

State what has been withheld and why.

Example:

> The private benchmark generator, scoring implementation, task corpus, and learning traces are withheld to preserve benchmark integrity and intellectual-property boundaries.

## Publication Checklist

- [ ] No private source code
- [ ] No training logic
- [ ] No benchmark generator logic
- [ ] No private task corpus
- [ ] No private prompts or traces
- [ ] No proprietary schemas
- [ ] No model weights
- [ ] No implementation-level diagrams
- [ ] Claim is supported by the shown evidence
- [ ] Disclosure label assigned
- [ ] IP-sensitive content reviewed or excluded
