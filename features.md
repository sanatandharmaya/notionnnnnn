# Feature catalogue

The following are **planned** features, grouped by owner and consuming application. They are not implemented. Source references resolve in [key sources](reports/key-sources.md). Release placements follow K07 and may need detailed specification reconciliation.

| ID | Domain / app | Supported behavior and roles | Rules, dependencies and acceptance | Scope / sources |
| --- | --- | --- | --- | --- |
| FEAT-001 | Foundation / admin, API, website | Admin/staff sign in to scoped operations; public website has a running shell. | REQ-001/002/005/015; deny without capability; audit privileged mutations; clean build and tests. | R0; K05, K08 |
| FEAT-002 | Editorial / admin, API | Staff author, review, translate and publish a versioned content record. | REQ-003/004/011/012; reviewer/rights gates; published projection updates and withdrawal removes visibility. | R1; K04 §11, K07 R1 |
| FEAT-003 | Knowledge / website, API | Reader discovers and reads published C01/C02 content by locale. | REQ-003/006/011/013; no private or unpublished fields; source and language distinctions survive. | R1; K07 R1 |
| FEAT-004 | Discovery / website, API | Reader uses lexical/faceted search across authorized public projections. | REQ-008/012/014; deterministic ranking, exclusions and owner-sourced index updates. | R2; K06 Search, K07 R2 |
| FEAT-005 | Account / website, API | Devotee manages own profile, bookmarks, notes, progress and preferences. | REQ-005/007/012; session-derived `me`, no cross-account disclosure or implicit family sharing. | R3; K05 D1-11/13, K07 R3 |
| FEAT-006 | Commerce / admin, website, API | Devotee views entitlements and completes approved purchase/donation journeys; staff reconcile outcomes. | REQ-009/012/014; provider callbacks idempotent, payment does not grant staff access. | R4; K07 R4 |
| FEAT-007 | Events/live / admin, website, API | Staff schedule events/streams; users register or view according to mode. | REQ-010/012/014; capacity and ticket mode enforced by owner; platform metadata distinct from YouTube execution. | R5; K07 R5 |
| FEAT-008 | API/integration / API | Owner-specific operations and later governed external webhooks. | REQ-002/014/015/017; versioned contracts, scoped credentials, revision/idempotency checks, P06 logical completeness and no duplicate owner store. | R0 internal foundation; R6 external expansion; K05 D1-05/08, K07, K18–K20 |

The [C01–C37 category notes](docs/categories/README.md) now link 37 source feature indexes containing 758 category-scoped IDs/names and source lines. Those indexes preserve the source inventory but do not merge child specifications, assign global `FEAT-*` IDs, or establish release approval. Do not treat this table as their substitute.
