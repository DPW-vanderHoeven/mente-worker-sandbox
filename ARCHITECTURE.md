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

### Verified absent

Confirmed missing across `main`, this branch, and both prior worker branches
(`mente/men118-smoke-1`, `mente/men137-e2e-1`) via `git cat-file -e`:

- Source directories (no `src/`, `app/`, `lib/`, `pkg/`, etc.).
- Package manifests: `package.json`, `pyproject.toml`, `Cargo.toml`, `go.mod`,
  `Gemfile`, `pom.xml`, `build.gradle`, `Package.swift`.
- Build/runtime config: `Makefile`, `Dockerfile`, `docker-compose.yml`.
- CI: no `.github/workflows/`, no `.circleci/`, no `.gitlab-ci.yml`.
- Repo governance: no `LICENSE`, `CODEOWNERS`, `.gitignore`, `.gitattributes`.
- Tests: no test suites, fixtures, or runners.

## Branches observed at audit time

- `main` — baseline, contains only `README.md`.
- `mente/men118-smoke-1` — adds `CONTRIBUTING.md` (contribution guide).
- `mente/men137-e2e-1` — adds `HELLO-men137.md` (worker greeting).
- `mente/tk-7bd93c7d-2fcb-4ef7-82fc-3f62b16508c0-t1` — this branch; adds
  `ARCHITECTURE.md` (the audit itself).

The sibling `mente/*` branches represent prior worker smoke/E2E runs; none are
merged into `main`, and none contribute application components.

## Implications

Any future ticket that references "existing modules" in this repo should treat
the codebase as empty and create rather than extend. Once real code lands,
this file should be updated to enumerate the actual components.
