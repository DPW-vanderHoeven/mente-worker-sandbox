# Architecture

This is the single, global architecture document for the
`mente-worker-sandbox` repository. It describes what this repository is,
what it contains today, and how the pieces relate to the wider Mente
system. Update this file whenever a component is added, removed, or
significantly restructured — do not create parallel architecture
documents elsewhere in the tree.

## Repository role

`mente-worker-sandbox` is a throwaway sandbox used by the Mente Mac
worker for end-to-end and smoke runs (originally the MEN-118 live run).
It is deliberately separate from `mente/mente-ios`: the paired worker
opens pull requests here so that experimental automation cannot touch
the production iOS repository.

Because the repository is a sandbox, its "architecture" is intentionally
minimal. Nothing here is shipped to end users. Anything you see in this
tree exists to exercise the worker, capture policy, or document how the
sandbox itself is meant to be used.

## Current contents

The repository currently contains no application source, build system,
package manifests, or runtime configuration. Every top-level file is a
policy or process document:

| Path              | Kind              | Purpose                                                                 |
| ----------------- | ----------------- | ----------------------------------------------------------------------- |
| `README.md`       | Overview          | Names the repo, states its sandbox role, and links to the docs below.   |
| `CONTRIBUTING.md` | Process           | Explains how to contribute and how to route security-sensitive changes. |
| `SECURITY.md`     | Policy            | Private vulnerability reporting channel, response SLAs, safe harbor.    |
| `ARCHITECTURE.md` | This document     | Global architecture and conventions for the sandbox.                    |
| `.git/`           | Version control   | Git metadata; worker branches and PRs land here.                        |

There is intentionally no `package.json`, `pyproject.toml`, `Cargo.toml`,
`go.mod`, `Gemfile`, CI workflow, or test suite. If you were sent here
to "extend an existing module", there is no module to extend — the
codebase is empty by design.

## How the pieces fit together

The three process documents form a small hub-and-spoke graph:

- `README.md` is the entry point. It links to `SECURITY.md` for
  vulnerability handling and to `CONTRIBUTING.md` for change
  management.
- `CONTRIBUTING.md` cross-links back to `SECURITY.md` so that anyone
  landing on the contribution guide first is still routed through the
  private channel for security issues.
- `SECURITY.md` is the authoritative source for the reporting channel
  and disclosure timeline; other documents defer to it rather than
  restating policy.
- `ARCHITECTURE.md` (this file) is the authoritative source for what
  the repository contains and how it is organised. Other documents
  should link here rather than duplicating structural claims.

## External interactions

The sandbox exists to be driven from outside. Two external actors are
in scope:

- **The Mente Mac worker.** Runs on a developer machine and opens pull
  requests on branches named `mente/<ticket-or-run-id>`. Each branch
  represents one ticket or smoke/E2E run. Branches are not expected to
  be merged into `main` unless a ticket explicitly targets `main`.
- **Human reviewers and security reporters.** Reviewers land through
  GitHub PRs; security reporters use the private advisory channel
  described in `SECURITY.md`.

There is no runtime, deployment target, or external service that this
repository talks to on its own.

## Branch and change conventions

- `main` is the baseline. It should only contain material that has been
  reviewed and merged through a PR.
- Worker branches use the `mente/tk-<uuid>-t<n>` (per-ticket) or
  `mente/<run-id>` (per-run) naming pattern. They are ephemeral and
  should not be treated as authoritative.
- Test artefacts created inside a ticket must be prefixed with that
  ticket's identifier so that stray files can be traced back to the run
  that produced them.
- Keep changes minimal and scoped to a single concern, as noted in
  `CONTRIBUTING.md`.

## Keeping this document accurate

Because the sandbox is small, this document is expected to stay short.
When you land a change that adds, removes, or renames a top-level
component:

1. Update the "Current contents" table in the same PR.
2. Update the "How the pieces fit together" section if cross-links
   change.
3. If real application code ever lands, replace the "no application
   source" statement with a description of the actual components rather
   than starting a second architecture document elsewhere.
