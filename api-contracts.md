# API contracts

This is a **logical contract plan**, not deployed OpenAPI. Admin, website and future integrations consume commands/queries from the authoritative M01/M03 owners. Payload CMS supplies editorial facilities; custom APIs cover owner behavior beyond generic CRUD. D2's reviewed logical decisions are summarized in the [D2–D6 brief](docs/architecture/logical-decisions-d2-d6.md); exact route/operation inventories and P06 schemas still need reconciliation. [K04 §10; K06 Backend/API; K13]

Every operation needs a stable operation ID, owner, typed input/output, validation, applicable principal/capability/resource/field policy, canonical errors, and compatibility/version rule. Large collections use cursor pagination. Mutations with retries or concurrency require idempotency keys and revision/ETag-like preconditions as appropriate. [K04 §10]

| Consumer need | Logical owner | Proposed operation family, not an approved path |
| --- | --- | --- |
| Admin editorial author/review/publish | M03 + S32/S33/S34 | Create revision; submit; approve; publish/withdraw |
| Website public reading | M03 published projection | List/detail by canonical ID and locale |
| Website private account | S02/S23 | Read/update own allowed state using session-derived principal |
| Website discovery | S04 over owner projections | Authorized lexical/facet query |
| Commerce and giving | S07/S08/S09/S11 | Entitlement, checkout, payment outcome, donation receipt |
| Events/live | S41/S12 | Schedule, registration, ticket, stream metadata |

Events represent committed owner facts. Define event type/version, occurrence ID, producer, timestamp, aggregate owner/ID/revision, payload, privacy projection, dedupe and ordering. Event schema version, aggregate revision and delivery attempt differ. Webhook credentials are S25-owned; S23 protects secrets; S01 grants scope. [K04 §10; K05 D1-05/08]

D2 establishes `data`/`meta` JSON envelopes, sanitized `error`, native RSS/binary/stream formats, and new-operation 400/422/401/403/404/409/412/428 distinctions. Opaque cursors reauthorize each page; idempotency binds the request to the principal/client and canonical body; committed events use outbox/inbox delivery rules. Existing endpoints may retain registered compatibility adapters. [K13 lines 31–49] Do not invent URL paths, provider payloads, unreviewed field enums or physical bindings here. The [tasks](tasks.md) include contract extraction and executable contract tests.
