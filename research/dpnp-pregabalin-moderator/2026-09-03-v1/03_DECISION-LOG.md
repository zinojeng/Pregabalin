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

## Decision 2026-09-03-05 — Gate 1 status: READY_WITH_PENDING_ITEMS, not PASS

- Decision: Gate 1 (source identities/search coverage) is declared `READY_WITH_PENDING_ITEMS`. Wave 2 is dispatched to `dpnp-guideline-diagnosis` and `dpnp-trials-comparative` for the leads already identified in `10_SOURCES/SOURCE_REGISTER.md` (§B1–B2, B5, C1–C4), and to `dpnp-pregabalin-safety` with instruction to independently search the Pregabalin label itself rather than wait. `dpnp-source-provenance` continues in parallel on the open gaps that are specifically its scope (Taiwan TFDA / FDA label discovery, ADA chapter DOI confirmation) rather than re-opening B1/B2 primary records, which are now `dpnp-guideline-diagnosis`'s job per role ownership.
- Taxonomy: `VERIFIED_NEW_SENSITIVITY` (proceeding is conditional, not unconditional)
- Reason: `dpnp-source-provenance`'s Wave 1 report (commit `5535eba`, merged `f9ea493`) shows disciplined, non-overstated tiering (`ACCESS_VERIFIED` / `IDENTIFIED_MULTI_SNIPPET` / `IDENTIFIED_SECONDARY_CITATION` / `NOT_YET_SEARCHED`) with good coverage across the required source classes (ADA 2026 Ch.12, AAN 2022 update, candidate trials/SR-MAs, Toronto Consensus lead) and no premature citation acceptance — sufficient to unblock guideline/trials verification work, which is exactly the deep-verification role those two peers own. However, no candidate has yet been opened at its own primary record by anyone, Taiwan TFDA and FDA label searches did not complete, and the ADA chapter DOI is unconfirmed — these are real gaps, not fabricable, so a full `PASS` would misrepresent verification state. Per Golden Rule 7, `BLOCKED`/partial gates are a valid research outcome, not a failure.
- Affected files: `05_STATUS.md`, `04_OPEN-QUESTIONS.md`.
- Approved by: Research Director.
