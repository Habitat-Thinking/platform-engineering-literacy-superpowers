# AI Literacy Assessment — 2026-04-10

## Header

- **Project**: Platform Engineering Literacy Superpowers
- **Date**: 2026-04-10
- **Assessor**: Claude Opus 4.6 (via /assess)
- **Assessed level**: L2 — Verification
- **Project type**: Content-only Claude Code plugin (no executable code)

## Observable Evidence

### Found

| Signal | File/Path | Level |
| --- | --- | --- |
| Repository with AI config | `.claude/settings.local.json` (27 permission rules) | L0-1 |
| 3 CI workflows | `.github/workflows/lint-markdown.yml`, `harness.yml`, `auto-enforcer.yml` | L2 |
| Markdownlint in CI | `.github/workflows/lint-markdown.yml` with pinned SHA | L2 |
| Secret scanning (gitleaks) | `.github/workflows/harness.yml` — gitleaks v8.30.1 | L2 |
| Agent-based PR review | `.github/workflows/auto-enforcer.yml` — parses HARNESS.md, calls Claude API | L2-3 |
| Pinned action SHAs | All 3 workflows use SHA-pinned checkout and action references | L2 |
| HARNESS.md | `HARNESS.md` — 8 constraints, 6 GC rules, status section | L3 |
| REFLECTION_LOG.md | `REFLECTION_LOG.md` — 1 entry (2026-04-10, signal: failure) | L3 |
| Health snapshot | `observability/snapshots/2026-04-10-snapshot.md` | L3 |
| Copilot instructions | `.github/copilot-instructions.md` — convention sync | L3 |
| Copilot prompt file | `.github/prompts/platform-literacy-assessment.prompt.md` | L3 |
| Markdownlint config | `.markdownlint.json` (MD013, MD024, MD025 disabled) | L3 |
| Reusable plugin | `platform-engineering-literacy-superpowers/.claude-plugin/plugin.json` v0.2.0 | L5 |
| Plugin skill | `skills/platform-literacy-assessment/SKILL.md` + 4 reference files | L5 |
| CONTRIBUTING.md | `CONTRIBUTING.md` — repo structure, PR process, skill conventions | L3 |
| CHANGELOG.md | `CHANGELOG.md` — maintained | L3 |
| README badges | 8 badges (license, version, CI status, harness, health) | L3 |

### Not Found

| Signal | Level | Notes |
| --- | --- | --- |
| Project-level CLAUDE.md | L3 | Global `~/.claude/CLAUDE.md` exists but no repo-level context engineering |
| AGENTS.md | L3 | No compound learning document |
| MODEL_ROUTING.md | L3 | No model-tier routing guidance |
| `.claude/skills/` | L3 | Skills are in plugin structure, not project-local |
| `.claude/agents/` | L3 | No custom agent definitions |
| `.claude/commands/` | L3 | No custom commands |
| Hooks configuration | L3 | No edit-time hooks (PreToolUse/PostToolUse) |
| GC ever run | L3 | 6 rules declared, 0 executed |
| `specs/` directory | L4 | No specification files |
| Implementation plans | L4 | No plan.md or plan-*.md files |
| Orchestrator pipeline | L4 | No orchestrator agent |
| Loop guardrails | L4 | No MAX_REVIEW_CYCLES or similar |
| Cross-team templates | L5 | No reusable harness templates |
| OpenTelemetry | L5 | No observability instrumentation |
| Org governance | L5 | No governance documentation |

## Clarifying Responses

1. **Verification**: Systematic — always reviews diffs, runs lint/tests before accepting AI output
2. **Cost awareness**: Not tracking yet — unknown monthly spend
3. **Spec discipline**: Writes specs and design documents, usually collaboratively with the agent
4. **Session workflow**: Starts fresh each session — no consistent checklist or review of prior state
5. **Team**: Solo developer. No other repos consume or contribute to these harness conventions yet

## Level Assessment

### Assessed level: L2 — Verification

The project has strong L3 infrastructure (HARNESS.md with 8 enforced constraints, auto-enforcer CI, reflection log, health snapshot) but is assessed at L2 because:

1. **Guardrail design is the ceiling**: No spec-first artifacts in the repo, no orchestrator pipeline, no loop guardrails. Specs are written collaboratively but not persisted as repo artifacts.
2. **L3 infrastructure is built but not operational**: GC rules have never run, only 1 reflection entry, no AGENTS.md for compound learning, no CLAUDE.md for session context.
3. **Missing compound learning loop**: REFLECTION_LOG has 1 entry but no AGENTS.md to promote learnings into. The learning cycle (reflect, curate, benefit) is incomplete.

The team is on the **threshold of L3**. The infrastructure investment is significant — activating what exists will close most gaps.

## Discipline Maturity

| Discipline | Level | Rationale |
| --- | --- | --- |
| Context engineering | L2-3 | HARNESS.md conventions are well-written and enforceable. Copilot instructions synced. But no CLAUDE.md for LLM session context, no AGENTS.md for accumulated knowledge. |
| Architectural constraints | L3 | 8 constraints with clear enforcement taxonomy. Auto-enforcer runs agent constraints via Claude API. Deterministic tools (markdownlint, gitleaks) working in CI. GC declared but never run. |
| Guardrail design | L2 | 3 CI workflows with pinned SHAs. Advisory agent comments on PRs. But no spec-first workflow in repo artifacts, no orchestrator, no edit-time hooks. |

## Strengths

1. **Constraint taxonomy**: Clean separation of deterministic vs agent enforcement, with a data-driven auto-enforcer that reads HARNESS.md at runtime
2. **Supply chain security**: All CI actions pinned by SHA, gitleaks scanning, no secrets in source
3. **Convention documentation**: HARNESS.md, copilot-instructions.md, and CONTRIBUTING.md provide overlapping coverage for humans and AI tools
4. **Observability foundation**: Health snapshot, README badges, and status section create visibility into harness health
5. **Plugin as product**: The repo itself is a reusable Claude Code plugin — a L5 signal for the plugin's consumers

## Gaps

1. **No project-level CLAUDE.md**: LLM sessions start without repo-specific context engineering
2. **No AGENTS.md**: No compound learning document to accumulate gotchas, style decisions, and architectural patterns
3. **No MODEL_ROUTING.md**: No guidance on model-tier selection or cost awareness
4. **GC never run**: 6 rules declared but entropy has never been checked
5. **No edit-time hooks**: Constraints enforce at PR time only — no inner-loop advisory feedback
6. **No spec artifacts**: Specs are written conversationally but not persisted as repo artifacts
7. **Sessions start fresh**: No consistent workflow to review prior state or REFLECTION_LOG

## Recommendations

1. **Create a project-level CLAUDE.md** pointing to HARNESS.md conventions and defining session start habits — this alone closes the biggest L3 gap
2. **Create AGENTS.md** with the gotcha from the reflection log (bash IFS limitations) and any architectural decisions — activates compound learning
3. **Run `/harness-gc` once** to activate garbage collection and establish the outer loop
4. **Add a session-start habit** to CLAUDE.md: review REFLECTION_LOG and HARNESS.md status before starting work
5. **Create MODEL_ROUTING.md** with at minimum the auto-enforcer's model choice (claude-opus-4-5) and cost tracking intent

## Immediate Adjustments Applied

- No stale counts to fix — HARNESS.md status and README badges were current
- AI Literacy badge added to README (L2, blue)

## Workflow Operation Changes

| Recommendation | Status | What Changed |
| --- | --- | --- |
| Create project-level CLAUDE.md | **Accepted** | Created `CLAUDE.md` with conventions, session-start habits, enforcement summary, and quarterly/monthly cadences |
| Create AGENTS.md | **Accepted** | Created `AGENTS.md` with 3 gotchas and 2 architectural decisions promoted from this session |
| Run /harness-gc | **Accepted** | Recorded as follow-up — requires separate GC agent dispatch |
| Create MODEL_ROUTING.md | **Accepted** | Created `MODEL_ROUTING.md` with agent routing table, cost tracking placeholder, and routing principles |

## Reflection

The gap between infrastructure and operations was the dominant finding. The project has strong L3 tooling (HARNESS.md, auto-enforcer, health snapshots) but lacked the three files that make compound learning work: CLAUDE.md (session context), AGENTS.md (accumulated knowledge), and MODEL_ROUTING.md (cost awareness). All three were created during this assessment. The next assessment should verify whether the operational cadences (monthly reflect, quarterly audit) are actually being followed — that's the difference between L2 and L3.

## Next Assessment Date

Suggested: 2026-07-10 (quarterly)
