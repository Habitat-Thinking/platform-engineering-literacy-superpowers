# Project Rules — Platform Engineering Literacy Superpowers

## What This Project Is

A Claude Code plugin providing the Platform Engineering Literacy Assessment (PELA) — a three-phase assessment protocol for determining literacy levels across six dimensions of platform engineering practice. This is a **content-only** project: no executable code, only Markdown skills and references.

## Session Start

At the start of every session:

1. Read `HARNESS.md` Status section — check constraint health and drift
2. Read `REFLECTION_LOG.md` — review recent surprises and proposals
3. Check `AGENTS.md` — review gotchas and architectural decisions

## Conventions

All conventions are defined in `HARNESS.md` Context section. Key rules:

- **Naming**: lowercase kebab-case directories, `SKILL.md` in named directories, YAML frontmatter with `name` and `description`
- **File structure**: multi-plugin layout, skills in `skills/<name>/SKILL.md`, optional `references/` subdirectory
- **Content integrity**: internal links must resolve, YAML frontmatter must be valid
- **Documentation**: authoritative but accessible voice, CHANGELOG and README updated every PR, markdown must pass linting

## Branch Discipline

Never commit directly to `main`. Create a feature branch for every change. Update CHANGELOG.md in every PR.

## Enforcement

Constraints are declared in `HARNESS.md` and enforced by:

- `lint-markdown.yml` — markdownlint on all Markdown files
- `harness.yml` — gitleaks secret scanning
- `auto-enforcer.yml` — agent-based PR review for content quality constraints

## Quarterly Cadence

- `/harness-audit` — verify enforcement matches reality
- `/assess` — AI literacy assessment
- `/harness-health` — generate health snapshot

## Monthly Cadence

- `/reflect` — capture session learnings
- `/harness-gc` — run garbage collection rules
