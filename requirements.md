# Canonical requirements

These IDs consolidate the currently reviewed core sources. They describe approved architecture or planned behavior, **not implemented code**. [Source keys](reports/key-sources.md) resolve page IDs and export paths. Full disposition of the 5,478 text entries remains pending in [reading coverage](reports/reading-coverage.md).

| ID | Requirement and material conditions | Status | Sources |
| --- | --- | --- | --- |
| REQ-001 | One monorepo contains admin, public website and API boundaries; this repository and `apps/website` are the user's target naming. | User confirmed; planned | User brief; K06 lines 17–52; CON-001 |
| REQ-002 | Each meaning/state has one owner; website and shared consumers use owner contracts rather than copies. | Approved logical rule | K02 lines 31–47; K04 §§3–4 |
| REQ-003 | Preserve M01 S01–S41, M02 W01–W09, M03 C01–C37, M04 X01–X25 as distinct namespaces; current C04/C05/C06 are Wellness/Ayurveda/Yoga. | Approved taxonomy | K03 lines 5–229; K09 |
| REQ-004 | Editorial publishing has revisioned draft, review, approval, publish, withdrawal and audit gates; translation, rights and safety review apply where required. | Approved logical behavior | K04 §11; K07 R1 |
| REQ-005 | Human identity is admin/devotee/staff; server authorization is deny by default, checks current scoped grants and resource/field access, and grants do not arise from type or payment tier. | Approved logical behavior | K05 D1-01/02/12 |
| REQ-006 | The website offers public discovery and reading through owner-backed projections; C01 and C02 form the first complete content slice. | Planned R1 | K04 §5; K07 R1 |
| REQ-007 | Progress, bookmarks, notes and preferences are private account state; sharing requires explicit scope and consent. | Approved logical boundary; planned R3 | K05 D1-11/13; K07 R3 |
| REQ-008 | Search is deterministic and authorization-aware; no generative/vector search is in current production scope. | Approved current direction; planned R2 | K06 lines 122–128; K05 D1-11 |
| REQ-009 | Subscription, payments, ecommerce and platform donations retain separate owners; provider execution and refund/reconciliation require evidence. | Approved ownership; planned R4 | K04 §4; K07 R4 |
| REQ-010 | Events and live services separate platform registration/scheduling from streaming execution; free, platform-paid and external ticket modes stay distinct. | Planned R5 | K07 R5; K06 lines 110–120 |
| REQ-011 | Canonical IDs are independent of labels/slugs/language; source, edition, locator and interpretation type remain explicit. Unknown provenance stays unknown. | Approved logical model | K04 §9; K11 ADR-005/006 |
| REQ-012 | Protect private fields, rights, consent, secrets and audit history across admin, API, website, search and events. No UI-only authorization. | Approved logical controls | K05 D1-02/05/13; K04 §23 |
| REQ-013 | Per-language records attach to a stable parent; accessible and localized interfaces require release-scoped verification. | Approved model; execution pending | K04 §9; K06 lines 138–158 |
| REQ-014 | Owner API operations define typed schemas, authorization, validation/error classes, stable IDs, pagination where needed, revision checks, idempotency and compatible events. | Approved logical contract; physical routes pending | K04 §10; K06 lines 67–82 |
| REQ-015 | A release passes only with reproducible build, migration, tests, security checks and execution evidence; specification status is distinct from implementation and deployment. | Approved delivery rule | K08 lines 104–118; K04 §28 |
| REQ-016 | Generic AI writing, translation, OCR/ASR, tagging, commentary and Ask-AI are excluded until separately decided. | Approved current exclusion | K04 §11; K11 ADR-010 |

Unique rules from detailed module packs are not yet asserted as fully consolidated. The [audit reports](reports/README.md) track that work.
