# mente-worker-sandbox

Throwaway repo for the MEN-118 live Mac-worker E2E run.
The paired worker opens PRs here (never against mente/mente-ios).

## Architecture

The app is organized into four top-level layers, each with a clear responsibility. This keeps feature code isolated from shared infrastructure and makes it easy to reason about dependencies (App depends on Features, which depend on Core and DesignSystem).

- **App entry** — launch, lifecycle, and root composition; wires the other layers together.
- **Core** — shared domain models, services, networking, and utilities used across features.
- **Features** — user-facing feature modules; each owns its screens, view models, and feature-local logic.
- **DesignSystem** — reusable UI primitives, tokens, and styling shared by all features.
