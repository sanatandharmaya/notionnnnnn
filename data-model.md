# Logical data model

**State:** approved logical boundaries, no physical tables or migrations. Canonical IDs are stable independent of title, slug or translation. A parent entity may have per-language content records; translations and transliterations do not replace the parent. Source, edition, locator, language and reviewer status attach to source-dependent claims. Quotation, transcription, translation, commentary, paraphrase, interpretation and computed output are distinct. [K04 §9]

| Owner | Logical entities / relationships | Key invariants |
| --- | --- | --- |
| S02/S23/S01 | Principal → credential/session and scoped role assignments | S02 issues immutable principal ID; S23 authenticates; S01 grants; same name/email is not identity proof. [K05 D1-01–04] |
| M03/S32/S33 | Domain entity → revision → language record → source/rights references → published projection | Domain meaning remains M03; S32 owns lifecycle; only approved exact revisions publish. [K02; K04 §§9, 11] |
| S05 | Media asset → rights metadata → authorized rendition | Provider URL is not canonical identity; rights/consent gate delivery. [K06 Storage] |
| S02 private registry | Principal → progress/bookmarks/notes/preferences | Private by default; never copied to public graph/search; explicit scoped sharing only. [K05 D1-11/13] |
| S07/S08/S09/S11 | Entitlement / payment / order / platform donation | Each state has one owner; payment outcome does not convey staff authority. [K04 §4; K05 D1-12] |
| S41/S12 | Event registration/ticket/check-in; live session metadata | Platform metadata and external streaming execution remain separate. [K07 R5] |
| S03/S04 | Taxonomy and authorized relationship edges; search projection | Projection is derived, not another content master; owner revisions invalidate stale edges. [K05 D1-11] |

Stateful entities require initial state, allowed transitions, history, archival/withdrawal and retention treatment. Soft delete, tombstone, anonymization, erasure and purge are distinct; no single retention period is specified. [K04 §9; K05 D1]

Physical keys, table names, relation cardinalities and migration order await review of the full P06/dictionary set and implementation. See [open questions](open-questions.md).
