# Agents — Platform Engineering Literacy Superpowers

## Gotchas

GOTCHA: Bash `IFS` only supports single-character delimiters. `IFS='|||'` treats each `|` as a separate delimiter, not a three-character string. Use tab (`$'\t'`) or rewrite parsing in Python when passing structured data through shell pipes. Discovered 2026-04-10 when the auto-enforcer template corrupted tool commands.

GOTCHA: GitHub Actions do not resolve truncated commit SHAs for pinned actions. Always copy the full 40-character SHA from the source workflow or action release page. A truncated SHA causes "Unable to resolve action" failures at job setup time.

GOTCHA: Generated CI workflows from templates may reference tools (markdownlint-cli2, gitleaks) that are not installed in the runner environment. Always add explicit install steps or use dedicated GitHub Actions for each tool.

## Architectural Decisions

ARCH_DECISION: Deterministic constraints (markdownlint, gitleaks) are enforced by `harness.yml` using dedicated GitHub Actions steps. Agent constraints are enforced separately by `auto-enforcer.yml` using the Claude API. This split avoids the fragility of running tools from a generic bash loop in the auto-enforcer.

ARCH_DECISION: The auto-enforcer uses a single Python script for all agent constraint evaluation rather than piping through bash `while read` loops. This eliminates IFS delimiter bugs and shell variable escaping issues.
