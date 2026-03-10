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

### Option A: Agent skills CLI (Claude Code, Cursor, Copilot, Windsurf, etc.)

```bash
npx skills add BESSER-PEARL/agent-skills@research-paper-review
```

This auto-installs the skill into your local agent. It activates automatically when you share a paper.

### Option B: ChatGPT, Claude, Gemini, or any other AI chat

No installation needed. Just:

1. Copy the contents of [SKILL.md](./SKILL.md)
2. Paste it as:
   - **ChatGPT** → Custom Instructions or start of conversation
   - **Claude.ai** → Project Knowledge or start of conversation
   - **Gemini** → Gems or start of conversation
3. Upload your paper (PDF) and ask for a review

> **Tip:** For best results, paste the SKILL.md content first, then upload the paper and write:
> *"Review this paper for [VENUE] as a [TYPE] submission."*

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
