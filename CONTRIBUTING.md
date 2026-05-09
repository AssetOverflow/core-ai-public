# Contributing to CORE

Thank you for your interest in CORE. This document describes how contributions to the public-facing documentation and architecture narrative are handled.

> **Note:** The core implementation is maintained in a private repository. This public repository accepts contributions to documentation, architecture discussion, and benchmark descriptions only.

---

## What You Can Contribute

- Corrections or clarifications to architecture documentation
- Questions, discussion, or feedback via GitHub Issues
- Suggestions for benchmark methodology descriptions
- Proposals for new public documentation topics

## What Requires Private Repo Access

- Code contributions (all source code is in the private repository)
- Curriculum corpus contributions
- Benchmark harness modifications

If you are interested in a research or engineering collaboration, open an issue or contact us via the address in [SECURITY.md](SECURITY.md).

---

## Documentation Standards

All documentation in this repository must adhere to the following principles from the CORE architecture philosophy:

1. **Share the "what" and "why."** Never document implementation details, operator internals, or algorithm specifics in the public repo.
2. **Accuracy over completeness.** If you are unsure whether something is safe to document publicly, open an issue and ask rather than guessing.
3. **Architecture narrative, not code narrative.** Documentation should describe what a component is responsible for and why it exists — not how it is implemented.

---

## Issue and PR Process

1. Open an issue describing the change you want to make.
2. Wait for acknowledgment before beginning a PR.
3. Keep PRs focused on a single topic.
4. Ensure no import paths, file paths, operator signatures, threshold values, or source code references appear in any documentation.

---

## Code of Conduct

All contributors are expected to engage respectfully. Architectural disagreements are welcome as issues; personal attacks are not.
