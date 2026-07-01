# Architecture inventory

Audit snapshot of the repository as of ticket `tk-7bd93c7d-2fcb-4ef7-82fc-3f62b16508c0-t1`.

## Repository purpose

Per `README.md`, this is a throwaway sandbox repo used for the MEN-118 live
Mac-worker E2E run. Pull requests opened by the paired Mente worker land here
rather than against `mente/mente-ios`.

## Major architectural components

The repository currently contains **no application code, build system, or
runtime components**. There is nothing to inventory beyond repository metadata
and documentation:

| Component | Path | Purpose |
| --- | --- | --- |
| Repo overview | `README.md` | Describes the sandbox purpose |
| Architecture inventory | `ARCHITECTURE.md` | This file |
| Git metadata | `.git/` | Version control |

No source directories, package manifests (`package.json`, `pyproject.toml`,
`Cargo.toml`, `go.mod`, `Gemfile`, etc.), CI configuration, or test suites are
present on `main`.

## Branches observed at audit time

- `main` — baseline, contains only `README.md`.
- `mente/men118-smoke-1` — adds `CONTRIBUTING.md` (contribution guide).
- `mente/men137-e2e-1` — adds `HELLO-men137.md` (single-line greeting).

These branches represent prior worker smoke/E2E runs; they are not merged into
`main` and do not contribute application components.

## Implications

Any future ticket that references "existing modules" in this repo should treat
the codebase as empty and create rather than extend. Once real code lands,
this file should be updated to enumerate the actual components.
