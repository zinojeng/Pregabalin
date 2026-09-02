# Guideline / Diagnosis Claim Table — Wave 2

Owner: `dpnp-guideline-diagnosis`. Last updated: 2026-09-03 (Asia/Taipei). Access date for all entries below: 2026-09-03.

Scope this wave: verify the four leads dispatched by `dpnp-research-director` (WAVE2_DISPATCH) — ADA Standards of Care 2026 Ch.12, AAN 2022 update (+ reconciliation with the 2011 predecessor), Toronto Consensus 2010, and an own-initiative search for a 2020s DSPN diagnostic-consensus update. All four opened at their own primary/publisher record, not press releases or citing-paper reference lists. Verification method for each source is stated so the Director/auditor can audit provenance.

---

## Source G1 — ADA Standards of Care in Diabetes—2026, Chapter 12 (Retinopathy, Neuropathy, and Foot Care)

- **Citation:** ADA Professional Practice Committee. "12. Retinopathy, Neuropathy, and Foot Care: Standards of Care in Diabetes-2026." *Diabetes Care.* 2026 Jan;49(Suppl 1):S261. [page range as printed on PMC/journal landing page; full end page not independently confirmed this wave]
- **DOI:** `10.2337/dc26-S012` — confirmed two independent ways: (a) PubMed record via `paper-search` MCP (PMID 41358886, doi field matches); (b) `doi.org/10.2337/dc26-S012` HTTP redirect resolves to `diabetesjournals.org/care/article/49/Supplement_1/S261/163919/12-Retinopathy-Neuropathy-and-Foot-Care-Standards`. This resolves the source register's "truncated DOI, do not fabricate" flag — DOI is now `ACCESS_VERIFIED`, not fabricated.
- **PMID:** 41358886
- **Access route:** PMC full text (`pmc.ncbi.nlm.nih.gov/articles/PMC12690177`), opened directly this session.
- **Verification tier:** `ACCESS_VERIFIED` (primary record opened directly).

| # | Concise paraphrase of clinical substance | Grade | Evidence class | Locator |
|---|---|---|---|---|
| Rec 12.17 | T2D 自診斷時、T1D 診斷滿 5 年後開始篩檢 DPN，此後至少每年評估。 | B | GUIDELINE / CONSENSUS | Ch.12, Neuropathy screening subsection |
| Rec 12.18 | DSPN 評估包括病史、temperature 或 pinprick（small-fiber）、128-Hz tuning fork vibration（large-fiber），並每年做 10-g monofilament 以辨識足部潰瘍／截肢風險。 | B | GUIDELINE / CONSENSUS | ibid. |
| Rec 12.19 | 依糖尿病型別與病程定期評估 autonomic neuropathy；有其他 microvascular complications 時尤其注意。 | E | GUIDELINE / CONSENSUS | ibid. — full clause/qualifier mapping was not used verbatim in synthesis |
| Rec 12.20 | 最佳化 glucose management，以預防／延緩 T1D neuropathy，並減慢 T2D neuropathy progression；此為多子句、多 grade 建議。 | A / C / B (multi-part) | GUIDELINE / CONSENSUS | ibid. — exact clause-to-grade mapping not quoted in synthesis |
| Rec 12.21 | 評估並處理 DPN pain 與 autonomic symptoms，以改善生活品質。 | B (pain) / E (autonomic sx) | GUIDELINE / CONSENSUS | ibid. — supports pain/sleep/function/QoL rather than nerve-reversal framing |
| Rec 12.22 | 初始藥物類別包括 gabapentinoids、SNRIs、TCAs、sodium-channel blockers；除罕見例外，不使用 opioids（含 tramadol、tapentadol）。 | A (drug classes, pooled) / B (against opioids) | GUIDELINE / CONSENSUS | ibid. |

**Explicit no-reversal statement (Charter-relevant):** "Specific treatment to reverse the underlying nerve damage in diabetes is currently not available" — direct textual support for the Charter's non-negotiable rule against implying analgesic therapy reverses nerve damage. **Class: GUIDELINE / CONSENSUS.**

**Differential/red-flag statement (paraphrased):** 即使病人有 diabetes 與 DPN，仍須考慮 alcohol／toxins、chemotherapy 等 neurotoxic medications、vitamin B12 deficiency、hypothyroidism、kidney disease、malignancy、HIV／hepatitis C 等替代病因。Acute/subacute、non-length-dependent、asymmetric 或 motor-predominant presentation 應考慮轉介。**Class: GUIDELINE / CONSENSUS.**

⚠️ **Sponsor-bias-relevant finding:** Rec 12.22 recommends gabapentinoids, SNRIs, TCAs, and sodium-channel blockers as a **pooled class-level Grade A** option — it does **not** single out pregabalin (or any one drug) as preferred. This must not be paraphrased into a pregabalin-specific "Grade A" claim in synthesis.

⚠️ **Caveat on this table's own reliability:** Rec 12.19/12.20 substance was extracted via WebFetch reading the PMC page rather than raw PDF page images. The DOI and Rec 12.17/12.18/12.21/12.22 core substance was consistent across two independent tool calls and the source register, so confidence is HIGH for those. Rec 12.19 and the exact grade-to-clause mapping in 12.20 remain **lower confidence** and are not quoted verbatim in `40_SYNTHESIS/`. Logged rather than silently smoothed over, per CLAUDE.md's "never silently repair" rule.

---

## Source G2 — AAN 2022 Practice Guideline Update: Oral and Topical Treatment of Painful Diabetic Polyneuropathy

- **Citation:** Price R, Smith D, Franklin G, Gronseth G, Pignone M, David WS, Armon C, Perkins BA, Bril V, Rae-Grant A, Halperin J, Licking N, O'Brien MD, Wessels SR, MacGregor LC, Fink K, Harkless LB, Colbert L, Callaghan BC. "Oral and Topical Treatment of Painful Diabetic Polyneuropathy: Practice Guideline Update Summary: Report of the AAN Guideline Subcommittee." *Neurology.* 2022;98:31–43.
- **DOI:** `10.1212/WNL.0000000000013038`
- **PMID:** 34965987 — confirmed via `paper-search` MCP PubMed search; full author list matches source register lead exactly (previously only "Price/Franklin/Gronseth et al." was corroborated — now complete).
- **Access route:** (a) PubMed abstract (effect sizes, top-line Level B statements) — `ACCESS_VERIFIED`; (b) AAN's own lawfully-hosted clinician summary PDF (`aan.com/Guidelines/home/GetGuidelineContent/1055`), fetched directly and checked locally with `pdftotext`. **Full PDF stored locally only** at `20_EVIDENCE/guidelines-diagnosis/fulltext-local/AAN-2022-painful-DPN-guideline-summary.pdf` (gitignored) per AAN's "single copy for personal use" redistribution restriction. The committed table below is a concise paraphrase of the clinical substance and Level grades; it does not reproduce the full recommendation text.
- **Verification tier:** `ACCESS_VERIFIED` (primary record + own-society-published clinician summary, not a press release).

| Rec # | Concise paraphrase of clinical substance | Level |
|---|---|---|
| 1 | 評估 peripheral neuropathic pain，以及它對功能與生活品質的影響。 | B |
| 2 | 開始藥物治療時先設定務實目標：降低疼痛，不保證完全消除。 | B |
| 3 | 同步評估並處理 mood 與 sleep disorders。 | B |
| 4 | 可提供 TCAs、SNRIs、gabapentinoids 或 sodium-channel blockers 作為有效類別選項。 | B |
| 5 | 納入病人對 oral、topical、nontraditional 與 nonpharmacologic interventions 的偏好；原摘要列有 topical agents、CBT、exercise、Tai Chi、mindfulness 等例子。 | C |
| 6 | 因類別間療效相近，選藥應同時考慮不良反應、共病、成本與病人偏好。 | B |
| 6 (cont.) | 有生育可能者避免 valproic acid；其他病人亦不宜使用，除非多種有效藥物皆失敗且已衡量其嚴重風險。 | B |
| 7 | 事先說明可能需要依序試用數種藥物；足量治療約 12 週仍無具臨床意義的改善，或副作用大於效益，可視為失敗。 | B |
| 7 (cont.) | 初始類別無 meaningful improvement 或有顯著不良反應時，改試另一有效類別；部分改善時，可改試另一類別或加入不同類別做 combination therapy。 | B |
| 8 | 不以 opioids 治療；已使用者可討論安全 taper 與 nonopioid alternatives。 | B（不用）／C（taper option） |
| 9 | 不以 tramadol 或 tapentadol 治療；已使用者可討論安全 taper 與 nonopioid alternatives。 | C |

**Effect-size data (PubMed abstract, PMID 34965987; class-pooled, not drug-specific):**

| Drug class | SMD | 95% CI |
|---|---:|---|
| Gabapentinoids | 0.44 | 0.21–0.67 |
| SNRIs | 0.47 | 0.34–0.60 |
| Sodium-channel blockers | 0.56 | 0.25–0.87 |
| SNRI/opioid dual-mechanism agents | 0.62 | 0.38–0.86 |
| TCAs | 0.95 | 0.15–1.8 |

The first four estimates cluster around the guideline's medium-effect threshold; the TCA estimate is larger but markedly imprecise and rated with low confidence. **Class: DIRECT EVIDENCE** (meta-analytic synthesis underlying the guideline), reported at the **drug-class** level, not specific to pregabalin within the gabapentinoid class.

⚠️ **Sponsor-bias-relevant finding:** This is the current operative AAN recommendation, and it treats TCAs/SNRIs/gabapentinoids/sodium-channel blockers as an undifferentiated first-line tier (Level B, "offer…and/or"), explicitly stating comparable effect sizes make "recommendations for one [class] over another difficult." No pregabalin-specific superiority claim is supported by this source.

**Renal/edema/comorbidity content in this summary:** gabapentinoid-specific dose/renal-adjustment tables were **not** included in this clinician-summary PDF; this is flagged as a gap for `dpnp-pregabalin-safety` to source from the FDA/product label rather than duplicated here (file-ownership boundary).

**CORRECTION LOG (2026-09-03, in response to Director's challenge round):** The Recommendation-number labels for the "similar efficacy / valproic acid" and "series of medications / 12-week failure / different-class trial / combination therapy" items were originally misattributed, and the opioid/tramadol items were consequently off by one. Re-verification against the PDF's raw (non-`-layout`) reading order corrected only the Rec-# locators; no clinical substance, Level grade, or drug-class statement changed. The table was subsequently converted from verbatim text to concise paraphrases during final compliance review; Rec 1–9 numbering and grades remain source-checked.

---

## Source G3 — AAN 2011 Predecessor Guideline (Bril et al.) — operative-status reconciliation

- **Citation:** Bril V, England J, Franklin GM, Backonja M, Cohen J, Del Toro D, Feldman E, Iverson DJ, Perkins B, Russell JW, Zochodne D. "Evidence-based guideline: Treatment of painful diabetic neuropathy: report of the American Academy of Neurology, the American Association of Neuromuscular and Electrodiagnostic Medicine, and the American Academy of Physical Medicine and Rehabilitation." Multiply co-published: *Neurology* 2011 (DOI `10.1212/WNL.0b013e3182166ebe`), *PM&R* 2011 (DOI `10.1016/j.pmrj.2011.03.008`), *Muscle Nerve* 2011 (DOI `10.1002/mus.22092`).
- **PMIDs:** 21482920 (Neurology), 21497321 (PM&R), 21484835 (Muscle & Nerve) — all confirmed via `paper-search` MCP PubMed search this session.
- **Verification tier:** `ACCESS_VERIFIED` (PubMed record titles/abstracts opened directly).

**Finding that directly answers `04_OPEN-QUESTIONS.md` ("which recommendation set is currently operative"):** The PubMed record for the *Neurology* co-publication (PMID 21482920) carries the title tag **"[RETIRED]"** appended by the publisher/PubMed itself: *"Evidence-based guideline: Treatment of painful diabetic neuropathy [RETIRED]: report of the American Academy of Neurology…"* This is independent, primary-source confirmation that the 2011 guideline is formally superseded, and the 2022 Price et al. update (Source G2) is the currently operative AAN guidance. **Class: GUIDELINE / CONSENSUS (administrative/retirement status, not a clinical claim).**

⚠️ **Numeric/wording discrepancy — flagged, not silently reconciled (per CLAUDE.md hard rule):** The 2011 (retired) guideline stated **"Pregabalin is established as effective and should be offered for relief of PDN (Level A)"** — a **drug-specific** Level A rating unique to pregabalin among the anticonvulsants (gabapentin was only "probably effective," Level B, in the same 2011 document). The now-operative 2022 update (Source G2) does **not** carry forward a pregabalin-specific rating; it rates "gabapentinoids" as a pooled class at Level B alongside TCAs/SNRIs/sodium-channel blockers. **This is a materially important change for the sponsor-bias guardrail:** citing only the 2011 "pregabalin Level A" language without noting it is retired and superseded by a class-pooled Level B recommendation would misrepresent current guideline status. Both values are preserved above exactly as published; Director/auditor should treat the 2022 wording as the operative claim and the 2011 wording as historical/superseded context only.

---

## Source G4 — Toronto Consensus (Tesfaye et al. 2010)

- **Citation:** Tesfaye S, Boulton AJM, Dyck PJ, Freeman R, Horowitz M, Kempler P, Lauria G, Malik RA, Spallone V, Vinik A, Bernardi L, Valensi P, on behalf of the Toronto Diabetic Neuropathy Expert Group. "Diabetic Neuropathies: Update on Definitions, Diagnostic Criteria, Estimation of Severity, and Treatments." *Diabetes Care.* 2010;33(10):2285–2293.
- **DOI:** `10.2337/dc10-1303`
- **PMID:** 20876709 — confirmed via `paper-search` MCP PubMed search; author list matches exactly.
- **Access route:** Open-access author/publisher PDF via institutional repository (White Rose Research Online, University of Sheffield deposit), distributed under **CC BY-NC-ND**; downloaded and read directly by this session (`pdftotext` extraction of the lawfully-obtained PDF). Full PDF stored locally only at `fulltext-local/Tesfaye-2010-Toronto-Consensus.pdf` (gitignored); short excerpts below are within CC BY-NC-ND terms (attribution given, non-commercial, no alteration).
- **Verification tier:** `ACCESS_VERIFIED` (primary open-access record opened directly, not a citing-paper reference list).

**Minimal criteria for typical DPN (DSPN) — exact wording:**
1. **"Possible DSPN.** The presence of symptoms or signs of DSPN may include the following: symptoms — decreased sensation, positive neuropathic sensory symptoms (e.g., 'asleep numbness,' prickling or stabbing, burning or aching pain) predominantly in the toes, feet, or legs; or signs — symmetric decrease of distal sensation or unequivocally decreased or absent ankle reflexes."
2. **"Probable DSPN.** The presence of a combination of symptoms and signs of neuropathy include any two or more of the following: neuropathic symptoms, decreased distal sensation, or unequivocally decreased or absent ankle reflexes."
3. **"Confirmed DSPN.** The presence of an abnormality of NC and a symptom or symptoms or a sign or signs of neuropathy confirm DSPN. If NC is normal, a validated measure of small fiber neuropathy (SFN) (with class 1 evidence) may be used."
4. **"Subclinical DSPN.** The presence of no signs or symptoms of neuropathy are confirmed with abnormal NCs or a validated measure of SFN (with class 1 evidence)."
- "We recommend that definitions 1, 2, or 3 be used for clinical practice and definitions 3 or 4 be used for research studies."

**Atypical DPN — exact wording (red-flag basis):** "The atypical DPNs are different from DSPN in several important features, i.e., onset, course, manifestations, associations, and perhaps putative mechanisms…They appear to be intercurrent varieties, developing at any time during the course of a patient's diabetes…Onset of symptoms may be acute, subacute, or chronic, but the course is usually monophasic or fluctuating over time. Pain and autonomic symptoms are typical features and altered immunity has been suggested."

**Painful DPN definition — exact wording:** "pain arising as a direct consequence of abnormalities in the peripheral somatosensory system in people with diabetes," adapted from an IASP definition; diagnosis "is a clinical one, which relies on the patient's description of pain," with symptoms "distal, symmetrical, often associated with nocturnal exacerbations, and commonly described as prickling, deep aching, sharp, like an electric shock, and burning…with hyperalgesia and frequently allodynia upon examination," noting "occasionally in acute painful DPN, the symptoms may occur in the absence of signs," and that "other causes of NP must be excluded."

**Class: GUIDELINE / CONSENSUS** (formal multi-society expert-group consensus, NEURODIAB/Toronto meeting output) for all of the above.

⚠️ **Currency caveat:** This is a 2010 consensus; it is 16 years old at the time of this run. It remains the most-cited formal diagnostic-criteria consensus and is referenced approvingly inside both MEDNOTE sources and (via its case-definition lineage) the ADA chapter's neighborhood, but no formal successor consensus with the same multi-society weight was found this wave (see Source G5 for the closest 2020s alternative, which is a lower evidence tier).

---

## Source G5 — 2020s candidate for a DSPN diagnostic-consensus update (open-gap search, own initiative)

- **Citation:** Atmaca A, Ketenci A, Sahin I, Sengun IS, Oner RI, Erdem Tilki H, Adas M, Soyleli H, Demir T. "Expert opinion on screening, diagnosis and management of diabetic peripheral neuropathy: a multidisciplinary approach." *Front Endocrinol (Lausanne).* 2024;15:1380929.
- **DOI:** `10.3389/fendo.2024.1380929`
- **PMID:** 38952393 — confirmed via `paper-search` MCP PubMed search; title/DOI match exactly.
- **Access route:** PMC open access (`pmc.ncbi.nlm.nih.gov/articles/PMC11215140`), opened directly.
- **Verification tier:** `ACCESS_VERIFIED`.

**⚠️ Evidence-tier classification — read carefully before any use in synthesis:** This is **not** a formal multi-society consensus like Toronto 2010 or a systematically-graded practice guideline like the AAN documents. It is a **narrative expert-opinion document from 9 authors across 4 specialties**, stating they "critically analyzed recommendations from existing guidelines" and "agreed on a series of statements supported by scientific evidence and expert clinical opinion" — no formal Delphi process, no independent systematic evidence grading described. **Class: EXPERT INTERPRETATION, not GUIDELINE / CONSENSUS.** It explicitly builds on, but does not claim to formally supersede, Toronto Consensus.

**Proposed screening/diagnostic algorithm — exact wording:** "DPN should be considered in a patient with prediabetes or diabetes who presents with neuropathic symptoms (involve both sides symmetrically) and/or signs of neuropathy in the presence of DPN risk factors (i.e., advancing age, obesity, hypertension, dyslipidemia, poor glycemic control), with careful consideration of laboratory testing to rule out other causes of distal symmetric peripheral neuropathy and referral for a detailed neurological work-up for a confirmative test of either small or large nerve fiber dysfunction only in atypical cases."

**Atypical/red-flag list for specialist referral — exact wording:** "(1) asymmetry and rapid progression of the symptoms, (2) predominant motor weakness over sensory loss, (3) mononeuropathy or cranial nerve involvement, (4) progression of the neuropathy despite optimal glycemic control, (5) symptoms from the upper limbs, (6) family history of nondiabetic neuropathy, (7) severe painful symptoms in the feet whilst clinical examination is normal, (8) diagnosis of DPN cannot be ascertained by clinical examination with the semi-quantitative bedside tests." This is materially more granular than Toronto 2010's atypical-DPN paragraph and is useful for the moderator brief's differential-diagnosis section **provided it is labeled EXPERT INTERPRETATION, not elevated to guideline status.**

**Point-of-care/adjunct diagnostic technologies named (not yet independently verified against their own validation literature — flag as unverified device claims if used):** corneal confocal microscopy (CCM), SUDOSCAN, quantitative sensory testing (QST), NeuroQuick, NeuroPAD.

**Management-principles wording:** "the management of DPN is based [on] three principles including (1) optimal diabetes treatment via intensive glycemic control, lifestyle modification and multifactorial risk intervention, (2) pathogenetically oriented pharmacotherapy, and (3) symptomatic pain relief." Notes alpha-lipoic acid (ALA) as "an important first-line pathogenesis-directed agent" — **this is an ALA-specific claim from an EXPERT INTERPRETATION-tier source, not corroborated yet against a systematic review; do not present as guideline-grade in synthesis without further verification, and it is outside this session's drug-class scope (`dpnp-trials-comparative`/`dpnp-pregabalin-safety` territory if pursued).**

---

## Cross-source reconciliation notes for the Director

1. **Open question resolved:** `04_OPEN-QUESTIONS.md` — "Which current AAN…recommendations remain operative, and have newer updates superseded them?" → **Answered:** AAN 2011 (Bril et al.) is formally `[RETIRED]` per PubMed; AAN 2022 (Price et al.) is the current operative AAN guidance. See Source G3.
2. **Open gap addressed:** "2020s update to the DSPN diagnostic consensus distinct from Toronto Consensus" → No formal successor consensus found; closest available is Source G5, an EXPERT INTERPRETATION-tier multidisciplinary opinion, not a replacement consensus. This should be stated as a limitation in `40_SYNTHESIS/`, not glossed over.
3. **Sponsor-bias guardrail data point (Decision 2026-09-03-02):** Across all three current-generation sources that grade pharmacologic treatment (ADA 2026 Rec 12.22, AAN 2022 Rec 4, and the now-retired AAN 2011's drug-specific pregabalin Level A), **the current operative guideline language treats gabapentinoids as a class alongside TCAs/SNRIs/sodium-channel blockers, not pregabalin individually.** Any moderator-brief claim of pregabalin-specific "Grade A" status must cite the retired 2011 source explicitly as historical, not present it as current guideline standing.
4. **Not yet closed by this session:** Rec 12.19/12.20 verbatim re-verification against raw PMC/journal text (see caveat under G1); Freeman 2008 pregabalin dose-ranging RCT synthesis (handed to `dpnp-trials-comparative` per file ownership — referenced here only as it appears in ADA's reference list); Taiwan/FDA label content (belongs to `dpnp-pregabalin-safety`).

## Search log (this wave)

| Tool | Query/action | Result |
|---|---|---|
| WebFetch | `pmc.ncbi.nlm.nih.gov/articles/PMC12690177` | ADA Ch.12 content extraction |
| `paper-search` MCP `get_crossref_paper_by_doi` | `10.2337/dc26-S012` | Empty (Crossref lag) — did not block verification, PubMed + doi.org resolution sufficed |
| `paper-search` MCP `search_pubmed` | ADA 2026 Ch.12 title search | PMID 41358886 confirmed |
| WebFetch | `doi.org/10.2337/dc26-S012` | 302 redirect to journal page confirming citation |
| `paper-search` MCP `search_pubmed` | AAN 2022 guideline title search | PMID 34965987 confirmed, full author list, SMDs |
| WebFetch | `neurology.org/doi/10.1212/WNL.0000000000013038` | 403 Forbidden (paywalled) — not bypassed, per policy |
| WebFetch | `aan.com/Guidelines/home/GetGuidelineContent/1055` | AAN's own clinician-summary PDF retrieved lawfully; parsed locally with `pdftotext` (LlamaParse MCP timed out twice, local fallback used) |
| `paper-search` MCP `search_pubmed` | Bril 2011 AAN guideline search | 3 co-publication PMIDs confirmed, one explicitly `[RETIRED]` |
| WebSearch | Toronto Consensus citation lookup | PMID 20876709 / DOI 10.2337/dc10-1303 identified |
| WebFetch | White Rose eprints record + open-access PDF | Full text retrieved (CC BY-NC-ND), parsed locally with `pdftotext` |
| WebSearch | 2020s DSPN diagnostic consensus update search | Located Atmaca et al. 2024 (Frontiers) as closest candidate |
| WebFetch | `pmc.ncbi.nlm.nih.gov/articles/PMC11215140` | Full extraction of algorithm/red-flag wording |
| `paper-search` MCP `search_pubmed` | Atmaca 2024 title search | PMID 38952393 confirmed |

No Sci-Hub, paywall bypass, or authentication evasion used. One paywalled attempt (Neurology.org direct article page) returned 403 and was not retried by another route; the AAN's own open clinician-summary PDF served as the lawful substitute primary record for exact recommendation wording.
