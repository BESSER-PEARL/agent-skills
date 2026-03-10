# research-paper-review

An AI agent skill for systematic academic paper review.

## What It Does

When you share a research paper (PDF, LaTeX, or plain text), this skill guides the agent through a structured review process:

1. **Venue context** — Adapts the review to the target conference/journal standards
2. **Structured summary** — Problem, contributions, methodology, results, limitations
3. **Numerical & consistency checks** — Cross-references numbers across text, tables, and figures; verifies statistics, acronyms, terminology, and citations
4. **Critical analysis** — Evaluates novelty, soundness, significance, clarity, reproducibility, and venue alignment
5. **Actionable feedback** — Strengths, weaknesses, questions, minor issues, and venue-specific recommendations
6. **Top 10 actions** — Prioritized by impact-to-effort ratio so authors know where to start

## Installation

```bash
npx skills add BESSER-PEARL/agent-skills@research-paper-review
```

## Usage

Share a paper with the agent and optionally specify the venue and paper type:

```
Review this paper for ICWE 2026 as a tool demo submission.
```

```
Check this PDF for numerical inconsistencies and broken references.
```

```
Give me pre-submission feedback on our TOSEM journal paper.
```

The agent will fetch venue-specific guidelines when available and produce a review following the output template in [SKILL.md](./SKILL.md).

## Supported Formats

- PDF files (read page by page)
- LaTeX source (`.tex` files, follows `\input` / `\include` commands)
- Plain text / markdown

## Authors

- [Armen Sulejmani](https://github.com/armensulejmani)
- [Ivan David Alfonso](https://github.com/ivan-alfonso)
- [Jordi Cabot](https://github.com/jcabot)

Part of the [BESSER-PEARL](https://github.com/BESSER-PEARL) project at the Luxembourg Institute of Science and Technology.
