# Model Routing — Platform Engineering Literacy Superpowers

## Agent Routing

| Agent / Use Case | Model | Tier | Rationale |
| --- | --- | --- | --- |
| Auto-enforcer (CI agent constraints) | claude-opus-4-5 | High | PR constraint review needs strong reasoning for nuanced content rules |
| Interactive development (Claude Code) | claude-opus-4-6 | High | Primary development tool for plugin authoring |

## Cost Tracking

- **Last cost capture**: never
- **Monthly average**: not tracked
- **Budget**: not set

Run `/cost-capture` quarterly to record spend and update this section.

## Routing Principles

1. **Content review needs strong reasoning**: Agent constraints evaluate whether content meets quality standards (frontmatter validity, link integrity, naming conventions). Use high-tier models for accuracy.
2. **Cost awareness is a habit, not a gate**: Start by tracking, then optimise. Don't downgrade models before understanding where quality matters.
3. **Reassess quarterly**: Review whether the auto-enforcer model could be downgraded to Sonnet for simpler constraints (e.g. CHANGELOG presence) while keeping Opus for nuanced ones (e.g. content quality).
