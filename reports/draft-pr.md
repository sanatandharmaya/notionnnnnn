# Prepared draft pull request

**Title:** Document Eternal Sanskriti architecture and source audit (provisional)

**Base:** `main`

**Head:** `docs/eternal-sanskriti-knowledge`

**Status:** Not opened. `gh pr create --draft` returned `Post "https://api.github.com/graphql": Forbidden` on 2026-10-23 UTC; direct API access also returned a 403 tunnel error. Git push succeeded. A compare URL is available: https://github.com/sanatandharmaya/notionnnnnn/compare/main...docs/eternal-sanskriti-knowledge?expand=1

## Scope

Creates the requested documentation baseline for the admin panel, public website and API; records the user-confirmed Sanatan Platform replacement root; inventories 5,479 export entries, current C01–C37 categories, 758 source feature identifiers, exact-file duplicates and key conflicts. No application code or configuration is scaffolded.

## Coverage and validation

All 5,478 exported text entries were decoded and scanned line by line (2,093,941 lines). This is not complete semantic review: 14 core pages have a first detailed reading, 11 are partial, 37 category registries are structurally indexed, and 5,417 entries remain pending. See [reading coverage](reading-coverage.md) and [progress](progress.md). All 19 root documents, 37 category notes and 37 category audit maps exist. Local Markdown targets, planning ID references and staged whitespace checks passed; application tests do not apply.

## Decisions and blockers

Current category numbering and D1 scoped authorization take precedence over legacy combined C04 and automatic ADMIN bypass. The user's repository and `apps/website` name supersede historical paths. D2–D6 logical decisions further define contract, privacy, computation and verification boundaries. This is a provisional draft: detailed child requirements, legacy source mapping, rights/policy gates and physical contracts must be reconciled before implementation readiness. See [conflicts](conflict-register.md) and [unresolved gaps](unresolved-gaps.md).
