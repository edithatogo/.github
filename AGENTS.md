# AGENTS.md

This account's repositories are maintained by one developer. Prefer automated tests, security checks, and reproducible evidence over mandatory human approval.

Repository defaults:
- no required reviewer, CODEOWNERS approval, team assignment, or second-person gate;
- use focused pull requests and require stable automated checks;
- keep workflows read-only by default and grant writes per job;
- pin actions to immutable commits and update dependencies with Renovate;
- use Codecov OIDC only where executable tests produce real coverage;
- never commit credentials or sensitive data.

Project-specific AGENTS.md files override these defaults only where they explicitly say so.