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

## Decision 2026-09-03-06 — Accept trials-comparative Wave 2 evidence table; flag mandatory counter-bias content

- Decision: Accept `dpnp-trials-comparative`'s Wave 2 evidence table (`20_EVIDENCE/trials-comparative/01_EVIDENCE-TABLE.md`, branch commit `9475035`, merged `985c3ed`) as READY_WITH_PENDING_ITEMS for its own scope. Explicitly designate three findings as mandatory content for `40_SYNTHESIS/` under the sponsor-bias guardrail (Decision 2026-09-03-02): (a) Soliman/NeuPSIG 2025's class-pooled α2δ-ligand NNT (8.9) ranking numerically worse than TCA (4.6) and SNRI (7.4) NNTs despite equal guideline grade; (b) COMBO-DN's non-significant primary combination-vs-monotherapy result (P=0.370) and its uncorrected exploratory duloxetine>pregabalin finding; (c) OPTION-DM's finding of no significant pathway superiority among amitriptyline-, pregabalin-, and duloxetine-based regimens. These may not be omitted, softened, or buried in synthesis.
- Taxonomy: `VERIFIED_AND_REPLACE` (n/a — no prior conflicting value) / functionally `VERIFIED_NEW_SENSITIVITY` for the sponsor-bias mandate.
- Reason: All six sources (T1-T6) were opened by the peer at their own primary bibliographic record (PubMed/Crossref), not secondary snippets; numeric tokens copied verbatim; evidence correctly classified as DIRECT vs INDIRECT (T3 pregabalin/DPN-specific claims are class-pooled/mixed-etiology extrapolation, not direct). This is exactly the kind of finding the Research Charter (Primary question 4-5) and CLAUDE.md sponsor-bias rule require to be surfaced, not the kind that gets normalized away by narrative convenience.
- Affected files: `04_OPEN-QUESTIONS.md` (Wave 2 gaps + counter-bias findings section), `90_CROSS-SESSION-LOG/2026-09-03_STARTUP.md`.
- Approved by: Research Director.

## Decision 2026-09-03-07 — PI requirement: at least one lawful full-text PDF must be downloaded and LlamaParse-parsed before Final Gate

- Decision: Per explicit Human PI instruction (2026-09-03), Final Gate may not be declared until at least one lawfully acquired, decision-relevant guideline or regulator PDF has actually been downloaded locally and parsed PDF-to-Markdown via the globally configured `llamaparse` MCP — not merely identified as a lawful route. Dispatched to `dpnp-source-provenance` (owner of `10_SOURCES/` and the full-text ledger) rather than performed by the Director, per the Persistent Specialist Rule. No API key or credential may be exposed/persisted; no Sci-Hub/paywall bypass; restricted full text stays local/ignored; `10_SOURCES/FULLTEXT_LEDGER.md` must record URL, license, checksum, parser used, and output path for a completed acquisition, or an explicit `BLOCKED` reason if not achievable this wave. Current Wave 2 work (guideline-diagnosis, trials-comparative, pregabalin-safety verification) continues in parallel and is not paused for this.
- Taxonomy: `NEEDS_ANALYST` reframed as a direct PI directive — not optional, but scoped as an addition, not a blocker to ongoing Wave 2.
- Reason: PI-level requirement for demonstrated lawful full-text acquisition capability as part of Final QA, distinct from the discovery-only leads already logged.
- Affected files: `10_SOURCES/FULLTEXT_LEDGER.md`, `99_FINAL-QA.md` (future — Final Gate checklist item).
- Approved by: Human PI (relayed by Research Director).

## Decision 2026-09-03-08 — Accept guideline-diagnosis Wave 2 claim table; flag second sponsor-bias finding as mandatory

- Decision: Accept `dpnp-guideline-diagnosis`'s Wave 2 claim table (`20_EVIDENCE/guidelines-diagnosis/01_CLAIM-TABLE.md`, branch commit `11ba25b`, merged `b916280`) as READY_WITH_PENDING_ITEMS. Designate as mandatory `40_SYNTHESIS/` content under the sponsor-bias guardrail: both currently operative guidelines (ADA 2026 Rec 12.22, AAN 2022 Rec 4) grade gabapentinoids/SNRIs/TCAs/sodium-channel blockers as a **pooled class**, not pregabalin specifically; only the now-**retired** AAN 2011 guideline gave pregabalin a drug-specific Level A (vs. gabapentin's Level B in that same retired document). Any synthesis statement of pregabalin-specific "Grade A" status must cite 2011 explicitly as historical/superseded, never as current standing. This complements Decision 2026-09-03-06's trials-comparative findings — both specialists independently converged on the same structural point (current evidence/guidelines support the drug **class**, not pregabalin uniquely) from different source types.
- Also resolves two Open Questions: (a) AAN 2011 is formally `[RETIRED]` per its own PubMed record (PMID 21482920); AAN 2022 (Price et al.) is current operative AAN guidance. (b) No formal 2020s successor to Toronto Consensus (2010) was found; Atmaca et al. 2024 (Frontiers) is the closest candidate but is narrative expert-opinion (9 authors, no formal Delphi/grading process) and is classified `EXPERT INTERPRETATION`, not `GUIDELINE/CONSENSUS` — usable for the differential/red-flag section of the brief only if labeled as such.
- Taxonomy: `VERIFIED_NEW_SENSITIVITY` (sponsor-bias mandate) + `NEEDS_ANALYST` for the one open item below.
- Reason: ADA DOI confirmed two independent ways (PubMed + doi.org redirect); AAN 2022 verified via PubMed abstract + AAN's own lawfully-hosted clinician-summary PDF after Neurology.org returned 403 (paywall respected, not bypassed — lawful alternative primary record used instead); Toronto Consensus verified via a CC BY-NC-ND open-access institutional-repository PDF, used within license terms (short excerpts, attribution, no commercial use). All quotations verbatim with locators. One item flagged rather than smoothed over: Rec 12.19's sentence and Rec 12.20's exact clause-to-grade mapping were extracted via WebFetch summarization of the PMC page, not raw HTML/PDF text — logged as MODERATE confidence, needs a raw-text re-pull before verbatim use in synthesis (`NEEDS_ANALYST`, non-blocking for Gate 2).
- Affected files: `04_OPEN-QUESTIONS.md`.
- Approved by: Research Director.

## Decision 2026-09-03-09 — Accept pregabalin-safety Wave 2 label verification; Wave 2 complete

- Decision: Accept `dpnp-pregabalin-safety`'s Wave 2 report (`20_EVIDENCE/pregabalin-safety/LABELING_FDA.md`, `LABELING_TFDA.md`, `SAFETY_TOPICS.md`; local branch `worktree-dpnp-pregabalin-safety`, commit `735dd5c`, merged directly from the shared local git object store since the peer's `git push` was blocked by its own session's tool permissions — merged `405d999`) as READY_WITH_PENDING_ITEMS. All Wave 2 dispatches (guideline-diagnosis, trials-comparative, pregabalin-safety) are now complete. Both the current FDA label (Revised 04/2025, NDA 021446/022488) and the TFDA-stamped Taiwan package insert (衛署藥輸字第024995號, 2024-11-30) were opened and read directly, page by page; renal dosing tables are numerically identical between the two, treated as corroboration not independent replication.
- Taxonomy: `NO_CHANGE` (report accepted as delivered) with two `NEEDS_SOURCE` items carried forward, not silently resolved.
- Reason: Correctly discarded a same-session false lead (an accessdata.fda.gov URL that actually resolved to SUBOXONE, a different drug/NDA) before use — good provenance discipline. Correctly identified and flagged a VGHTPE patient-leaflet HLA-B*1502 genetic-testing mention as a likely carbamazepine-class-AED template artifact misapplied to pregabalin, not a pregabalin-specific requirement — excluded from any counseling checklist pending independent corroboration. Taiwan controlled-drug (管制藥品) schedule status could not be confirmed via TFDA's own site this wave; not guessed, flagged `NEEDS_SOURCE`.
- Affected files: `04_OPEN-QUESTIONS.md`, `05_STATUS.md`.
- Approved by: Research Director.
