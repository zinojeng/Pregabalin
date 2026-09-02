# Decision Log

## Decision 2026-09-03-01 — Clinical Evidence Review topology

- Decision: Use one persistent Research Director and four persistent specialists: source/provenance, guideline/diagnosis, trials/comparative effectiveness, and Pregabalin safety/implementation. Use an independent temporary read-only auditor only after synthesis.
- Taxonomy: `NO_CHANGE`
- Reason: Matches the Clinical Evidence Review pattern while keeping persistent sessions few and role ownership non-overlapping.

## Decision 2026-09-03-02 — Sponsor-bias control

- Decision: Pregabalin receives detailed evaluation but no presumptive preferred status. All recommendation language must include appropriate alternatives, uncertainty, harms, and applicability.
- Taxonomy: `VERIFIED_NEW_SENSITIVITY`
- Reason: The educational event is medication-sponsored; scientific integrity requires a predeclared counter-bias rule.

## Decision 2026-09-03-03 — Full-text acquisition

- Decision: Use lawful open access, publisher/author copies, user-supplied files, or already-authorized institutional access. Do not use Sci-Hub or paywall bypass. Keep restricted PDFs and parsed text local/ignored.
- Taxonomy: `NO_CHANGE`
- Reason: Copyright, licensing, public-repository, and provenance requirements.

## Decision 2026-09-03-04 — Academic research agents repository

- Decision: Use `zinojeng/academic-research-agents` as workflow inspiration only, not as an evidence source or production MCP.
- Taxonomy: `NO_CHANGE`
- Reason: Direct inspection found placeholder PubMed/arXiv/Semantic Scholar searchers and placeholder PDF parsing/summarization functions.
