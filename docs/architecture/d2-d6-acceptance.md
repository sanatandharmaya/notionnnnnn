# D2–D6 acceptance-case map

The five adopted logical decision pages each define 20 authored cases. All 100 are **NOT EXECUTED**. This map points to the exact export source locations in [K13–K17](../../reports/key-sources.md); it does not substitute for owner specifications, implementation fixtures, or observed test results.

| Source | Authored cases and location | Verification concern | Cases to carry into implementation planning |
| --- | --- | --- | --- |
| K13, D2 | `D2.TST-001`–`020`, lines 110–190 | Legacy identity/category migration, fields, API wire and concurrency, event delivery, routes and publication | `001` record-level C04 split; `003` ambiguous Person alias quarantine; `009`/`010` stale or absent `If-Match`; `011`/`012` idempotency; `013` cursor audience binding; `014`–`016` event dedupe/order/version; `017`–`019` public routes, locales and feed eligibility |
| K14, D3 | `D3.TST-001`–`020`, lines 137–217 | Payment/subscription ownership, template delivery, ticket capacity and compensation, maintenance/status separation | `001`–`004` payment replay, callback ordering and refund balance; `005`–`007` subscription state; `008`–`010` template variable and locale safety; `011`–`016` ticket capacity, late payment and external ticketing; `017`–`020` maintenance precedence and restoration |
| K15, D4 | `D4.TST-001`–`020`, lines 135–215 | Private progress, family permissions, offline resets, consent/erasure/holds, backups and rights withdrawal | `001`/`002` cross-user and family denial; `006`–`008` offline and shared-device safety; `009`–`014` consent, erasure, legal hold and restore; `015`–`019` media rights and projection invalidation; `020` minimized analytics |
| K16, D5 | `D5.TST-001`–`020`, lines 147–227 | Source provenance, qualified review, current no-AI boundary, deterministic search and calendar computation | `001`–`004` attribution and review; `005`–`008` disabled AI/ASR/translation/semantic paths; `009`–`011` computation inputs and versioning; `012`–`018` C03/C11 ownership, unavailable state and disagreement; `019`/`020` fixture execution evidence |
| K17, D6 | `D6.TST-001`–`020`, lines 175–255 | Source access, repository selection, evidence provenance, UI/security/CI gates and M05 resume | `001`–`004` source pinning and instructions; `005`–`010` implementation versus executed-test evidence; `011`–`016` accessibility, locale, denial, provider exclusion and CI; `017`–`020` conflict, saved-document state and resume gate |

## Planning implications

- D2–D5 define behavior that later implementation tests must prove against a pinned code revision and owner contract. A case's presence in the source does not prove its implementation or correctness.
- D6 defines the evidence standard: pin source snapshot, fixture, runner, environment and observed outcome. A pass on one commit is not automatically evidence for another. [K17 lines 207–215]
- Negative cases must demonstrate absence of forbidden effects, including unauthorized data disclosure and prohibited provider calls. [K17 lines 225–231]
- D3 and D4 explicitly leave provider details, legal/retention policy and physical mechanics open. D5 leaves corpus and computation engine selection open. [K14 lines 219–223; K15 lines 217–221; K16 lines 229–233]
- D6's historical M05 gate does not authorize application implementation in this documentation assignment. The selected repository currently contains documentation only. [K17 lines 257–272]

The source tails also link to owning packs and registers. Those linked pages require their own semantic review before any case is turned into a final implementation contract. See [reading coverage](../../reports/reading-coverage.md) and [progress](../../reports/progress.md).
