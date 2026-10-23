# Prepared draft pull request

**Title:** Document Eternal Sanskriti architecture and source audit (provisional)

**Base:** `main`

**Head:** `docs/eternal-sanskriti-knowledge`

**Historical status:** This prepared text predates [PR #1](https://github.com/sanatandharmaya/notionnnnnn/pull/1), which was subsequently merged into `main`. It is retained as a record of the earlier proposed draft. Continuing work is on `docs/eternal-sanskriti-reconciliation`; prepare a fresh draft PR from its actual diff. The historical `gh pr create --draft` attempt returned `Post "https://api.github.com/graphql": Forbidden` on 2026-10-23 UTC.

## Scope

Creates the requested documentation baseline for the admin panel, public website and API; records the user-confirmed Sanatan Platform replacement root; inventories 5,479 export entries, current C01–C37 categories, 758 source feature identifiers, exact-file duplicates and key conflicts. No application code or configuration is scaffolded.

## Coverage and validation

All 5,478 exported text entries were decoded and scanned line by line (2,093,941 lines). This was not complete semantic review. Current counts are in [reading coverage](reading-coverage.md) and [progress](progress.md). All 19 root documents, 37 category notes and 37 category audit maps existed at this stage. Local Markdown targets, planning ID references and staged whitespace checks passed; application tests did not apply.

## Decisions and blockers

Current category numbering and D1 scoped authorization take precedence over legacy combined C04 and automatic ADMIN bypass. The user's repository and `apps/website` name supersede historical paths. D2–D6 logical decisions further define contract, privacy, computation and verification boundaries. This is a provisional draft: detailed child requirements, legacy source mapping, rights/policy gates and physical contracts must be reconciled before implementation readiness. See [conflicts](conflict-register.md) and [unresolved gaps](unresolved-gaps.md).
