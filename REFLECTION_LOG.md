# Reflection Log

---

- **Date**: 2026-04-10
- **Agent**: Claude Opus 4.6
- **Task**: Initialized project harness (HARNESS.md, CI workflows, health snapshot, badges) and fixed all audit drift issues
- **Surprise**: The auto-enforcer template's `IFS='|||'` delimiter broke in bash because IFS treats each character individually, not as a multi-character string. This caused three CI debugging rounds. The markdownlint-cli2-action SHA was also truncated in the generated harness.yml, causing another failure. Both were template-level bugs invisible until CI ran.
- **Proposal**: Add AGENTS.md gotcha — generated CI workflows from templates need local validation before push. Bash IFS only supports single-character delimiters.
- **Improvement**: CI workflows generated from templates should be tested locally (e.g. with `act` or YAML validation) before committing, to catch environment issues before they hit GitHub Actions.
- **Signal**: failure
- **Constraint**: CI workflow validation on PR (agent)
