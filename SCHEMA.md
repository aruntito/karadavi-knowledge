# KARADAVI Knowledge Record Schema (Proposal)

**Status:** Draft proposal — review before production use. This document does not establish a live website contract.

## Principles

1. Stable identifiers: entity IDs should not depend on titles or URLs.
2. Explicit provenance: factual claims should be traceable to sources.
3. Separate evidence from narrative: source descriptions are not automatically facts.
4. Avoid false precision: use null or omit a field when it is unknown.
5. Preserve language and script: store Kannada text in Unicode; do not transliterate away the original form.
6. Avoid duplicate canonical entities: aliases should point to a stable entity ID.
7. Human publication gate: proposed records remain outside the published data path until reviewed and approved.

## Proposed entity record

```json
{
  "schema_version": "0.1",
  "id": "entity:example-stable-id",
  "type": "place",
  "title": {
    "en": "Example place",
    "kn": "ಉದಾಹರಣೆ ಸ್ಥಳ"
  },
  "aliases": [
    {
      "value": "Example alias",
      "language": "en",
      "kind": "alternate-name"
    }
  ],
  "summary": {
    "en": "A concise, evidence-grounded summary written in KARADAVI's editorial style.",
    "kn": "ಕರಾಡವಿಯ ಸಂಪಾದಕೀಯ ಶೈಲಿಯಲ್ಲಿ ಬರೆಯಲಾದ ಸಂಕ್ಷಿಪ್ತ, ಆಧಾರಿತ ಸಾರಾಂಶ."
  },
  "trail": "places",
  "claims": [
    {
      "predicate": "located_in",
      "object_id": "entity:parent-place-id",
      "source_ids": ["source:example-source"],
      "confidence": "supported"
    }
  ],
  "relationships": [
    {
      "predicate": "related_to",
      "target_id": "entity:related-entity-id"
    }
  ],
  "sources": [
    {
      "id": "source:example-source",
      "title": "Source title",
      "url": "https://example.org/source",
      "publisher": "Publisher name",
      "accessed_at": "2026-10-16",
      "license": "Check and record the actual applicable licence",
      "attribution": "Required attribution, if any",
      "supports": ["claim:example-claim"]
    }
  ],
  "media": [],
  "editorial": {
    "status": "approved",
    "reviewed_at": "2026-10-16",
    "reviewer_role": "human-editor"
  }
}
```

The IDs, example URL, dates, language examples, and values above are illustrative. Do not treat them as a live production schema or create references to entities that do not exist.

## Field guidance

- `schema_version`: allows records and consumers to evolve deliberately.
- `id`: immutable KARADAVI identifier; never reuse it for a different entity.
- `type`: canonical entity type agreed by KARADAVI's domain model.
- `title` and `aliases`: preserve original forms, language tags and provenance where needed.
- `summary`: original editorial prose grounded in evidence, not copied source passages.
- `trail`: one of the canonical KARADAVI trails; validate against the agreed enum.
- `claims`: atomic claims with source references, allowing disputed facts to be evaluated independently.
- `relationships`: links to stable IDs, with predicates from an agreed vocabulary.
- `sources`: source metadata, not a guarantee that a source is accurate or reusable.
- `editorial.status`: public records should be human-approved. Keep private reviewer notes and workflow data in the private system.

## Validation rules to adopt

- Reject invalid JSON and unsupported schema versions.
- Reject duplicate IDs and references to missing entities.
- Require source evidence for material factual claims.
- Require source-licence and attribution review before publication.
- Do not publish credentials, personal private data, unpublished drafts, or internal workflow data.
- Never allow an AI agent to change a proposal directly into an approved state.
- Keep the actual approval record and audit trail in the private workflow system; only expose minimal publication metadata publicly.

## Important

This proposal must be reconciled with KARADAVI's existing canonical entity model and ten-trail taxonomy before bulk import or website integration.
