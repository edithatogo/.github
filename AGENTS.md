# AGENTS.md

## Operating model

This account's repositories are maintained by one developer. Prefer automated tests, security checks, and reproducible evidence over mandatory human approval.

Repository defaults:
- no required reviewer, CODEOWNERS approval, team assignment, or second-person gate;
- use focused pull requests and require stable automated checks;
- keep workflows read-only by default and grant writes per job;
- pin actions to immutable commits and update dependencies with Renovate;
- use Codecov OIDC only where executable tests produce real coverage;
- never commit credentials or sensitive data.

## Validation

Read the receiving repository's README, contribution guidance and Conductor
workflow to identify its actual setup, validation commands and qualified
runtime. Run the checks appropriate to the change and report exact commands,
results, skips and unavailable capabilities. Do not invent a universal test
command or treat a configured workflow as evidence that it executed.

When changing shared community/bootstrap material, also use
`scripts/audit_community_bootstrap.py` in
[`repository-standards`](https://github.com/edithatogo/repository-standards).
Its README documents setup and the audit command. Pass the relevant checkout
and actual observed settings; distinguish local files from inherited defaults.
The source audit supplements the project's required hosted checks.

## Boundaries

Preserve repository-specific instructions and unrelated work. Keep examples
synthetic and generated material reproducible. Do not activate providers,
publish data or releases, or change credentials merely because a source check
passes. Use the affected repository's security policy for private reporting.

Project-specific AGENTS.md files override these defaults only where they explicitly say so.
