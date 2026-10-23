# Proposed monorepo

The user confirms three applications. The following **planned** directories describe responsibilities; no application directory or executable configuration has been created. Source P07.17 confirms a monorepo and workspace/tooling baseline; folder names below follow the user's requested `website` name. [K06 lines 17–52; CON-001]

```text
apps/
  admin/       Payload editorial and operational administration
  website/     Next.js public and account experience
  api/         owner-specific custom API boundary where needed
packages/
  contracts/   versioned public types and schemas, if multiple apps consume them
  ui/          browser-safe design primitives, if admin and website genuinely share them
```

`apps/admin`: editors/reviewers use S32/S33/S34 workflows; other authorized staff administer their owning S modules. Payload CMS v3 is the source-selected base. Operations check server-side grants and audit changes. Needs API/DB/media/locale configuration; verify one denied and one authorized operation, and complete editorial workflow. [K05; K06; K08]

`apps/website`: public readers browse W01 and later W02–W09 experiences. It consumes API projections, never authoritative finance, content, search or access state. Private W03/W04 screens require authenticated owner checks. Verify published content rendering, locale, inaccessible draft/private data, and key accessible journeys. [K03 W01–W09; K04 §5]

`apps/api`: custom owner operations, authenticated projections and later external integrations. Keep DB, secrets, provider adapters, and privileged business logic here or in server-only owner modules; Payload CMS may supply some editorial endpoints. The exact internal split between Payload and custom API is an implementation decision that must avoid two stores for one owner. Verify schema, auth, idempotency and error behavior. [K05; K06 lines 67–92]

`packages/contracts` is justified by typed requests/events shared by apps; it may depend only on portable schema/type code and cannot contain credentials or server data access. `packages/ui` is justified by S27 primitives used in both browser apps; its public interface is components/tokens, with no privileged API. Other packages named in P07.17 are possible later, but should be introduced only with actual consumers and ownership. Shared imports flow toward contracts/UI; apps must not import one another's private modules. [K02 lines 35–43; K06 lines 35–52]

A future `database/`, `e2e/`, and `.github/` structure is source-proposed, not present. Mobile is reserved future scope, not an initial application. [K06 lines 29–52]
