# Verification strategy

No application code exists here; **no application tests have run**. The documentation check is separate from implementation evidence. A specification marked complete does not mean built, tested, release ready or deployed. [K04 §28]

At implementation time, verify in layers: schema/contract, owner integration, UI component, end-to-end journeys, negative access/privacy, accessibility/localization, concurrency/idempotency, migrations/restore, performance and provider sandbox where applicable. Exact runners are implementation-time selections. [K06 Testing]

Critical cases: deny a staff/admin request without scoped grant; reject own sensitive revision approval; publish only rights-cleared exact revision and remove it on withdrawal; keep private notes out of search; preserve stable IDs and source provenance across translations; retry payment callbacks without double grant; preserve event capacity; reject invalid webhook signatures. [K05 acceptance cases; K07]

R0 exits only when a clean clone can install, migrate, build, test and run admin/website shells; access and audit checks execute, health works, CI is reproducible, and source-to-code/test mapping exists. R1 adds the full author → review → translate → approve → publish → public read path with rights/audit evidence. No zero-test or skipped critical check counts as proof. [K08 lines 104–118; K07 R1]

For this documentation branch, validate Markdown links, unique IDs, cross-file traceability and source coverage; report exceptions in [reports](reports/README.md).

D6 requires every later test result to pin source snapshot, fixture revision, runner/command, environment, timestamp and observed outcome. UI verification covers rendered ready/loading/empty/unavailable/restricted/stale/error states where applicable, plus accessibility and locale behavior. Negative tests must establish prohibited effects are absent. Saved specification, implemented code, executed test, release readiness and deployment each need separate evidence. [K17 lines 42–96; decision brief](docs/architecture/logical-decisions-d2-d6.md).

The 100 authored D2–D6 acceptance cases are grouped by owner and risk in the [acceptance-case map](docs/architecture/d2-d6-acceptance.md). They remain **not executed**; the map is a source index, not a passing test report.

P06 adds 20 authored logical completeness cases (`P06.TST-001`–`020`) for field, relationship, lifecycle, contract and evidence classification. These also remain **not executed**. [P06 closure](docs/architecture/p06-logical-closure.md); [K18 lines 114–194](reports/key-sources.md).
