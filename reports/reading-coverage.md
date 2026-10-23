# Reading coverage

Checkpoint: 2026-10-23 UTC. All **5,478 text entries** in the three ZIPs and nested legacy ZIP were decoded as UTF-8 and processed line by line into the [file register](source-files.csv): **2,093,941 lines**, with no decoding errors. The one ZIP entry is inventoried as a container. This proves byte-level traversal and metadata coverage; it does **not** mean every assertion has been reconciled. The file register marks 22 core pages `reviewed_core`, 6 pages `partial`, 37 category feature registries `structured_indexed`, and 5,414 entries `pending`. A structured index records feature IDs/names and source lines; it does not certify the child requirements, acceptance cases, conflicts or release scope. The full live Notion scope remains unknown.

The current reviewed set includes the project summary, architecture index, master category registry, C04–C06 split decision, D1 ownership decision, P07.17 stack, P07.18 releases, P07.19 R0 plan, eternalmu ADR log, full D2–D6 logical pages, and three P06 closure pages. The Sanatan Platform master architecture has a partial review focused on stack and authorization conflicts. See the [D2–D6 brief](../docs/architecture/logical-decisions-d2-d6.md), [acceptance-case map](../docs/architecture/d2-d6-acceptance.md), and [P06 closure](../docs/architecture/p06-logical-closure.md). Current conclusions are provisional until detailed specs and legacy differences have been reconciled.

| Measure | Result |
| --- | --- |
| Supplied archive entries | 5,479 including one nested ZIP container |
| Text entries with full line scan | 5,478 / 5,478 |
| Lines scanned | 2,093,941 |
| Core pages marked semantically reviewed | 22 / 5,478 text entries |
| Category registries indexed by structure | 37 / 37 current C01–C37 registries; 758 source feature identifiers indexed, not fully reconciled |
| Current category reference files mapped | 511 text entries across C01–C37; legacy source mapping pending |
| Requested roots with matching exports | 3 / 3 after user confirmed Sanatan replaces the original root |
| Requirement disposition coverage | Unknown: detailed extraction is incomplete |
| Unresolved decisions | At least the issues in the [conflict register](conflict-register.md); full count pending |

No live Notion comments, edit timestamps, unsupported attachments, or inaccessible descendants are claimed as reviewed.
