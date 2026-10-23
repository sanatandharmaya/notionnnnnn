# Source inventory

The [file register](source-files.csv) assigns a stable `SRC-Fnnnnn` ID to every archive entry and records export-relative path, page ID when present, byte count, line count, SHA-256, and review state. Paths reference the uploaded ZIPs; original source text is not copied into this repository. Retrieval and archive inventory: 2026-10-23 UTC. ZIP metadata does not establish Notion's last-edited time, comments, or live-page state.

| Root ID | Confirmed root | Export status | Contents |
| --- | --- | --- | --- |
| SRC-001 | [Sanatan Dharma Platform](https://fir-surfboard-a8a.notion.site/Sanatan-Dharma-Platform-3d4005f3ba78805e9d65eec128f592b9), `3d4005f3ba78805e9d65eec128f592b9` | Supplied | 1,581 Markdown files, including 163 files without a Notion page ID in the filename. The user confirmed this root replaces the originally listed Eternal Sanskriti root `3e7005f3ba7880b9a88ce2d5556ed8c9`. |
| SRC-002 | [The eternal](https://fir-surfboard-a8a.notion.site/The-eternal-3ee005f3ba7880b1ba35dc9808362b97), `3ee005f3ba7880b1ba35dc9808362b97` | Supplied | 3,221 Markdown files plus one nested legacy ZIP containing 29 text files. |
| SRC-003 | [eternalmu](https://fir-surfboard-a8a.notion.site/eternalmu-3ea005f3ba788017b314e33c3d275e50), `3ea005f3ba788017b314e33c3d275e50` | Supplied | 645 Markdown files and 2 CSV files. This URL was submitted twice in the original brief; one root is registered. |

The exports contain no separately packaged image, audio, video, or PDF files; the nested ZIP is a legacy Puranas reference and was separately inventoried. Exported comments and database properties may be absent. The public site URLs still return tunnel 403 from this environment; analysis uses the ZIPs. [Reading coverage](reading-coverage.md) distinguishes automated line scanning from semantic review.
