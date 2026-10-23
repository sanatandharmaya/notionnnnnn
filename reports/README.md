# Audit and source reports

The [source inventory](source-inventory.md), [per-file register](source-files.csv), [current category file map](current-category-sources.csv), [key source references](key-sources.md) and [reading coverage](reading-coverage.md) define what was supplied, mapped and reviewed. The [progress checkpoint](progress.md) records next actions; the [validation checkpoint](validation.md) records executed documentation checks.

| Audit concern | Report |
| --- | --- |
| Current domains and proposed Notion mirror | [Category map](category-map.md) |
| Per-category source maps and consolidation status | [Category reports](categories/README.md) |
| Exact file bytes and semantic duplicate findings | [Exact duplicate pairs](exact-duplicate-files.csv) · [Duplicate register](duplicate-register.md) |
| Contradictory source statements | [Conflict register](conflict-register.md) |
| Source → requirement → feature → decision → phase → task | [Requirement traceability](requirement-traceability.md) |
| Retained, merged and outstanding work | [Consolidation summary](consolidation-summary.md) · [Unresolved gaps](unresolved-gaps.md) |

The source ZIPs are not committed here. The CSV register provides page IDs, archive paths, hashes and review status; it does not contain raw source content.
