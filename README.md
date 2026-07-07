# .github

Shared org-level GitHub Actions utilities for `edithatogo`.

## Code scanning gate

Reusable composite action:

- `.github/actions/code-scanning-gate`

It fails workflows when the current commit has open `high` or `critical`
code-scanning alerts.
