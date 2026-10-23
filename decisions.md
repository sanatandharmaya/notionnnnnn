# Decision index

Decision status applies to architecture documentation, not implementation evidence. [Source keys](reports/key-sources.md) identify approved records. The user's explicit target repository and three-app naming control this documentation task.

| ID | Decision | Status / evidence | Consequence |
| --- | --- | --- | --- |
| DEC-001 | One authoritative owner for each meaning/state; M01/M02/M03/M04 boundaries. | Approved; K02 lines 9–57, K04 §§3–4 | No second content, payment, authorization or private-state master. |
| DEC-002 | Current content taxonomy C01–C37, with old combined C04 split into Wellness, Ayurveda and Yoga. | Adopted; K03 lines 155–195, K09 | Historical C IDs require migration mapping. |
| DEC-003 | Monorepo, pnpm, Turborepo, strict TypeScript, Payload CMS v3, Next.js, PostgreSQL. | Frozen source baseline; K06 lines 17–33 | Exact versions and several vendors remain open. |
| DEC-004 | Admin/devotee/staff human types; Free/Seva/Premium separate tiers; scoped deny-by-default grants. | Adopted logical D1; K05 D1-01/02/12 | Neither role label nor payment grants staff authority. |
| DEC-005 | Editorial-first publishing with source/rights review; no generic production Ask-AI. | Accepted/current; K04 §11, K11 ADR-002/010 | AI capabilities need separate decision. |
| DEC-006 | R0–R6 dependency order, C01/C02 first knowledge slice. | Final pre-implementation plan; K07/K08 | Each phase needs executed exit evidence. |
| DEC-007 | Use `sanatandharmaya/notionnnnnn` and `apps/website` in this documentation. | User instruction supersedes historical target; CON-001 | Do not bootstrap historical `sanskritieternal/shiv`. |
| DEC-008 | Payload jobs, Cloudflare R2, Tailwind and GitHub Actions. | Preferred only; K06 lines 54–168 | Re-evaluate with implementation evidence/ADR. |
| DEC-009 | Exact auth library, HTTP framework beyond Payload/Next, search engine, hosting, observability vendor. | Implementation-time open; K06 lines 67–168 | Select during coding with owner contracts. |

Earlier eternalmu ADR-014 and ADR-022 are marked proposed in K11; their subject matter should not be mislabelled as approved merely because related later plans exist. See [conflicts](reports/conflict-register.md).
