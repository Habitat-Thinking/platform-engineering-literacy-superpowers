# Contributing to Platform Engineering Literacy Superpowers

Thank you for your interest in contributing to this plugin.

## Plugin Structure

```
platform-engineering-literacy-superpowers/
├── .claude-plugin/
│   └── plugin.json          # Plugin manifest
├── skills/                   # Skills (assessment, future additions)
│   └── platform-literacy-assessment/
│       ├── SKILL.md          # Facilitator protocol
│       └── references/       # Assessment content
├── README.md
├── CONTRIBUTING.md
├── LICENSE
└── CHANGELOG.md
```

## Adding a New Skill

1. Create a directory under `skills/` with a descriptive name
2. Add a `SKILL.md` with YAML frontmatter:

```yaml
---
name: skill-name
description: When this skill should be triggered — be specific about trigger phrases
---
```

3. If the skill needs reference content, add a `references/` subdirectory
4. Open a PR with a clear description of what the skill does and when to use it

## Adding Agents, Commands, and Hooks

As the plugin grows, it can include:

- **Agents** (`agents/`): autonomous specialists dispatched as subagents
- **Commands** (`commands/`): user-facing slash commands
- **Hooks** (`hooks/`): event-driven automation (PreToolUse, PostToolUse, Stop)

See the [Claude Code plugin documentation](https://docs.anthropic.com/en/docs/claude-code/plugins) for details on these component types.

## Keeping Assessment Content in Sync

The PELA content in `skills/platform-literacy-assessment/references/` is
derived from the canonical assessment document in the
[platform-engineering-literacy](https://github.com/russmiles/platform-engineering-literacy)
framework repository at `framework/assessment/platform-literacy-assessment.md`.

When the canonical document changes:
1. Extract the updated sections into the corresponding reference files
2. Update the PELA instrument version in `SKILL.md` if rubric descriptors changed
3. Bump the plugin version in `plugin.json`
4. Update `CHANGELOG.md`

## Pull Request Process

1. Create a branch from `main`
2. Make your changes
3. Update `CHANGELOG.md`
4. Open a PR with a clear description
5. Wait for review
