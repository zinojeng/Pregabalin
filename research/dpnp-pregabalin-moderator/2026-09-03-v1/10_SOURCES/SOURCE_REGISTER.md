# Source / Search Register — Wave 1

Owner: `dpnp-source-provenance`. Last updated: 2026-09-03 (Asia/Taipei). Access date for all entries below is 2026-09-03 unless noted.

## Verification status legend

- `ACCESS_VERIFIED` — this session directly opened/fetched the resource and captured its content.
- `IDENTIFIED_MULTI_SNIPPET` — bibliographic identity corroborated by ≥2 independent search-result snippets (title/journal/date/DOI or PMID agree), but this session has not yet opened the primary page/PDF directly. Treat as a strong lead, not yet an accepted citation.
- `IDENTIFIED_SECONDARY_CITATION` — found only inside another paper's reference list or a press release; not yet independently located/opened at its own primary record. Weakest tier — do not cite without direct verification.
- `NOT_YET_SEARCHED` — a required source class from `02_SOURCE-INVENTORY.md` with no search attempt completed this wave (tool interruption/failure), an explicit open gap.

No entry below should be treated as an accepted citation for `40_SYNTHESIS/` until the owning specialist (`dpnp-guideline-diagnosis`, `dpnp-trials-comparative`, or `dpnp-pregabalin-safety`) has opened the primary record directly and logged the exact quotation/locator.

---

## A. Context inputs (already logged in `02_SOURCE-INVENTORY.md`)

| ID | Source | Status this wave |
|---|---|---|
| MEDNOTE-001 | 糖尿病神經病變 臨床表現與診斷評估 | `ACCESS_VERIFIED` — full capture in `MEDNOTE_CAPTURE.md` |
| MEDNOTE-002 | 糖尿病神經病變管理：藥物與非藥物治療策略 | `ACCESS_VERIFIED` — full capture in `MEDNOTE_CAPTURE.md`; fallback acquisition was not needed, direct WebFetch succeeded |

## B. Guideline / regulatory sources (candidates for `dpnp-guideline-diagnosis`)

### B1. ADA Standards of Care in Diabetes—2026, Chapter 12 (Retinopathy, Neuropathy, and Foot Care)

- Status: `IDENTIFIED_MULTI_SNIPPET`
- Corroborating sources (independent, converging on same recommendation numbering/wording):
  - PMC full text: https://pmc.ncbi.nlm.nih.gov/articles/PMC12690177 (title: "12. Retinopathy, Neuropathy, and Foot Care: Standards of Care in Diabetes—2026")
  - PubMed record: https://pubmed.ncbi.nlm.nih.gov/41358886 — "Standards of Care in Diabetes-2026." *Diabetes Care.* 2026 Jan 1;49(Suppl 1):S261–S276. Author: ADAPP Committee. DOI shown truncated in search snippet as `10.2337…` — **full DOI not yet confirmed, do not fabricate the suffix.**
  - Guideline Central mirror: https://www.guidelinecentral.com/guideline/14119
  - Publisher PDF mirror (secondary host, for cross-check only, not a substitute for the PMC/journal version): https://www.binasss.sa.cr/standards-of-care-2026.pdf
- Content already surfaced in snippets (needs direct page open + locator before citation):
  - Rec 12.20: glucose/weight/BP/lipid management to prevent/slow neuropathy (grades C/B)
  - Rec 12.21: assess and treat pain related to DPN (B) and autonomic neuropathy symptoms (E) to improve QoL
  - Rec 12.22: gabapentinoids, SNRIs, TCAs, and sodium-channel blockers recommended as initial pharmacologic treatments for diabetic neuropathic pain (A); combinations may provide additional relief (A); opioids incl. tramadol are addressed separately (AAN referenced against opioids except rare circumstances)
  - Rec 12.17–12.19: annual DSPN/autonomic-neuropathy screening timing and methods (10-g monofilament, 128-Hz tuning fork, temperature/pinprick, Ipswich touch test now cross-referenced)
  - Reference list includes: Freeman R et al., pregabalin 7-RCT dose-range analysis, *Diabetes Care* 2008;31:1448–1454 (candidate trials-comparative source, see C1); Goodwin B et al., topical capsaicin narrative SR, *Pain Manag* 2023;13:309–316; Bril V, England J, Franklin GM, et al. (AAN 2011 guideline authorship — likely predecessor to the 2022 update, see B2)
- **Action needed (not this session):** open the PMC or PubMed record directly, capture exact DOI, and pull recommendation 12.20–12.22 verbatim with page/section locator before any citation in synthesis.

### B2. AAN Practice Guideline Update — Oral and Topical Treatment of Painful Diabetic Polyneuropathy (2022)

- Status: `IDENTIFIED_MULTI_SNIPPET`
- Citation as found (via a citing paper's reference list, corroborated by two independent AAN press releases and one review-of-guidelines paper):
  - Price R, Smith D, Franklin G, Gronseth G, Pignone M, David W, et al. "Oral and topical treatment of painful diabetic polyneuropathy: practice guideline update summary: report of the AAN guideline subcommittee." *Neurology.* 2022;98:31–43. DOI: 10.1212/WNL.0000000000013038
  - Published online ahead of print 2021-12-27 per AAN press releases (https://www.aan.com/PressRoom/Home/PressRelease/4944 and /935); endorsed by AANEM; lead/senior author includes Brian C. Callaghan, MD, MS (University of Michigan); updates the 2011 AAN guideline
- Content already surfaced (needs direct verification against the Neurology article itself, not press releases):
  - Recommended classes: TCAs (amitriptyline, nortriptyline, imipramine), SNRIs (duloxetine, venlafaxine, desvenlafaxine), gabapentinoids (gabapentin, pregabalin), sodium-channel blockers (carbamazepine, oxcarbazepine, lamotrigine, lacosamide) — sodium-channel blockers newly added vs the 2011 version
  - Recommends against opioids except rare circumstances (Level B)
  - Recommends screening for mood/sleep disorders before selecting treatment (Level B)
  - Recommends offering a different effective class if initial therapy fails/is not tolerated (Level B)
- **Action needed (not this session):** open the Neurology 2022;98:31–43 record directly (PubMed/AAN/journal), confirm DOI and exact recommendation wording/grades, and reconcile with the Bril et al. AAN 2011 predecessor guideline referenced inside the ADA 2026 chapter (B1) to determine which wording is currently operative — this maps directly to `04_OPEN-QUESTIONS.md` item on AAN/superseding updates.

### B3. Taiwan TFDA / other national regulator Pregabalin label and safety communications

- Status: `NOT_YET_SEARCHED`
- Reason: search for "台灣 食藥署 Pregabalin Lyrica 仿單" was interrupted this wave before results returned (user directive to stop further Tavily calls this turn).
- Action needed: repeat this search in the next working turn; also check TFDA (衛生福利部食品藥物管理署) 藥物許可證查詢 and the Taiwan Lyrica package insert directly.

### B4. FDA Lyrica (pregabalin) prescribing information

- Status: `NOT_YET_SEARCHED`
- Reason: search was auto-backgrounded and then failed (`Tavily API error: read ETIMEDOUT`) this wave.
- Action needed: repeat search for FDA label via DailyMed (dailymed.nlm.nih.gov) or accessdata.fda.gov directly next turn; DailyMed is generally the fastest lawful primary route for current FDA label text/dosing tables/renal-adjustment tables.

### B5. Diagnostic consensus for DSPN / small-fiber neuropathy (red flags, atypical features)

- Status: `NOT_YET_SEARCHED`
- Note: Toronto Consensus (Tesfaye et al. 2010, *Diabetes Care*) is referenced as a lead inside both MEDNOTE-001 and MEDNOTE-002 and inside the ADA chapter's neighborhood — treat as the primary target to verify next, since it already appears three times independently.

## C. Trials / comparative-effectiveness sources (candidates for `dpnp-trials-comparative`)

### C1. Freeman R, Durso-Decruz E, Emir B. "Efficacy, safety, and tolerability of pregabalin treatment for painful diabetic peripheral neuropathy: findings from seven randomized, controlled trials across a range of doses." *Diabetes Care.* 2008;31:1448–1454.

- Status: `IDENTIFIED_SECONDARY_CITATION` (found inside the ADA 2026 chapter's reference list, ref #104 in the snippet)
- Note: author list in the snippet was truncated/garbled by the search extractor — do not treat "Efficacy, safety, and tolerability..." authorship as confirmed until the PubMed/journal record is opened directly.

### C2. Soliman N, Moisset X, Ferraro M, et al. "Pharmacotherapy and non-invasive neuromodulation for neuropathic pain: a systematic review and meta-analysis." *Lancet Neurol.* 2025;24:413–428. DOI: 10.1016/S1474-4422(25)00068-7

- Status: `IDENTIFIED_SECONDARY_CITATION` (found inside a 2026 Frontiers article's reference list, ref #20)

### C3. Mallick-Searle T, Adler JA. "Update on treating painful diabetic peripheral neuropathy: a review of current US guidelines with a focus on the most recently approved management options." *J Pain Res.* 2024;17:1005–1028. DOI: 10.2147/JPR.S442595

- Status: `IDENTIFIED_SECONDARY_CITATION` (found inside the same Frontiers article's reference list, ref #19) — narrative review, not primary trial evidence; useful as a guideline-landscape summary only if independently confirmed.

### C4. Frontiers in Endocrinology (2026) — pregabalin + duloxetine combination systematic review/meta-analysis

- Status: `IDENTIFIED_MULTI_SNIPPET` (content directly quoted in search snippet, page not yet opened by this session)
- URL: https://www.frontiersin.org/journals/endocrinology/articles/10.3389/fendo.2026.1750441/full
- DOI: 10.3389/fendo.2026.1750441
- SR registration: PROSPERO/INPLASY-style identifier CRD420251179997 (exact registry not confirmed from snippet alone)
- Snippet-reported conclusion: "Low-certainty evidence suggests that pregabalin plus duloxetine may improve short-term pain scores compared with monotherapy in painful diabetic neuropathy. Safety outcomes remain uncertain due to few trials and imprecision."
- Snippet-reported included-study example: QI 2022, n=51 vs 51, mean age ~66–68y, pregabalin 75mg BID + duloxetine 30mg BID vs duloxetine 30mg BID alone, 4-week treatment period, outcomes NRS/VAS/adverse events.
- Full text: Frontiers is gold/hybrid open access — lawful full-text route is the publisher page itself (no paywall expected); confirm license (likely CC-BY) before any extended quotation.
- Trial names referenced in MEDNOTE-002 (COMBO-DN, OPTION-DM) are candidate primary RCTs for head-to-head/combination-strategy evidence — not yet searched at their own primary registry/publication; hand off to `dpnp-trials-comparative` as named leads.

## D. Open coverage gaps at end of Wave 1 (source-provenance scope)

1. Taiwan TFDA and any major non-US regulator (EMA) Pregabalin label/safety communication — not yet searched (see B3).
2. FDA DailyMed/accessdata Pregabalin label — search attempted, failed on tool timeout, not retried this wave (see B4).
3. Exact/complete DOI for the ADA Standards of Care 2026 Chapter 12 record — truncated in all snippets obtained so far (see B1).
4. Direct primary-record confirmation (not press release or citing-paper reference list) for the AAN 2022 guideline (B2), Freeman 2008 (C1), Soliman 2025 (C2), and Mallick-Searle 2024 (C3).
5. Toronto Consensus (Tesfaye et al. 2010) primary citation not yet independently pulled, despite appearing as a lead in three places.
6. COMBO-DN and OPTION-DM trials named in MEDNOTE-002 not yet located at their own primary publications.
7. Numeric claims in `MEDNOTE_CAPTURE.md` (incidence/prevalence/NNT/NNH/discontinuation figures) have no primary citation attached yet.
8. No systematic search yet run for a current DSPN/small-fiber-neuropathy diagnostic consensus statement distinct from Toronto Consensus (e.g., any 2020s update).

None of the above gaps should be read as blocking downstream specialists from starting guideline/diagnosis or trials/comparative work on the leads already identified — they should independently open and verify the specific primary records listed above rather than waiting for source-provenance to do it a second time, per role-ownership boundaries. Source-provenance will continue closing B3/B4 and the DOI/primary-record gaps in the next turn.
