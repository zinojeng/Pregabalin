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

## Decision 2026-09-03-10 — Challenge-round phrasing guardrails from dpnp-trials-comparative

- Decision: Adopt four mandatory phrasing constraints for `40_SYNTHESIS/`, derived from `dpnp-trials-comparative`'s challenge-round response (no correction needed to `01_EVIDENCE-TABLE.md` itself — these are synthesis-time guardrails):
  1. T1 (Freeman 2008) is placebo-only, no active comparator — its dose-response/time-to-onset numbers may never be used to imply relative superiority over duloxetine/amitriptyline/gabapentin; must always be paired with T5/T6's head-to-head null findings.
  2. T3 (Soliman/NeuPSIG) NNT/NNH must always carry the verbatim qualifier "α2δ-ligands (pooling gabapentin and pregabalin; not a pregabalin-only estimate)" — never presented as a standalone "pregabalin NNT."
  3. T2 (Frontiers 2026 combo SR) maximally honest phrasing is fixed: "Very limited, low-certainty evidence (GRADE low, 3 RCTs, 471 patients, only 2 poolable for the primary endpoint) suggests pregabalin+duloxetine combination may reduce short-term pain more than monotherapy; safety outcomes remain uncertain due to few trials and imprecision — not yet a robust basis for a routine combination recommendation."
  4. The counter-bias findings (Decision 2026-09-03-06) must not be overcorrected into an unsupported opposite claim: T5's duloxetine>pregabalin result was an uncorrected exploratory analysis (hypothesis-generating, not confirmatory) on a non-significant primary outcome; T6 showed near-zero differences with CIs centered on zero (statistical equivalence, not inferiority). Correct framing is "head-to-head RCTs found no significant difference among pregabalin-, duloxetine-, and amitriptyline-based regimens" — never "pregabalin underperformed" or "proven inferior."
- Taxonomy: `VERIFIED_NEW_SENSITIVITY`
- Reason: The challenge round is specifically designed to catch both directions of sponsor bias (overselling pregabalin AND overselling the negative findings against it) before drafting, per Runbook §30.
- Affected files: `04_OPEN-QUESTIONS.md`.
- Approved by: Research Director.

## Decision 2026-09-03-11 — Accept guideline-diagnosis self-correction (Rec-number mislabeling)

- Decision: Accept `dpnp-guideline-diagnosis`'s challenge-round self-correction (commit `1e569ad`, merged `02e1ea0`). While re-checking its own table for the challenge round, the peer found and fixed 6 AAN-2022 recommendation-number locator labels that were off-by-one/misattributed, caused by `pdftotext -layout` interleaving the source PDF's two-column recommendation/rationale blocks; re-extracted with plain `pdftotext` (true reading order) and corrected. Verified directly via `git diff 11ba25b 1e569ad`: every verbatim quotation and every Level grade is byte-identical before and after — only the "Rec #" locator column changed, now matching the source's own Rec 1-9 numbering exactly. No clinical content or grade changed.
- Taxonomy: `VERIFIED_AND_REPLACE` (locator labels only)
- Reason: This is exactly the self-correction behavior the challenge round is designed to surface — a peer catching its own extraction-tool artifact before it reached synthesis, disclosing it with an in-file correction log rather than silently fixing it, and preserving the fact that no substantive/clinical content was wrong. Golden Rule 8 (never silently repair) was honored.
- Affected files: none outside `20_EVIDENCE/guidelines-diagnosis/01_CLAIM-TABLE.md` (peer-owned).
- Approved by: Research Director.

## Decision 2026-09-03-12 — Accept pregabalin-safety challenge-round response; elevate two synthesis guardrails

- Decision: Accept `dpnp-pregabalin-safety`'s challenge-round response (`20_EVIDENCE/pregabalin-safety/SAFETY_TOPICS.md`, commits `c7e5005`/`d562259`, merged `7f4d6e2`; push-permission issue from Decision 2026-09-03-09 is now resolved). Elevate two findings to mandatory `40_SYNTHESIS/` guardrails: (a) a compounded-risk callout for elderly + reduced renal function + concurrent CNS-depressant/diuretic/thiazolidinedione use — labeled `EXPERT INTERPRETATION` (inference from individually-documented label findings, not a directly-studied combined-risk trial finding); (b) a documentation-depth-asymmetry guardrail — this role's unusually exhaustive pregabalin harm documentation must not be read as "pregabalin has worse harms than comparators" by omission of context; respiratory depression with CNS depressants is a class-wide gabapentinoid warning, not pregabalin-unique, and Schedule V/misuse framing needs opioid/TCA context before any relative-safety statement.
- Taxonomy: `VERIFIED_NEW_SENSITIVITY`
- Reason: Item (b) is a distinct, subtle sponsor-bias risk not previously captured — asymmetric documentation depth across specialist roles (by design, since only pregabalin-safety was tasked with exhaustive label extraction) could read as an implicit safety comparison no one actually made. Also confirms citing only the reassuring PD-interaction sentence while omitting the broader postmarketing warning as a specific citation-fidelity failure mode for the eventual auditor to check.
- Affected files: `04_OPEN-QUESTIONS.md`.
- Approved by: Research Director.

## Decision 2026-09-03-13 — Gate 2: READY_WITH_PENDING_ITEMS

- Decision: Gate 2 (guideline, comparative evidence, and safety findings reconciled; challenge round complete) is declared `READY_WITH_PENDING_ITEMS`. All three Wave 2 specialists reported, were verified by direct file inspection (not summary-only), and completed the adversarial challenge round with substantive results: one genuine self-caught-and-corrected error (Decision 2026-09-03-11), and multiple synthesis-time phrasing/framing guardrails now fixed in the Decision Log (2026-09-03-06, -08, -10, -12). Two independently-convergent sponsor-bias findings (drug-class-vs-pregabalin-specific grading; NNT ranking) and one documentation-asymmetry guardrail are mandatory content for Wave 3. Remaining open items (`04_OPEN-QUESTIONS.md`) are non-blocking per each owning specialist's own assessment, except the PI's lawful-PDF+LlamaParse requirement (Decision 2026-09-03-07), which blocks Final Gate specifically, not Gate 2/Wave 3.
- Taxonomy: `VERIFIED_NEW_SENSITIVITY` (conditional advance, not unconditional)
- Reason: Per Golden Rule 6 (facts before interpretation) and Runbook §21/§30, Wave 3 synthesis drafting may now begin using only Director-approved facts/methods/evidence, carrying forward every guardrail fixed above verbatim rather than re-deriving them at drafting time.
- Affected files: `05_STATUS.md`.
- Approved by: Research Director.

## Decision 2026-09-03-14 — Accept source-provenance's B3/B4 closure and PI-directive first attempt; decline ADA PMC bulk-parsing on TDM license grounds

- Decision: Accept `dpnp-source-provenance`'s closure of B3 (Taiwan TFDA — one 2010 safety alert found, current package insert still not located, logged as a gap not fabricated) and B4 (FDA label via DailyMed, `ACCESS_VERIFIED`, internal date discrepancy flagged not reconciled) and the ADA Ch.12 DOI confirmation (10.2337/dc26-S012, corroborating `dpnp-guideline-diagnosis`'s independent confirmation). On the PI directive (Decision 2026-09-03-07): affirm the decision to **decline** downloading/LlamaParsing the ADA Standards of Care PMC PDF because its license explicitly bars text/data mining and machine-learning use without prior written permission — this is the correct call and is not to be revisited without ADA's written permission; short-quote/reading use by `dpnp-guideline-diagnosis` is unaffected. The FDA LYRICA label PDF was lawfully downloaded (public-domain US federal content, SHA-256 logged, gitignored, not committed) but `llamaparse` failed 3 consecutive times (WriteTimeout/ConnectTimeout) while general network egress worked — a tool-specific issue, not a policy block. Instructing one further retry, then fallback to an unambiguously OA candidate (Frontiers 2026 combination SR-MA or Mallick-Searle 2024) if `llamaparse` remains down, per the PI directive's own fallback ordering.
- Taxonomy: `NO_CHANGE` (B3/B4/DOI accepted) + `VERIFIED_NEW_SENSITIVITY` (TDM-license decline is a new, generalizable rule: no PDF under a text/data-mining restriction may be bulk-downloaded/parsed by any peer without written permission, regardless of the PI directive's general intent).
- Reason: Declining to override a publisher's explicit TDM restriction is required by CLAUDE.md's full-text policy (lawful routes only) even though the PI directive asked for a downloaded+parsed PDF — the PI directive's intent (demonstrate lawful acquisition capability) is best served by a fully-unrestricted OA source, not by pushing past a license the ADA has explicitly stated. This is a `BLOCKED_FOR_PI`-adjacent judgment call resolved in favor of the more conservative, clearly-lawful reading without needing to actually block and ask, since an unambiguous OA fallback already exists.
- Affected files: `10_SOURCES/SOURCE_REGISTER.md`, `10_SOURCES/FULLTEXT_LEDGER.md` (peer-owned, already updated).
- Approved by: Research Director.

## Decision 2026-09-03-15 — PI requirement (Decision 2026-09-03-07) status: `BLOCKED_FOR_PI` — environment-level network block, not resolvable in-session

- Decision: Accept `dpnp-source-provenance`'s root-cause diagnosis and declare the PI's "download + LlamaParse-parse one lawful PDF" requirement **`BLOCKED_FOR_PI`** for this run, pending Human PI/operator action outside this session. Diagnosis (code-only inspection, no credential exposure): a bare, unauthenticated, zero-payload request to `api.cloud.llamaindex.ai` stalls/times out identically to the real parse attempts, while requests to other hosts (DailyMed, google.com) succeed normally in the same session — this is a categorical network-egress block to the LlamaParse API host, independent of file size/content. Declined the peer's optional confirming test on a second PDF (Frontiers SR-MA) as not diagnostically useful, since a zero-payload request already reproduces the stall — correct call, avoids wasting a lawful download for a near-certain repeat failure with no new information.
- Taxonomy: `BLOCKED_FOR_PI` (not `NEEDS_ANALYST` — this is an infrastructure/network-allowlist condition, not a research judgment call, and not fixable by any peer's own effort)
- Reason: The requirement specifically named the `llamaparse` MCP; per Decision 2026-09-03-07's own instruction, no local parser (pdftotext, etc.) may silently substitute for "LlamaParse-parsed," and `dpnp-source-provenance` correctly did not do so. This is the correct, honest outcome per Golden Rule 7 (BLOCKED is a valid research outcome) — the alternative (fabricating success, or quietly declaring the requirement satisfied via a substitute tool) would misrepresent what was actually verified.
- Mitigation already in place: the FDA label's substantive content is fully captured via direct WebFetch/manual extraction in `LABELING_FDA.md` (Decision 2026-09-03-09) and used in `40_SYNTHESIS/`; the PI's underlying evidentiary need (verified lawful full-text label content) is met even though the specific LlamaParse-parse step is not.
- Affected files: `04_OPEN-QUESTIONS.md`, `05_STATUS.md`. **This blocker is surfaced directly to the Human PI and must remain open in `99_FINAL-QA.md`/Final Gate until the PI either (a) confirms network access is restored and authorizes a retry, or (b) explicitly waives this requirement for this run.**
- Approved by: Research Director (escalated, not unilaterally resolved).

## Decision 2026-09-03-16 — Gate 3: READY_FOR_AUDIT

- Decision: Both required Wave 3 deliverables are complete — `40_SYNTHESIS/DPNP_Pregabalin_Moderator_Brief_zh-TW.md` (7 sections: sponsor disclosure, executive summary, diagnosis/differential pathway, guideline comparison, treatment algorithm, Pregabalin efficacy/safety/implementation, controversies/sponsor-bias checklist, citation table) and `40_SYNTHESIS/DPNP_10_Insightful_QA_zh-TW.md` (exactly 10 questions, each with why-it-matters/model answer/evidence-and-uncertainty/follow-up probe). Director self-check performed before declaring Gate 3: (a) grepped both files for any `MEDNOTE` citation — none found, confirming the non-negotiable rule that MEDNOTE numeric/diagnostic claims never entered synthesis; (b) confirmed all "reverse nerve damage" language is used only in the negating/guardrail direction, per Charter; (c) cross-checked recurring numeric tokens (NNT 8.9/4.6/7.4, MD −1.82, P=0.370, OR 1.40, aIRR 2.92) appear identically in both synthesis files and trace to the merged evidence tables — no drift, no rounding.
- Taxonomy: `READY_FOR_AUDIT` (Gate 3 status, per Human PI's explicit instruction to use this Gate to hand off to the independent auditor now rather than wait on the unrelated LlamaParse blocker)
- Reason: Per Human PI direction (2026-09-03): work not blocked by the LlamaParse network issue must continue; the LlamaParse requirement (Decision 2026-09-03-07/-15) remains open and is NOT waived, and Final Gate may not be marked fully passed while it stands. Gate 3 concerns internal consistency of the synthesis, which is independent of that infrastructure blocker.
- Affected files: `05_STATUS.md`.
- Approved by: Research Director, per explicit Human PI instruction.

## Decision 2026-09-03-17 — Independent audit accepted (`PASS_WITH_MINOR_ISSUES`); two findings fixed; Final Gate = `READY_WITH_EXTERNAL_BLOCKER`

- Decision: Accept the independent read-only auditor's report (`99_FINAL-QA.md`, written by a temporary, read-only agent with no access beyond that one file). Research-quality verdict: `PASS_WITH_MINOR_ISSUES`. All six specifically-mandated sponsor-bias/evidence checks passed with zero exceptions; 8/8 spot-checked DOIs/PMIDs (including the load-bearing AAN 2011 `[RETIRED]` tag) independently resolved correctly via Europe PMC; zero MEDNOTE leakage confirmed independently; exactly 10 QA items confirmed. Two findings accepted and fixed directly in the Director-owned synthesis files (auditor has no write access to fix them itself): (a) **MODERATE** — a dose-stratified AE figure ("29%/16% at 600 mg/day") in the Brief did not trace to any locator in `LABELING_FDA.md`/`LABELING_TFDA.md`, which explicitly self-caveat that dose-stratified figures were not transcribed; struck from the Brief, replaced with only the already-`ACCESS_VERIFIED` All-PGB figures (21%/12%) plus an explicit note of why the dose-stratified number was removed rather than silently dropped. (b) **MINOR** — OPTION-DM's N was compressed in a way that dropped the N=140-randomised top line in both synthesis files; corrected to state the full N=140→130→84 funnel in both.
- Taxonomy: `VERIFIED_AND_REPLACE` (both findings — numeric/wording correction with the change and reason disclosed, not silently smoothed over)
- Reason: Golden Rule 8 (never silently repair) requires disclosing what was struck and why rather than just deleting it; the auditor's own file:line evidence made both corrections high-confidence (not judgment calls) — the sibling unlocated figures in `SAFETY_TOPICS.md` (edema/ataxia dose-stratified numbers, which never reached synthesis) are routed back to `dpnp-pregabalin-safety` for its own file, not fixed by the Director since that file is peer-owned.
- **Final Gate status: `READY_WITH_EXTERNAL_BLOCKER`** — not `FINAL`, not plain `PASS`. Research quality is `PASS_WITH_MINOR_ISSUES` (now fully addressed by this decision), but per explicit Human PI instruction, the run cannot be marked fully passed/FINAL while the LlamaParse network blocker (Decision 2026-09-03-15) remains open. This status will be revisited only when the Human PI confirms network access is restored (permitting a retry) or explicitly waives the requirement.
- Affected files: `40_SYNTHESIS/DPNP_Pregabalin_Moderator_Brief_zh-TW.md`, `40_SYNTHESIS/DPNP_10_Insightful_QA_zh-TW.md`, `05_STATUS.md`.
- Approved by: Research Director.
