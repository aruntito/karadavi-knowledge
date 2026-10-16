# KARADAVI Knowledge

Public, version-controlled knowledge data for KARADAVI — the Forest Trails knowledge platform.

## Purpose

This repository is intended to hold **human-approved, publishable knowledge records**, their entity relationships, provenance, and supporting indexes. It is separate from KARADAVI's private application code and operational systems.

## Editorial and safety rules

- **AI never publishes.** AI-generated or agent-generated material is a proposal until a human reviewer approves it.
- The default branch must contain only approved, publication-ready records.
- Keep research drafts, review queues, private notes, user data, credentials, tokens, and internal configuration out of this public repository.
- Record source URLs, attribution, access dates where relevant, and applicable source/data licences.
- Do not copy third-party material wholesale unless the applicable licence and terms permit it.
- Prefer stable KARADAVI entity IDs and small, category/entity-sharded files over a single giant dataset file.
- Validate records and references before proposing changes.

## Planned layout

```text
.
├── README.md
├── SCHEMA.md
├── SOURCES_AND_LICENSING.md
├── data/
│   ├── people/
│   ├── places/
│   ├── history/
│   ├── nature-earth/
│   └── society-culture/
├── indexes/
│   └── README.md
└── proposals/
    └── README.md
```

This is an initial organizational plan, not a claim that these directories or an integration already exist. We can refine category names to match KARADAVI's canonical ten trails.

## Suggested record principles

Each published record should generally include:
- a stable entity ID and entity type;
- canonical title and supported aliases;
- a concise KARADAVI-authored summary;
- source/provenance entries and licence/attribution details;
- relationships to other stable entity IDs;
- review/publishing metadata that is safe to expose publicly.

See [SCHEMA.md](SCHEMA.md) and [SOURCES_AND_LICENSING.md](SOURCES_AND_LICENSING.md) for the proposed contracts.

## Important architecture boundary

Git is the versioned source for static, published knowledge files; it is **not** a drop-in database replacement. A website integration should cache public data, handle missing or invalid records, and avoid making a GitHub API request on every page view. Accounts, roles, private drafts, approval state, and other operational data remain in the appropriate private backend.

## Current status

- [x] Public repository created
- [x] Initial repository policy documented
- [ ] Schema reviewed and accepted
- [ ] Example record validated by a human
- [ ] Index and validation strategy agreed
- [ ] Website integration separately reviewed and authorized

No connection to the live KARADAVI website is established by this repository alone.
