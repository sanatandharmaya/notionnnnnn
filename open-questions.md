# Open questions and blockers

These questions do not block writing the source-backed architecture baseline. They block a claim of complete implementation readiness or particular coding tasks. Answers should be recorded as decisions with source/owner and propagated to affected requirements.

| ID | Question, impact and recommendation | User answer needed? |
| --- | --- | --- |
| OQ-001 | Have the detailed M01/M02/M03/M04 specs, legacy pages and Sanatan Platform export been fully reconciled with the current P07 baseline? Coverage is still pending for most text entries. Finish source review before freezing category contracts. | No, editorial work first |
| OQ-002 | Which exact D2/P06 operation schemas, field enums, errors and route bindings govern R0? Extract approved owner dictionaries and mark proposals; blocks TASK-001/004. | Only for unresolved product choices |
| OQ-003 | Which legal, source-rights, living-person, child/family and retention policies apply to the first release? Use qualified review; do not invent numeric retention or consent rules. | Possibly, after source reconciliation |
| OQ-004 | What hosting, auth library, physical schema and provider adapters meet the frozen stack? Select at implementation time with evidence and ADR, not in this documentation task. | No, engineering choice within constraints |
| OQ-005 | Does each C03–C37 category have current approved fields, workflows, permissions, tests and source corpus? Review the per-category references; do not infer readiness from a title/index. | Only for missing approvals |
| OQ-006 | Which project-specific details in the supplied Sanatan Platform archive remain current after The eternal's P07 freeze? Treat identical files as duplicates and old IDs as provenance until reconciled. | No, source review first |

See [source coverage](reports/reading-coverage.md), [conflicts](reports/conflict-register.md) and [progress](reports/progress.md).
