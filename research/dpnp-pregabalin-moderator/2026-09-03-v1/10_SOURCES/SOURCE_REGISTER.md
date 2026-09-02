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

- Status: `ACCESS_VERIFIED` (PMC record itself opened directly by source-provenance for bibliographic/licensing purposes per Director's full-text-acquisition directive; recommendation-text verbatim/locator work for citation purposes remains owned by `dpnp-guideline-diagnosis` — not duplicated here)
- Confirmed bibliographic record (opened directly, 2026-09-03):
  - American Diabetes Association Professional Practice Committee for Diabetes. "12. Retinopathy, Neuropathy, and Foot Care: Standards of Care in Diabetes—2026." *Diabetes Care.* 2025 Dec 8;49(Suppl 1):S261–S276.
  - **DOI (confirmed): 10.2337/dc26-S012**
  - **PMID: 41358886** · **PMCID: PMC12690177**
  - Publisher: American Diabetes Association
  - URL: https://pmc.ncbi.nlm.nih.gov/articles/PMC12690177
  - **License (verbatim):** "© 2025 by the American Diabetes Association. Readers may use this work for educational, noncommercial purposes if properly cited and unaltered." Also states: "This publication and its contents may not be reproduced, distributed, or used for text or data mining, machine learning, or similar technologies without prior written permission."
  - **Full-text/PDF-parse implication:** the explicit no-TDM/no-ML clause means this PDF must NOT be run through LlamaParse or any similar automated extraction tool without ADA's prior written permission — see `FULLTEXT_LEDGER.md` (BLOCKED for bulk parsing; direct human-style reading/short verbatim quotation under the educational/noncommercial clause remains permitted).
- Note: `02_SOURCE-INVENTORY.md`'s original PubMed-snippet date ("2026 Jan 1") differs slightly from the PMC page's own citation date ("2025 Dec 8") for the same article — both refer to the same DOI/PMID; flagging per the non-negotiable rule against silently repairing discrepancies rather than picking one.
- Other corroborating mirrors (not opened, for cross-check only):
  - Guideline Central mirror: https://www.guidelinecentral.com/guideline/14119
  - Third-party PDF mirror (not authoritative, do not cite in place of PMC/journal): https://www.binasss.sa.cr/standards-of-care-2026.pdf
- Content already surfaced in snippets (still needs direct page open + locator before citation by the owning specialist):
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

- Status: `PARTIALLY_VERIFIED` — one regulatory safety communication `ACCESS_VERIFIED`; the current full package-insert (仿單) text is still an unresolved gap.
- `ACCESS_VERIFIED` (opened directly, 2026-09-03): 食品藥物管理局 (now 衛生福利部食品藥物管理署) safety communication, "食品藥物管理局提醒醫療人員及病患使用Lyrica藥物可能導致自殺意念或企圖之副作用." Published 2010-07-15/16 (page shows both "建檔日期：99-07-15" and a "July 16, 2010" rendering — dates differ by a day across two independently fetched pages, flagging rather than reconciling). Drug: Pregabalin / Lyrica (利瑞卡膠囊). License numbers: 衛署藥輸字第024955、024956、024957號. Content: warns of possible suicidal ideation/attempt risk with pregabalin (antiepileptic-class signal), instructs physicians to inform patients and monitor behavior. URLs: https://www.fda.gov.tw/tc/siteListContent.aspx?id=3127 and mirrored at https://www.mohw.gov.tw/cp-16-26335-1.html.
- **Caveat:** this is a 2010 safety alert, not the current TFDA-approved package insert/label full text, and its license numbers (024955-024957) may not match the currently marketed product's license number(s).
- `IDENTIFIED_MULTI_SNIPPET` (not yet opened directly): a distinct, apparently more current license — 衛部藥輸字第027054號 (via a military/dependent-pharmacy formulary listing, reg.802.mnd.gov.tw) — and hospital patient-education material (奇美醫療體系, chimei.org.tw) naming two currently dispensed Taiwan products: Lyrica 利瑞卡膠囊 75mg (藥號23P192) and Pregabalin Viatris 普痛佳寧膠囊 75mg (藥號23P225), both listing 糖尿病周邊神經病變所引起的神經性疼痛 among indications. These are secondary/derivative sources (formulary listing, hospital patient leaflet), not the primary TFDA license record — do not cite as the label itself.
- **Action needed (not this session unless re-dispatched):** open the TFDA drug-license query system (info.fda.gov.tw) directly for license 027054 (or the current Lyrica/普痛佳寧 license) to obtain the current, authoritative 仿單 text with exact indication wording and dosing table; reconcile against the 2010 alert's license numbers.

### B4. FDA Lyrica (pregabalin) prescribing information

- Status: `ACCESS_VERIFIED`
- Located via DailyMed public SPL index (https://dailymed.nlm.nih.gov/dailymed/services/v2/spls.json?drug_name=LYRICA), opened directly, 2026-09-03:
  - SPL setid: `60185c88-ecfd-46f9-adb9-b97c6b00a553`, spl_version 59, **SPL index published_date: 2025-09-29**
  - Page header itself (opened at https://dailymed.nlm.nih.gov/dailymed/lookup.cfm?setid=60185c88-ecfd-46f9-adb9-b97c6b00a553) displays **"Updated June 15, 2020"** — a discrepancy between the SPL index date and the page's own displayed update date; both are recorded here rather than silently reconciled. `dpnp-pregabalin-safety` should confirm which date reflects the operative label version before citing.
  - Manufacturer: Parke-Davis Div. of Pfizer Inc. Controlled substance schedule: CV.
  - Indications include: management of neuropathic pain associated with diabetic peripheral neuropathy, postherpetic neuralgia, adjunctive seizure therapy (≥1 month old), fibromyalgia, neuropathic pain from spinal cord injury.
  - Renal dose-adjustment table (CrCl bands ≥60 / 30–60 / 15–30 / <15 mL/min against 150/300/450/600 mg/day) captured verbatim in the fetch; full table to be re-verified by `dpnp-pregabalin-safety` directly against the PDF (see `FULLTEXT_LEDGER.md` — PDF downloaded this wave).
  - Key warnings captured: angioedema, respiratory depression w/ CNS depressants, antiepileptic-class suicidality signal (~2x), peripheral edema (6% vs 2% placebo), weight gain (≥7% gain in 9% vs 2% placebo), withdrawal/taper guidance (≥1 week), Schedule CV abuse/dependence potential.
  - Adverse reactions: dizziness 30% vs 8% placebo; somnolence 23% vs 8% placebo; peripheral edema 6% vs 2% placebo.
  - No boxed warning present on this label.
- **US federal regulatory content is not subject to US copyright (17 U.S.C. §105) — no TDM/license restriction applies; this is the source used for the PI-directed download+parse task (see `FULLTEXT_LEDGER.md`).**

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

## D. Open coverage gaps as of this update (source-provenance scope)

Closed since Wave 1 report: B1 DOI now confirmed (10.2337/dc26-S012) and its license captured; B3 has one `ACCESS_VERIFIED` TFDA/MOHW safety communication; B4 is `ACCESS_VERIFIED` with the FDA label content captured and the PDF downloaded (see `FULLTEXT_LEDGER.md`).

Still open:

1. Taiwan TFDA current package-insert (仿單) full text for the currently marketed Lyrica/普痛佳寧 product (license likely 衛部藥輸字第027054號 or a 23P19x/23P22x-series number) — only the 2010 suicidality alert is directly verified; no current label opened yet (see B3).
2. Any major non-US regulator beyond Taiwan/US (e.g., EMA SmPC) — not searched this run.
3. Direct primary-record confirmation (not press release or citing-paper reference list) for the AAN 2022 guideline (B2), Freeman 2008 (C1), Soliman 2025 (C2), and Mallick-Searle 2024 (C3) — now owned by `dpnp-guideline-diagnosis` / `dpnp-trials-comparative` per Director's Wave 2 dispatch; source-provenance will not re-open these.
4. Toronto Consensus (Tesfaye et al. 2010) primary citation not yet independently pulled, despite appearing as a lead in three places — owned by `dpnp-guideline-diagnosis` (B5) per Wave 2 dispatch.
5. COMBO-DN and OPTION-DM trials named in MEDNOTE-002 not yet located at their own primary publications — owned by `dpnp-trials-comparative` per Wave 2 dispatch.
6. Numeric claims in `MEDNOTE_CAPTURE.md` (incidence/prevalence/NNT/NNH/discontinuation figures) have no primary citation attached yet.
7. No systematic search yet run for a current DSPN/small-fiber-neuropathy diagnostic consensus statement distinct from Toronto Consensus (e.g., any 2020s update).
8. Two internal date discrepancies logged rather than silently reconciled: the ADA chapter's citation date on PMC (2025-12-08) vs. the earlier PubMed-snippet date (2026-01-01); and the FDA LYRICA SPL index date (2025-09-29) vs. the label page's own "Updated June 15, 2020" text.

Items 3–5 are explicitly owned by other specialists per the Director's Wave 2 dispatch; source-provenance will not duplicate that verification. Source-provenance continues to own items 1, 2, 6, 7, 8.
