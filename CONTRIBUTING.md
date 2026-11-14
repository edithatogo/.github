# Contributing

This is the shared contribution guide for the `edithatogo` repositories that
inherit it. Read the receiving repository's README, `AGENTS.md` and any local
contribution instructions for its actual commands, scope and ownership rules.

## Getting started

1. Read the project purpose, maintenance status, licence and supported versions.
   Search existing issues, pull requests and Conductor tracks for related work.
2. For a substantial feature or behaviour change, describe the problem and
   proposed acceptance criteria in the relevant issue before implementing it.
   Small corrections can be submitted directly as a focused pull request.
3. Fork or clone the repository and create a branch for the change. Use a
   descriptive name such as `fix/parser-error`, `feat/export-format` or
   `docs/setup-example`, following local conventions when present.
4. Install the toolchain and dependencies using the repository's documented
   setup and lockfiles. Keep development environments isolated; never add local
   credentials or private data to the repository.

## Development

- Follow the surrounding code style and the repository's formatter/linter.
- Preserve public interfaces and data contracts unless the issue explicitly
  includes their migration. Explain any compatibility change in the PR.
- Add a focused regression test for a reproducible defect when executable
  behaviour changes. Keep fixtures synthetic or appropriately licensed.
- Update documentation and examples alongside changed behaviour. Regenerate
  derived files with their documented commands and retain source provenance.
- Use concise commit messages that explain the change. Follow the repository's
  established commit format; do not rewrite other contributors' history.

## Validation

Run the verification command documented by the receiving repository's README,
`CONTRIBUTING.md`, `AGENTS.md` or Conductor workflow. Commands and runtime versions
are project-specific; this shared guide does not prescribe one test runner for
every language. If the command is undocumented, report the missing instructions
and state which available checks you could run.

Before submitting, inspect the diff and check for whitespace errors:

```sh
git diff --check
git status --short
```

Record the exact validation commands, relevant toolchain versions and outcomes
in the PR. A skipped or unavailable check is not a pass. Explain failures and
remaining hosted, integration, data, credential or publication gates. Do not
attach secret values, private records or unredacted security logs as evidence.

## Pull requests

Use the PR template to explain the problem, resulting behaviour, linked work,
validation and compatibility implications. Keep unrelated changes separate and
preserve repository-specific extensions when adopting shared standards.

Required automated checks must pass before integration. These repositories use
a solo-maintainer model: no mandatory second human approval, CODEOWNERS approval
or team assignment is introduced. A successful test run does not authorise a
release, deployment, data publication or change to credentials.

Review feedback should address the code and evidence respectfully. Identify
which acceptance criteria are complete and which remain open; close an issue
only when its actual scope is satisfied.

## Security and conduct

Follow the [security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md)
for vulnerability reports and the
[code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md)
for community participation. For usage questions and maintenance expectations,
see [support](https://github.com/edithatogo/.github/blob/main/SUPPORT.md).
