# Sources, Provenance, Attribution, and Licensing

**Status:** Policy draft — evaluate each source and dataset before use.

## Core rule

A publicly accessible page or dataset is not automatically free to copy, modify, redistribute, or republish. KARADAVI should write original summaries grounded in evidence, retain source metadata, and comply with the terms and licences that actually apply.

## Record for each source

Where applicable, capture:
- title and canonical URL;
- author, creator, publisher, or originating institution;
- publication/update date and access date;
- source identifier or dataset version;
- the applicable content or dataset licence and a link to its terms;
- required attribution and any share-alike or redistribution obligations;
- which claims or records the source supports;
- known limitations, uncertainty, and correction history.

Do not guess a licence. If the licence is unclear, mark it for human review and do not assume redistribution is permitted.

## Use upstream datasets carefully

Before ingesting from encyclopedias, public knowledge graphs, government portals, research indexes, biodiversity databases, maps, libraries, or other providers, confirm the terms for the particular API, dataset, database, and content fields. Different components of a service may carry different terms.

Keep data and prose from sources with incompatible licensing requirements separated where needed. Seek qualified advice for unclear obligations, especially attribution, share-alike, database rights, and redistribution requirements.

## Original editorial content

- Prefer concise, original KARADAVI explanations.
- Use sources to support factual claims rather than copy their expression.
- Do not import large blocks of article text or media without confirming that the licence permits it.
- For images and media, store their original source URL, creator, licence, attribution, and relevant reuse conditions.
- Correct errors while preserving enough provenance to explain why a record changed.

## Public repository hygiene

Never commit API keys, tokens, passwords, private drafts, personal data not suitable for public release, or internal admin details. Public Git history can retain removed content; do not rely on deleting a file later to make exposed secrets safe. Revoke any secret that is accidentally exposed and follow the relevant incident process.

## Human review checklist

Before approving imported or generated knowledge, a human reviewer should confirm:
1. The claim is relevant and supported by a credible source.
2. The source and any underlying dataset may be used as intended.
3. Required attribution and licence notices are included.
4. No copied expression exceeds what is permitted.
5. Relationships and entity resolution are sensible.
6. Sensitive or private information is excluded.
7. The record is consistent with KARADAVI's editorial standards.

AI may assist research and draft proposed summaries; **AI does not approve or publish records**.
