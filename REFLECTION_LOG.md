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

---

- **Date**: 2026-04-10
- **Agent**: Claude Opus 4.6 (via /assess)
- **Task**: AI literacy assessment — Level 2 (Verification)
- **Surprise**: Strong L3 infrastructure (HARNESS.md, auto-enforcer, health snapshots) but assessed at L2 because the three compound learning files (CLAUDE.md, AGENTS.md, MODEL_ROUTING.md) were missing and GC had never run. The gap was between building and operating.
- **Proposal**: Add AGENTS.md session-start check to CLAUDE.md so accumulated knowledge is actually read. Recommend quarterly assessment cadence.
- **Improvement**: Future assessments should check not just whether files exist, but whether they've been read or updated recently (git blame dates on key files).
- **Signal**: context
- **Constraint**: none

---

- **Date**: 2026-04-10
- **Agent**: Claude Opus 4.6
- **Task**: Full harness lifecycle — init, health snapshot, audit, drift fixes, reflection, and AI literacy assessment with habitat adjustments
- **Surprise**: MD060 (table column style) caused repeated lint failures across every generated Markdown file with tables. Compact separators (`|---|---|`) are standard and widely used, but the rule demands spaced separators (`| --- | --- |`). The same fix was applied to 6+ files in a single session.
- **Proposal**: none (config fix applied directly)
- **Improvement**: Disable low-value lint rules proactively when they create systematic friction. MD060 was disabled in `.markdownlint.json` to prevent recurrence.
- **Signal**: failure
- **Constraint**: Disabled MD060 in .markdownlint.json (config fix, not a harness constraint)
