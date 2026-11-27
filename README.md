# Grumo Templates

This repository intentionally contains a single supported scaffold: `default/`.

The default scaffold is the canary for the current public Grumo experience. It should stay small, stable, and aligned with the recommended Store-first runtime path.

## Policy

- `default/` uses only stable, recommended Grumo APIs.
- Fresh scaffolds target the current 3.2 compatibility line (`>=2.0.0,<3.0.0`);
  the generated project's lockfile owns reproducibility after creation.
- Grumo Store is the default durable application infrastructure (`.grumo/application.grumo`).
- SQLite/PostgreSQL/Redis/S3 remain explicit adapters, not scaffold defaults.
- Specialized templates (agents, MCP, Edge, showcases, etc.) are intentionally deferred until their public APIs are stable enough to support as long-lived scaffolds.

A Grumo release should not be considered healthy if a fresh `default/` project cannot install, start, create its Runtime Store, stop, and restart successfully.
