# Dependency-aware phases

This roadmap adapts the source's approved R0–R6 release order to this repository. **PH** IDs are documentation planning IDs; no implementation phase has started. [K07; K08]

| Phase | Objective, prerequisites and scope | Deliverable / exit evidence | Risks |
| --- | --- | --- | --- |
| PH-01 (R0) | Foundation after source-to-code mapping; FEAT-001/008, REQ-001/002/005/014/015. | Reproducible monorepo, admin/website/API boundaries, PostgreSQL/Payload, identity/grants, audit, media, jobs, locales, CI; clean install/migrate/build/test/run and security cases. | Physical contracts and policy details must be reconciled. |
| PH-02 (R1) | Editorial first slice after PH-01; FEAT-002/003, C01/C02. | Author → review → translate → rights check → publish → public read → withdraw works with audit and tests. | Source/rights and reviewer qualification. |
| PH-03 (R2) | Broader knowledge and deterministic discovery after PH-02; FEAT-004, C03–C37 in reviewed batches. | Category owners mapped, authorized index/search, locale/SEO and content tests. | Category ID migration, cultural/source differences, computed engines. |
| PH-04 (R3) | Authenticated devotee/private state after PH-01 and owner privacy model; FEAT-005. | W02–W04 and private progress/bookmarks/notes verified with denial and consent tests. | Family/child sharing and retention policy. |
| PH-05 (R4) | Money flows after identity, audit and private state; FEAT-006. | Subscriptions, checkout, orders and platform donations pass sandbox/idempotency/refund/reconciliation checks. | Provider contracts, rights and entitlements. |
| PH-06 (R5) | Events/live after account and payment modes; FEAT-007. | Registration/capacity/check-in and platform schedule/live metadata tested; free and paid modes distinct. | External stream execution and ticket modes. |
| PH-07 (R6) | External integrations and operating maturity after earlier owner contracts; FEAT-008 expansion. | Governed API/webhooks, restore drills, monitoring, scale/security evidence and runbooks. | Production operations and policy evidence. |

Security, privacy, audit, accessibility and testing are release-specific gates throughout, not a final catch-up phase. [K07 cross-release rules]
