# Documentation validation checkpoint

Checked 2026-10-23 UTC on `docs/eternal-sanskriti-reconciliation`. The checkout contains documentation and CSV audit indexes only; application installation, build and runtime tests are inapplicable.

| Check | Observed result |
| --- | --- |
| Required root documents | 19 / 19 exist with the requested capitalization; no lowercase competing `agents.md` |
| Current category organization | 37 notes, 37 source feature indexes and 37 category source maps |
| Relative Markdown links | 0 missing targets among 865 local links across 187 Markdown files in a local link-target scan |
| Source inventory | 5,479 unique `SRC-F` rows; 5,478 decoded text entries, 2,093,941 lines scanned, zero UTF-8 decode errors |
| Current category source mapping | 511 reference-subtree files; other/legacy files remain to be mapped semantically |
| Registry extraction | 758 category-scoped feature identifiers indexed with source lines across 37 registries; child specifications are not fully dispositioned |
| Core planning IDs | 17 `REQ`, 8 `FEAT`, 15 `DEC`, 7 `PH`, 10 `TASK`, 9 `CON`, 6 semantic/repeated-link `DUP` IDs; previous ID audit found no duplicate definition IDs or undefined Markdown references; repeat full ID audit after further reconciliation |
| Exact-file duplicates | 544 `DUP-F` pairs indexed separately; semantic effects still require review |
| Whitespace | `git diff --check` passed |

The link scan checks local targets, not semantic correctness of their destinations. ID checks find duplicate definitions in the current canonical files; they do not prove that all 5,478 text entries have requirement dispositions. The [reading coverage](reading-coverage.md) records 22 core reviewed pages, 6 partially reviewed pages, 37 structurally indexed registries and 5,414 pending entries. **Requirement disposition coverage remains unknown.** Conflicts and unresolved decisions are indexed in the [conflict register](conflict-register.md) and [open questions](../open-questions.md). The documentation is a reviewable provisional baseline, not an implementation-ready substitute for the source packs.
