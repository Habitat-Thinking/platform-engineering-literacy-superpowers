# Platform Engineering Literacy Superpowers

[![Harness](https://img.shields.io/badge/Harness-7%2F7_enforced-808080?style=flat-square)](HARNESS.md)
[![Agent Harness Enabled](https://img.shields.io/badge/Agent_Harness-Enabled-000000?style=flat-square)](HARNESS.md)
[![Harness Health](https://img.shields.io/badge/Health-Attention-F5A623?style=flat-square)](observability/snapshots/2026-04-10-snapshot.md)

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) plugin that provides the **Platform Engineering Literacy Assessment (PELA)** — a three-phase assessment protocol for determining literacy levels across six dimensions of platform engineering practice.

## What is the PELA?

The PELA measures your platform engineering literacy across six dimensions:

1. **Context Awareness** — can you see the system?
2. **Cognitive Load Design** — can you design for developer flow?
3. **Pattern Application** — can you apply the Platform Pattern Language?
4. **Feedback and Measurement** — can you build learning loops?
5. **Strategic Thinking** — can you navigate technology evolution?
6. **Human and Cultural Dimensions** — can you navigate adoption and culture?

Each dimension is assessed across five levels (0–4), from **Aware** to **Steward**. The assessment uses three phases:

- **Quick Scan** — structured self-rating across all six dimensions (~15 min)
- **Guided Exploration** — conversational probing of interesting signals (~20 min)
- **Deep Dive** (optional) — scenario-based or evidence-based validation

The output is a layered developmental profile: headline level, dimensional breakdown, and a development roadmap with specific course modules and fluency habits.

## Installation

```bash
claude plugin add Habitat-Thinking/platform-engineering-literacy-superpowers/platform-engineering-literacy-superpowers
```

## Usage

Run the assessment with:

```text
/platform-literacy-assessment
```

Or ask naturally:

- "Run a PELA"
- "Assess my platform engineering literacy"
- "Where am I on the framework?"
- "Check my level"

The skill supports **individual**, **instructor-led**, and **team** assessments.

## Repository Structure

This repo uses a multi-plugin layout. Each plugin lives in its own
subdirectory with a self-contained `.claude-plugin/plugin.json` and
component directories:

```text
platform-engineering-literacy-superpowers/   # Plugin: PELA skill
├── .claude-plugin/
│   └── plugin.json
└── skills/
    └── platform-literacy-assessment/
        ├── SKILL.md
        └── references/
```

Future plugins can be added as sibling directories at the repo root.

## The Framework

This plugin is part of the [Platform Engineering Literacy](https://github.com/russmiles/platform-engineering-literacy) framework. The framework includes:

- A comprehensive literacy model (5 levels, 6 dimensions)
- 20 teaching modules with Le Bon Mot narratives
- 10 Platform Patterns
- 15 fluency habits
- A standalone pen-and-paper assessment document

The plugin packages the assessment as a portable, interactive experience that works in any project.

## License

Apache 2.0 — see [LICENSE](LICENSE).
