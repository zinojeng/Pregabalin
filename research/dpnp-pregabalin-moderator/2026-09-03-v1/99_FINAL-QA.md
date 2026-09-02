# Independent Final QA

PROJECT: `dpnp-pregabalin-moderator` | RUN: `2026-09-03-v1` | Audit date: 2026-09-03 (Asia/Taipei)
Auditor role: independent, read-only, temporary. Reviewed the full run tree (`CLAUDE.md`, Runbook, `00`–`05` control files, `10_SOURCES/`, `20_EVIDENCE/*`, `30_METHODS/`, `40_SYNTHESIS/*`, `90_CROSS-SESSION-LOG/`) plus `git log`/`git show` for provenance cross-checks, and spot-verified 8 primary-record DOIs/PMIDs via Europe PMC. No file other than this one was written.

---

## 1. Summary verdict

**Research-quality verdict: `PASS_WITH_MINOR_ISSUES`.**

The evidence base is disciplined, well-tiered, and unusually resistant to sponsor bias for a sponsor-commissioned brief: both currently-operative guidelines are correctly framed as class-level (not pregabalin-specific) recommendations; the retired 2011 AAN pregabalin-specific Level A is never presented without its retirement status; the two head-to-head RCTs (COMBO-DN, OPTION-DM) are consistently and correctly reported as null/no-significant-difference rather than "pregabalin inferior" or "pregabalin superior"; the Soliman/NeuPSIG NNT is never stripped of its class-pooled qualifier; the respiratory-depression reassuring PK/PD finding is never cited without the broader case-report/postmarketing warning in the same breath; MEDNOTE-001/002 numeric or diagnostic content does not leak into either synthesis file (independently grepped, zero hits); and the compounded-risk callout and documentation-depth-asymmetry guardrail are both present and correctly labeled `EXPERT INTERPRETATION`, not `DIRECT EVIDENCE`. Eight spot-checked DOIs/PMIDs (including the load-bearing AAN 2011 `[RETIRED]` tag) all resolved to the claimed title/journal/year with no mismatch.

One `MODERATE` numeric-traceability gap was found (a dose-stratified adverse-event figure in the Brief that does not trace to a locator in the committed evidence files) and one `MINOR` simplification (OPTION-DM's N reported incompletely). Neither materially changes any clinical conclusion or sponsor-bias framing; both are correctable without re-opening Gate 2. See §2 for detail and a specific fix for each.

**This verdict is separate from, and does not waive, the disclosed LlamaParse network blocker (Decision 2026-09-03-15).** See §6 — that blocker is confirmed honestly and prominently disclosed, per explicit Human PI instruction, and is not something this audit is grading or has authority to close.

---

## 2. Findings by category

### 2.1 Numbers

- **[MODERATE] Untraceable dose-stratified AE figure in the Brief.** `40_SYNTHESIS/DPNP_Pregabalin_Moderator_Brief_zh-TW.md:187` states "頭暈 21%（安慰劑 5%）；嗜睡 12%（安慰劑 3%）——600 mg/day 時上升至 29%/16%." The 21%/5% and 12%/3% "All PGB" figures trace exactly to `20_EVIDENCE/pregabalin-safety/LABELING_FDA.md:68` and `LABELING_TFDA.md:86` (both `ACCESS_VERIFIED`, page-cited). The "29%/16% at 600 mg/day" clause does **not** appear in either labeling file — `LABELING_FDA.md:68` explicitly states "(full dose-stratified table preserved in source PDF; do not re-derive figures not listed here without re-opening the source)," i.e., the specialist's own committed extraction flags that dose-stratified numbers were deliberately *not* transcribed. The figure instead first appears in `20_EVIDENCE/pregabalin-safety/SAFETY_TOPICS.md:15` ("rising to 29%/16% at 600 mg/day") with no page/table locator, and from there flowed into the final Brief with no locator either. Two sibling figures in the same `SAFETY_TOPICS.md` file (edema "rising to 12% at 600 mg/day," `SAFETY_TOPICS.md:28`; ataxia "rising to 7% at 600 mg/day," `SAFETY_TOPICS.md:19`) have the identical provenance gap, though they were not carried into either synthesis file and so are noted here as an evidence-layer issue rather than a synthesis-layer one.
  This is not evidence of fabrication — the specialist states elsewhere that the PDF was read "page by page" — but it fails this project's own non-negotiable rule ("every important claim must be traceable to a primary source with ... page/table/section when available") and its own file's explicit self-caveat. **Recommended fix:** either (a) `dpnp-pregabalin-safety` re-opens the FDA label PDF, adds the dose-stratified row(s) with a page/table locator to `LABELING_FDA.md`/`LABELING_TFDA.md`, and the figure stands; or (b) if not re-verified before dissemination, strike "——600 mg/day 時上升至 29%/16%" from the Brief and leave the already-verified "21%（安慰劑 5%）；12%（安慰劑 3%）" All-PGB figures, which are fully traceable on their own.

- **[MINOR] OPTION-DM sample size reported incompletely, not incorrectly.** `20_EVIDENCE/trials-comparative/01_EVIDENCE-TABLE.md` (T6) reports "N = 140 randomised, 130 started a pathway, 84 completed ≥2 pathways (analysed for primary outcome)." The Brief (§4.2) and QA (Q3) both compress this to "N=130 完成分析 84 人" / "完成雙路徑分析者僅 84 人," dropping the top-line N=140 randomised. The numbers used (130, 84) are themselves accurate and not fabricated or drifted, but the compression could read as if only 130 were ever enrolled. **Recommended fix:** state "N=140 randomised（130 人開始至少一個治療路徑，84 人完成 ≥2 路徑並納入主要療效分析）" if the Brief is revised again; not blocking as-is.

- All other load-bearing statistics checked — Soliman/NeuPSIG NNT/NNH (TCA 4.6/17.1, α2δ-ligands 8.9/26.2, SNRI 7.4/13.9), AAN 2022 SMDs (0.44/0.47/0.56/0.62/0.95 with their CIs), COMBO-DN (P=0.370, P=0.068, P<0.001), OPTION-DM pathway comparisons (all three mean differences and 98.3% CIs), Frontiers 2026 combination SR-MA (MD −1.82, 95% CI −2.10 to −1.54; 3 RCTs/471 patients/2 poolable), FDA/TFDA renal dosing table (all four CLcr bands, mg-for-mg), thiazolidinedione interaction figures (19%/7.5% vs 8%/4% vs 3%/0%), Yuen 2026 aIRR figures (2.92, 0.84, 3.15, 1.91), and Scott 2024 OR (1.40, 95% CI 1.18–1.66) — **all traced exactly (same digits, same units, same CIs) to their respective `20_EVIDENCE/` source, with no rounding or drift**, and Decision 2026-09-03-16's self-reported cross-check of these same tokens is independently confirmed correct.

### 2.2 Methods/Evidence

All six specific checks in the audit brief were run and passed with **zero exceptions found**:

- (a) No sentence anywhere in `40_SYNTHESIS/` states or implies a current drug-specific "Grade A"/"Level A" for pregabalin without explicitly flagging the 2011 AAN guideline as retired/historical (verified by direct reading plus targeted `grep` for every "Grade A"/"Level A" occurrence in both files — 8 hits, all correctly qualified).
- (b) The Soliman/NeuPSIG NNT 8.9 never appears without its "α2δ-ligands, pooling gabapentin and pregabalin" qualifier (verified by `grep` for "8.9" — 4 substantive hits across both files, all qualified).
- (c) No sentence overstates COMBO-DN/OPTION-DM's non-significant findings into "pregabalin proven inferior" or a superiority claim; both are consistently and correctly framed as "no significant difference" (Brief §4.2, §7; QA Q3).
- (d) No sentence cites the respiratory-depression PK/PD reassuring finding (oxycodone/lorazepam/ethanol study, "no clinically important effects on respiration") without the broader case-report/postmarketing warning in the same breath (Brief §5.5; QA Q5 — both pair the two explicitly and instruct that they "應併陳，不得僅引用其一").
- (e) Zero MEDNOTE-001/002 citations or numeric/diagnostic claims found anywhere in `40_SYNTHESIS/` — confirmed independently via `grep -rni "mednote"` (no hits) and a targeted search for MEDNOTE-only figures (300 million by 2045, 71% ten-year mortality, 221-day Taiwan discontinuation, 10-kHz SCS 79%/5%) — none present.
- (f) Both the compounded-risk callout (elderly + reduced renal function + concurrent CNS-depressant/diuretic/thiazolidinedione use) and the documentation-depth-asymmetry guardrail are present in the Brief (§5.5, opening warning box and the dedicated paragraph before §6) and correctly labeled `EXPERT INTERPRETATION`, matching Decisions 2026-09-03-06/-08/-10/-12 in framing and substance, not merely referenced in the decision log without synthesis-side follow-through.

### 2.3 Writing

- Executive summary (§1) is fully consistent with the body sections that follow it; no claim in §1 is contradicted or unsupported downstream.
- No unsupported causal/disease-modifying language about pregabalin was found. The Charter-mandated "no reversal of nerve damage" statement is present in both files (Brief §2.4, §Sponsor disclosure header; QA Q7) and is used only in the negating/guardrail direction — verified by `grep` for "逆轉" (4 hits, all correctly framed as denials of a reversal effect).
- No stale or internally contradicted numeric values were found between the Brief and the QA file (see §2.1 cross-check).
- The sponsor-bias checklist (Brief §6.2, 9 items) was checked item-by-item against what the brief actually does elsewhere in the document — all 9 items are backed by a corresponding enforced practice in the body (e.g., item 1 ↔ the 2011-retirement framing throughout §3.1/§7; item 2 ↔ the NNT-qualifier discipline in §5.2; item 5 ↔ the documentation-depth-asymmetry box in §5.5), not a checklist that exists only on paper.
- Exactly 10 QA questions are present (independently counted via `grep -c "^## Q"` = 10), each with all four required components (why it matters / model answer / evidence-and-uncertainty / follow-up probe).
- No unresolved template placeholders found in either synthesis file.

### 2.4 Provenance

Eight of the most load-bearing DOIs/PMIDs cited in the Brief's §7 citation table were independently spot-checked via Europe PMC (chosen for reliability, since PubMed itself returned a cookie-consent wall to WebFetch): AAN 2011 (PMID 21482920 — **independently confirmed `[RETIRED]` in title**, the single most sponsor-bias-critical fact in the whole brief), AAN 2022 (PMID 34965987), ADA 2026 Ch.12 (PMID 41358886, DOI 10.2337/dc26-s012), Soliman/NeuPSIG 2025 (PMID 40252663), COMBO-DN (PMID 23732189), OPTION-DM (PMID 36007534), Toronto Consensus 2010 (PMID 20876709), and Freeman 2008 (PMID 18356405). **All eight resolved to the exact title, journal, and year claimed in the citation table, with zero mismatches.** No fabricated or misattributed citation was found in this sample. (Not exhaustive — G5/Atmaca 2024, S1–S4 were not independently re-resolved this pass, but were already `ACCESS_VERIFIED` with PMIDs recorded by the owning specialists and are lower-stakes for the sponsor-bias question this audit prioritized.)

### 2.5 Process integrity — LlamaParse blocker disclosure

**Confirmed: honestly and prominently disclosed, not buried, not silently waived.** `05_STATUS.md`'s Current Gate line (line 5) states in bold, before any other content: "Final Gate will NOT be marked FINAL/PASS while the LlamaParse network blocker (Decision 2026-09-03-15) stands — per explicit Human PI instruction, this requirement is not waived." The same file's "Residual blocker" section (lines 50–52) gives the full root-cause diagnosis, the exact remediation path (restore network egress to `api.cloud.llamaindex.ai`, then retry parsing the already-downloaded FDA label PDF), and the interim mitigation already in place. `03_DECISION-LOG.md` carries the full diagnostic chain across four linked decisions (2026-09-03-07 the original PI directive, -14 the TDM-license-driven fallback reasoning, -15 the network root-cause and `BLOCKED_FOR_PI` declaration, -16 Gate 3's explicit statement that this blocker is separate from and does not resolve via Gate 3). `04_OPEN-QUESTIONS.md` also carries a matching entry requiring an explicit Human PI decision. This is a textbook case of Golden Rule 7 ("BLOCKED is a valid research outcome") being honored rather than smoothed over — no finding.

---

## 3. Recommended Final Gate status

**`PASS_WITH_MINOR_ISSUES`** — for research quality, independent of the LlamaParse blocker.

Basis: one `MODERATE` finding (an untraceable dose-stratified figure that should be either sourced with a locator or removed before wide dissemination — §2.1) and one `MINOR` finding (an incomplete-but-not-incorrect sample-size compression — §2.1), against an otherwise clean pass across all six specifically-mandated evidence/bias checks (§2.2), writing consistency (§2.3), and provenance spot-checks (§2.4). Neither finding invalidates any clinical conclusion, sponsor-bias guardrail, or evidence classification in the brief.

**This verdict does not address, waive, or downgrade the LlamaParse network blocker (Decision 2026-09-03-15).** That blocker remains open, is correctly and prominently disclosed as required, and is a matter for the Human PI to close (confirm network egress restored and authorize a retry, or explicitly waive the requirement) — not something this audit has the standing to resolve or penalize the research quality for.

---

## 4. Auditor scope note

This file is the only file the auditor wrote. No other file in the run tree was modified. No `git` state-changing command was run. Eight DOI/PMID resolutions used Europe PMC's public API via WebFetch (PubMed itself returned a cookie-consent interstitial to the fetch tool); no other external verification was performed this pass.
