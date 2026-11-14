# Shared GitHub standards

Account-wide community guidance, issue and pull request templates, inherited
Renovate configuration and reusable security utilities for `edithatogo`.

## Usage

The shared package includes bug, feature and documentation issue forms, an issue
chooser, a pull request template, and contribution, conduct, security and support
guidance. Start with [Support](SUPPORT.md), [Contributing](CONTRIBUTING.md),
[Security](SECURITY.md) or the [Code of conduct](CODE_OF_CONDUCT.md).

GitHub supplies supported community files to this account's repositories when
they do not define their own. A receiving repository's valid issue template or
issue chooser configuration overrides the entire inherited issue-template
directory. Local customisations therefore need to preserve all wanted forms.
Inherited defaults are displayed by GitHub but are not copied into clones.
See [GitHub's default community-file rules](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file).

## Repository-specific adoption

Workflow files, `AGENTS.md`, editor configuration and development environments
require explicit repository-local adoption. Their presence here does not make
them inherited community files or activate a hosted provider. Private security
reporting and Discussions also require their own repository settings.

Reusable CI/CD workflows, the community/bootstrap contract and archetype starter
repositories are maintained through
[`repository-standards`](https://github.com/edithatogo/repository-standards).
Use that repository's validation guidance when changing the shared contract.

This is a solo-maintainer estate: stable automated checks and evidence govern
integration, with no mandatory second-person or CODEOWNERS approval.

## Development and validation

Clone this repository to edit the shared files. Keep form field IDs unique and
use synthetic examples. The canonical validator lives in `repository-standards`;
set up its documented Python environment and run the audit from that checkout:

```sh
.venv/bin/python scripts/audit_community_bootstrap.py \
  --repository-dir ../.github \
  --metadata observed-settings.json
```

Replace the repository path with your local checkout location. Supply
`observed-settings.json` using the validator's documented metadata fields and
the actual current repository settings. The audit requires explicit observations
for settings such as Discussions and template status; unknown settings are not
successful verification. It checks local file structure and guidance, not live
provider activation or delivery of a security report.

Run `git diff --check` in this checkout and include the audit result and any
unavailable checks in the PR. Changes to the Python security utility also need
the relevant executable checks documented by its owning standards workstream.

## Security

Use [SECURITY.md](SECURITY.md) to find the affected repository's private reporting
route. The presence of this policy does not enable private vulnerability
reporting. Keep vulnerability details, credentials and personal data out of
public issues and validation output.

## Rights and citation

This repository currently has no `LICENSE` file recording a repository-wide
reuse licence. Do not infer such a licence from a linked project or from the
repository's public visibility. Third-party material remains subject to its own
terms; record provenance when adding or adapting it. A licence decision remains
with the repository owner.

Use the existing [CITATION.cff](CITATION.cff) when citing this repository. Its
metadata does not establish a licence or imply a DOI deposit.
