# BESSER Agent Skills

A collection of AI agent skills by [BESSER-PEARL](https://github.com/BESSER-PEARL), the open-source low-code platform research group at the Luxembourg Institute of Science and Technology (LIST).

These skills work with any agent that supports the [Agent Skills](https://skills.sh) specification: Claude Code, Cursor, GitHub Copilot, Windsurf, and more.

## Available Skills

| Skill | Description |
|-------|-------------|
| [research-paper-review](./research-paper-review/) | Systematic academic paper review with numerical consistency checks, structured critique, venue-specific feedback, and prioritized action items |

## Installation

Install all skills:

```bash
npx skills add BESSER-PEARL/agent-skills
```

Install a specific skill:

```bash
npx skills add BESSER-PEARL/agent-skills@research-paper-review
```

## Usage

Once installed, skills activate automatically when the agent detects a matching task. You can also invoke them explicitly:

```
/research-paper-review
```

### Example: Reviewing a Paper

Provide the paper (PDF, LaTeX, or text) and optionally specify the target venue and paper type:

```
Review this paper for ICSE 2026 as a full research paper submission.
```

The skill will produce a structured review covering summary, strengths, weaknesses, numerical consistency checks, venue-specific recommendations, and a prioritized list of actions.

## Contributing

We welcome contributions of new skills or improvements to existing ones.

### Adding a New Skill

1. Create a directory with your skill name (lowercase, hyphens only)
2. Add a `SKILL.md` with YAML frontmatter (`name` and `description` required)
3. Optionally add a `package.json` for metadata
4. Submit a pull request

### Skill Structure

```
my-skill/
├── SKILL.md          # Agent instructions (required)
├── package.json      # Metadata (optional)
├── references/       # Supporting docs loaded on demand (optional)
└── scripts/          # Automation helpers (optional)
```

## About BESSER-PEARL

[BESSER](https://github.com/BESSER-PEARL/BESSER) is an open-source low-code platform for building smart applications using model-driven engineering. Learn more at [besser.readthedocs.io](https://besser.readthedocs.io).

## License

MIT
