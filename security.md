# Security and privacy

Apply authorization at the API and owner boundary for every protected operation, including field-level filtering. Do not put server secrets, database access, private notes, child or family metadata, or privileged logic in browser packages. Public search, graph, cache, analytics and notifications must use privacy-safe projections. [K05 D1-02/05/13; REQ-012]

Credentials are protected by S23 and registered/lifecycle-managed by S25. Reveal a new secret only at authorized issue/rotation, never in generic serialization or audit payloads. Webhook signing uses the current per-subscription key model; unknown, revoked and out-of-window keys deny. No silent global fallback. [K05 D1-05/08]

Editorial publishing requires sourced claims, rights and safety checks, qualified review where relevant, and a way to withdraw or correct a specific revision. Living-person profiles and family/child data need explicit consent and privacy review; unsupported public-figure exemptions do not bypass the gate. [K05 D1-13; K04 §§9, 11]

Threat modeling, dependency review, secret scanning, negative authorization tests, restore drills and provider sandbox checks belong in each release's evidence. Exact retention, breach response, legal policy, RPO/RTO and hosting controls remain source/implementation decisions; no numeric targets are invented here. [K07 cross-release rules; K08 R0 acceptance]
