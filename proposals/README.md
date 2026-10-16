# Knowledge Proposals

This directory describes the intended workflow; it is not intended to host private drafts.

## Publication workflow

1. A research agent gathers source references and creates a proposed change in a separate proposal location or draft system.
2. Automated checks validate syntax, required provenance, licences/attribution fields, entity IDs, and references.
3. A human editor reviews factual support, originality, sensitive information, licensing, and KARADAVI editorial style.
4. The human editor approves the exact change.
5. Only the human-approved, validated result is merged into the published data branch.
6. A generated index is refreshed and checked against the approved records.
7. Website consumption happens only through a separately reviewed integration.

## Guardrails

- AI agents may research, draft, validate, and recommend; they must not self-approve or publish.
- No automatic merge of an agent-created proposal into the published branch.
- No credentials, private review comments, personal data, or operational state in this public repository.
- A failed validation blocks publication.
- Keep an auditable link between the approved change, its source references, and the review performed.

Use KARADAVI's private editorial workflow for private drafts and reviewer notes.
