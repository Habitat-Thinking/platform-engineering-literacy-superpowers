# Project Conventions

## Platform Engineering Literacy Assessment

This is a Claude Code plugin that provides the Platform Engineering
Literacy Assessment (PELA). The primary artefacts are Markdown files
that define the assessment protocol and reference content.

## Content Conventions

- **Voice**: Authoritative but accessible — write for practising
  platform engineers, not academics
- **Structure**: The PELA skill is in `skills/platform-literacy-assessment/`,
  with reference content in `references/`
- **Naming**: Skills use `SKILL.md` inside a named directory. All
  directory names are lowercase kebab-case.
- **Format**: Markdown for all content. YAML frontmatter on skill files
  with `name` and `description` fields.

## Plugin Structure

- `skills/` — assessment skills with `SKILL.md` and optional `references/`
- `.claude-plugin/plugin.json` — plugin manifest

## Workflow

- **Branch discipline**: never commit to main
- **Commit messages**: concise, what and why, no postamble
- **CHANGELOG**: update before every PR
