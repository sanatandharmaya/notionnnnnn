# D2–D6 logical decision brief

This brief preserves the current logical reconciliations in [K13–K17](../../reports/key-sources.md). It is a selective synthesis of the decision, schema and lifecycle sections reviewed so far. Their acceptance-case and source-reference tails still need review, so this page is **not a physical schema or implementation-ready contract**. D6 records that M05 implementation evidence is paused; the user's current repository and documentation-only task supersede historical repository identities in D6.

## D2 — identity, wire contracts and routes

- Canonical references use immutable owner-issued opaque IDs plus owner, kind and revision. Legacy aliases retain source namespace/entity/ID/revision and a reviewed mapping disposition; ambiguity is quarantined. The current C04 split requires record-level migration, while old C05–C35 map by +2 only within the adopted mapping context. [K13 lines 11–21]
- Logical field records include type, validation, requiredness/nullability, read/write policy, cardinality, lifecycle and SPEC/TEST links. Object/array members need explicit constraints. One parent identity has language variants; content language and UI locale are distinct. [K13 lines 23–29]
- JSON single/collection operations use `data` plus `meta`; sanitized errors use `error`. Native binary/RSS/stream formats remain native. New operations distinguish 400 malformed syntax, 422 invalid fields, 401 unauthenticated, 403 safe denial, 404 absence/concealment, 409 business/idempotency conflict, 412 stale `If-Match`, and 428 required `If-Match` missing. Existing revision endpoints can keep registered adapters. [K13 lines 31–37]
- New collections use audience/query/locale-bound opaque cursors, stable ordering and per-page reauthorization. Create/transaction idempotency binds principal/client, owner, operation and canonical request hash. Committed state changes use an outbox; consumers dedupe atomically and must not let old events reverse newer state. S25 transports signed webhooks, S26 executes jobs and S17 audits. [K13 lines 39–49]
- M02 owns a single route dictionary. Locale switching resolves the same canonical entity. Public GET/HEAD aliases can redirect 308 only to eligible published targets; mutation routes do not redirect by slug. Missing language variants show a labeled unavailable/fallback state. S13 owns article bodies; Series groups article references. Cross-owner deletion does not cascade silently. [K13 lines 51–65]

## D3 — money, communication, events and maintenance

- S08 owns payment execution/refunds/reconciliation; S07 owns subscription and effective entitlements; S09 orders; S11 donations; S41 event participation. Money carries amount, ISO currency and a precision policy. Business, provider and settlement states are distinct, and provider callbacks are authenticated and idempotent. [K14 lines 11–33]
- S38 owns published, versioned templates and variable schemas; S06 delivers using a pinned template version and validated inputs. Secrets and prohibited private fields cannot enter generic variables, previews or logs. [K14 lines 35–41]
- S41 owns registration, capacity, holds, ticket issuance and check-in. Free RSVP, platform-paid and external-ticketed modes remain distinct. Payment success alone does not issue admission; refunds and participation cancellations have separate owners. [K14 lines 43–53]
- S19 owns maintenance activation/scope/bypass; S40 owns health/incidents. Neither state implies the other. Cross-owner compensation is explicit, and retention is purpose-specific rather than one inherited global period. [K14 lines 55–65, 127–135]

## D4 — private state, rights and retention

- S02 owns private progress/bookmark/note state using X07/X08/X09 semantics. Private activity cannot become a public profile, sitemap, ranking, search index or marketing input through an account relationship alone. Reading, course, attendance, practice and devotional metrics remain distinct; no spiritual worth score is inferred. [K15 lines 11–21]
- Family labels do not prove guardianship or cross-account access. Child data needs purpose minimization and explicit policy. Withdrawn/superseded content leaves a private unavailable reference rather than leaking text or guessing a replacement. A reset generation prevents late/offline updates from resurrecting cleared progress. [K15 lines 23–41]
- Consent withdrawal, erasure, legal hold, backup expiry and content-rights withdrawal are different governed operations. S31 determines purpose/retention policy; S24 restores backups only with tombstone/revocation replay. S05 rights eligibility and domain/S32 publication jointly gate delivery; private references cannot retain access to withdrawn media. [K15 lines 43–65, 125–133]

## D5 — source truth and computation

- Domain owners retain source-grounded meaning. Published source-dependent claims need work/document, edition where material, locator, language/origin and review state. Quotation, transcription, translation, paraphrase and interpretation are distinct; traditions and schools can retain different attributed interpretations. Qualified review is a domain gate. [K16 lines 11–25]
- Current production scope excludes AI inference/generation, ASR, OCR, automated translation/tagging, embeddings and semantic search. Search uses explicit deterministic lexical/facet rules over eligible owner fields. Human translation pins source revision and review evidence. [K16 lines 27–37]
- C03/shared calculation authority computes versioned results; C03 owns Jyotisha meaning and definitions. C11 owns festival definitions and reviewed occurrence projections, not the calculation engine. A place/date result needs location, IANA time zone, timezone-data version, engine/rule/profile and relevant astronomical assumptions. `Unsupported`, `stale`, `failed`, `disputed` and `computed` are distinct states. Source disagreement stays visible with scope and provenance. [K16 lines 39–65]

## D6 — implementation evidence

- Historical D6 repository-access claims concern other repositories and do not describe this user's selected `sanatandharmaya/notionnnnnn`. D6 explicitly separates completed architecture documentation from the future implementation-evidence gate. [K17 lines 3–38]
- Implementation findings must pin repository/snapshot, inspected artifact, mapped requirement, behavior and test evidence. Access failure is `BLOCKED/UNKNOWN`, not proof of absent code. Authored acceptance cases remain `NOT EXECUTED`; physical schema, runtime behavior and UI states require actual evidence. Negative security/privacy tests and CI evidence are separate release gates. `SAVED VERIFIED`, `IMPLEMENTED`, `TESTED`, `RELEASE READY` and `DEPLOYED` are not interchangeable. [K17 lines 42–96]

The per-source [file register](../../reports/source-files.csv) retains exact page IDs and archive paths. This brief does not copy the source's full logical type definitions or acceptance cases; review the owning page before designing a physical schema, endpoint or release test.
