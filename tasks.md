# Implementation backlog

Every task below is **not started**. Documentation is planning evidence only. IDs map to [requirements](requirements.md), [features](features.md), [phases](phases.md), and [source keys](reports/key-sources.md). Exact implementation tickets should be split further after detailed source reconciliation.

| ID | Outcome / affected area | Phase; IDs; dependency | Acceptance and verification | Blockers |
| --- | --- | --- | --- | --- |
| TASK-001 | Reconcile D2/P06 and module dictionaries into a versioned operation and data contract inventory; docs/API. | PH-01; REQ-002/014, FEAT-008; none | Each operation has owner, schema, access, error, revision/idempotency rule and source ID; review matrix. | Detailed source review |
| TASK-002 | Bootstrap three app boundaries and justified shared packages; monorepo. | PH-01; REQ-001/015, FEAT-001; TASK-001 | Clean clone install/build/test runs; dependency boundary check. | Implementation task, no code here |
| TASK-003 | Establish principal, session and scoped grant foundation; API/admin. | PH-01; REQ-005/012, FEAT-001; TASK-001/002 | Executed allow/deny/expiry/self-escalation tests and audit. | Exact capability registry |
| TASK-004 | Establish PostgreSQL/Payload migration and editorial base; admin/API. | PH-01; REQ-002/004/011, FEAT-001; TASK-001/002 | Migration and revisioned storage tests; no duplicate authority. | Physical schema approval |
| TASK-005 | Implement C01/C02 author-to-public journey; admin/API/website. | PH-02; REQ-003/004/006/011/012/013, FEAT-002/003; TASK-003/004 | Full workflow, rights, locale, withdrawal and public read E2E evidence. | Source/rights review |
| TASK-006 | Build authorized deterministic search projection; API/website. | PH-03; REQ-008/012/014, FEAT-004; TASK-005 | Published only, scoped query/facets, stale revision invalidation; negative privacy tests. | Search contract extraction |
| TASK-007 | Add private self-service progress, bookmarks and notes; API/website. | PH-04; REQ-005/007/012, FEAT-005; TASK-003 | Session-derived own state; other-account/private-field denial; consent/revocation tests. | Family/child policy |
| TASK-008 | Integrate separated subscription/payment/order/donation owners; API/admin/website. | PH-05; REQ-009/012/014, FEAT-006; TASK-003/007 | Sandbox payment, duplicate callback, refund and entitlement tests. | Provider/policy details |
| TASK-009 | Implement event registration and live metadata; API/admin/website. | PH-06; REQ-010/012/014, FEAT-007; TASK-008 where paid | Capacity/concurrency, ticket mode, stream schedule and failure tests. | External service contract |
| TASK-010 | Harden external APIs/webhooks and operations; API/deployment. | PH-07; REQ-012/014/015, FEAT-008; TASK-001–009 | Signature rotation, scope, retry/dedupe, restore, security and operational evidence. | Policies and provider selection |

Additional C03–C37 tasks must be generated from each reconciled category specification; a single vague “build content” task would hide unique constraints.
