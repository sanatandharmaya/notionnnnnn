# Category and domain map

Current source architecture separates **M01 system** (S01–S41), **M02 website** (W01–W09), **M03 content** (C01–C37), **M04 shared contracts** (X01–X25), and **M05 delivery**. [K02–K03](key-sources.md). M03 current names and links are in [docs/categories](../docs/categories/README.md); each has a [source audit](categories/README.md). The K10 classification registry is a **working canonical input**, and category-level validation remains required before schema freeze (K10 lines 403–407).

The old combined C04 was split; current IDs C04 Wellness, C05 Ayurveda, C06 Yoga must not be interpreted using old C05–C35 labels without the [renumbering map](conflict-register.md#conflict-register). Other key boundaries: C09 deity relationships vs C28 places; C27 pilgrimage routes vs C28 places; C08 heritage vs C33 performing arts and C34 crafts; C23 language knowledge vs C31 courses. [K09; K10 lines 377–387]

## Proposed Notion mirror hierarchy

The requested GitHub Markdown is the consolidated output. A future Notion mirror could use:

```text
Eternal Sanskriti documentation
├── Start here / product / goal
├── Governance, decisions and open questions
├── Architecture
│   ├── M01 System S01–S41
│   ├── M02 Website W01–W09
│   ├── M03 Content C01–C37 (one page per current category)
│   ├── M04 Shared X01–X25
│   └── M05 Delivery and release evidence
├── Requirements and feature catalogue
├── Admin / Website / API contracts
├── Phases and tasks
└── Audit reports / source inventory / duplicates / conflicts / coverage
```

This is a proposed organization, not a Notion edit. Preserve original pages and page IDs. Cross-links should point to one canonical owner rather than copying content into every category.
