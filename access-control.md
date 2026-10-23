# Access control

The logical policy is deny by default. Admin, devotee and staff are the only human account types; anonymous is request context and machine identities are technical principals. Editor, translator, reviewer, auditor and support are scoped grant bundles. Free/Seva/Premium are entitlements, never RBAC roles. [K05 D1-01/02/12]

Every protected request checks an active principal and session, current registered capability, resource scope, field scope, publication state, entitlement, consent and rights as applicable. Admin/staff type alone grants nothing; hiding a button does not authorize an operation. Expired or revoked assignments deny immediately. [K05 D1-02/06/12]

| Actor / function | Allowed only with | Denied by default |
| --- | --- | --- |
| Public reader | Published, rights-cleared public projection | Draft, private or restricted fields |
| Devotee | Session-derived own-resource allowlist | Other accounts, grants, staff routes |
| Editor/translator | Explicit domain and locale operations | Publish/security/customer access by job title alone |
| Reviewer | Delegated exact-revision review | Own sensitive revision approval without independent authority |
| Role/recovery administrator | Explicit registered grants, MFA and protected governance | Self-escalation and removal of final recovery principal |
| Webhook operator | Scoped `system.webhooks_operate` | Governance/purge without `system.webhooks_manage` |

S02 owns principal/profile, S23 credentials/sessions/MFA, S01 grants, S25 API client/credential lifecycle. Person editorial identity is distinct from login identity. C10 Person and CM04 Organization are current logical editorial masters; historical IDs require migration mapping. [K05 D1-03–11]

The exact capability registry, bootstrap/recovery runbooks and resource-specific policy matrices need review and implementation evidence. [K05 lines 90–97]
