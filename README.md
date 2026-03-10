# BESSER Agent Skills

A collection of AI agent skills by [BESSER-PEARL](https://github.com/BESSER-PEARL), the open-source low-code platform research group at the Luxembourg Institute of Science and Technology (LIST).

These skills work with **any AI assistant**:

- **Coding agents** (via CLI): Claude Code, Cursor, GitHub Copilot, Windsurf, and [40+ more](https://skills.sh)
- **AI chats** (via copy-paste): ChatGPT, Claude.ai, Gemini, and any LLM that accepts a system prompt

## Available Skills

| Skill | Description |
|-------|-------------|
| [research-paper-review](./research-paper-review/) | Systematic academic paper review with numerical consistency checks, structured critique, venue-specific feedback, and prioritized action items |

## Installation

### Coding agents (Claude Code, Cursor, Copilot, Windsurf, etc.)

Install all skills:

```bash
npx skills add BESSER-PEARL/agent-skills
```

Install a specific skill:

```bash
npx skills add BESSER-PEARL/agent-skills@research-paper-review
```

Once installed, skills activate automatically when the agent detects a matching task. You can also invoke them explicitly with `/research-paper-review`.

### ChatGPT, Claude.ai, Gemini, or any AI chat

No installation needed:

1. Open the [SKILL.md](./research-paper-review/SKILL.md) of the skill you want
2. Copy its contents
3. Paste it into your AI chat as:
   - **ChatGPT** → Custom Instructions or start of conversation
   - **Claude.ai** → Project Knowledge or start of conversation
   - **Gemini** → Gems or start of conversation
4. Upload your paper and ask for a review

## Example

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
