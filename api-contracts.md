# API contracts

This is a **logical contract plan**, not deployed OpenAPI. Admin, website and future integrations consume commands/queries from the authoritative M01/M03 owners. Payload CMS supplies editorial facilities; custom APIs cover owner behavior beyond generic CRUD. Exact routes and schemas must be reconciled with D2/P06 before code. [K04 §10; K06 Backend/API]

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

Do not invent URL paths, HTTP status mappings, provider payloads, or field enums here. The [tasks](tasks.md) include contract extraction and executable contract tests.
