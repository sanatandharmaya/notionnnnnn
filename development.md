# Development workflow

This repository currently contains documentation only. There are no package manifests, lockfiles, application commands or application tests. Do not run or claim `install`, `dev`, `build` or `test` for an application until implementation creates and verifies them.

The source-approved future baseline is pnpm workspace, Turborepo, strict TypeScript, Payload CMS v3, Next.js and PostgreSQL. Exact compatible versions, scripts, auth package, deployment provider and physical schema are implementation choices. [K06]

Documentation workflow: read [goal](goal.md), [coverage](reports/reading-coverage.md) and [progress](reports/progress.md); resolve the source IDs through [file register](reports/source-files.csv); update requirement/feature/decision/category reports with export paths and line or heading citations; run link/ID/traceability checks before committing. Preserve user work and original exports. [K02 governance; user brief]

The default branch was initialized with a README-only commit. Continue documentation on `docs/eternal-sanskriti-knowledge`; application scaffolding belongs to a later coding task.
