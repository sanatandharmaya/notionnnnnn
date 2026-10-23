# Durable project memory

Eternal Sanskriti is a multilingual Sanatan Dharma knowledge, devotional, editorial and digital-services platform. This repository is the user-selected documentation and future monorepo target. Three applications are confirmed: admin, website and API. Current source architecture separates M01 System (S01–S41), M02 Website (W01–W09), M03 Content (C01–C37), M04 Shared (X01–X25), and M05 delivery evidence. [K02–K04](reports/key-sources.md)

The current approved taxonomy splits former C04 into C04 Wellness, C05 Ayurveda and C06 Yoga; old numeric IDs cannot be reused without mapping. One owner governs each fact/state. Admin/devotee/staff are human account types; Free/Seva/Premium are tiers. Editorial publishing needs sourced, revisioned review; generic production AI is excluded. [decisions](decisions.md)

The source-selected frozen stack is pnpm/Turborepo/strict TypeScript/Payload v3/Next.js/PostgreSQL. Three-app folder names follow the user's `apps/admin`, `apps/website`, `apps/api` request. Exact versions and several vendor choices remain for implementation. No application code, runtime tests or deployments exist. [architecture](architecture.md) · [monorepo](monorepo.md)

The uploaded exports have been line-scanned, but most detailed content still needs semantic reconciliation. Check [reading coverage](reports/reading-coverage.md) and [progress](reports/progress.md) before using these documents as a coding contract. The historical source repository `sanskritieternal/shiv` is superseded for this task by `sanatandharmaya/notionnnnnn`. [CON-001](reports/conflict-register.md)
