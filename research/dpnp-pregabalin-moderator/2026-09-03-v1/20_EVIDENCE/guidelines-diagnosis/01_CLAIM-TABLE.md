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

| # | Exact wording (verbatim) | Grade | Evidence class | Locator |
|---|---|---|---|---|
| Rec 12.17 | "All people with diabetes should be assessed for diabetic peripheral neuropathy starting at diagnosis of type 2 diabetes and 5 years after the diagnosis of type 1 diabetes and at least annually thereafter." | B | GUIDELINE / CONSENSUS | Ch.12, Neuropathy screening subsection |
| Rec 12.18 | "Assessment for distal symmetric polyneuropathy should include a careful history and assessment of either temperature or pinprick sensation (small-fiber function) and vibration sensation using a 128-Hz tuning fork (large-fiber function). All people with diabetes should have annual 10-g monofilament testing to identify feet at risk for ulceration and amputation." | B | GUIDELINE / CONSENSUS | ibid. |
| Rec 12.19 | "Symptoms and signs of autonomic neuropathy should be assessed in people with diabetes starting at diagnosis of type 2 diabetes and 5 years after the diagnosis of type 1 diabetes, and at least annually thereafter, and with evidence of other microvascular complications, particularly kidney disease and diabetic peripheral neuropathy…" | E | GUIDELINE / CONSENSUS | ibid. — sentence truncated in extraction; **flag for re-verification of full sentence before final synthesis quotation** |
| Rec 12.20 | "Optimize glucose management to prevent or delay the development of neuropathy in people with type 1 diabetes [A] and to slow the progression of neuropathy in people with type 2 diabetes [C]…[B]" | A / C / B (multi-part) | GUIDELINE / CONSENSUS | ibid. — **multi-graded recommendation; exact clause-to-grade mapping needs re-check against the journal PDF before verbatim quotation in `40_SYNTHESIS/`, current extraction is PMC-page-derived, not page-image-verified** |
| Rec 12.21 | "Assess and treat pain related to diabetic peripheral neuropathy [B] and symptoms of autonomic neuropathy to improve quality of life. [E]" | B (pain) / E (autonomic sx) | GUIDELINE / CONSENSUS | ibid. — directly supports Charter's "treatment goals = pain/sleep/function/QoL, not nerve reversal" framing |
| Rec 12.22 | "Gabapentinoids, serotonin-norepinephrine reuptake inhibitors, tricyclic antidepressants, and sodium channel blockers are recommended as initial pharmacologic treatments for neuropathic pain in diabetes. [A]… Opioids, including tramadol and tapentadol, should not be used for neuropathic pain treatment in diabetes given the potential for adverse events except in rare circumstances. [B]" | A (drug classes, pooled) / B (against opioids) | GUIDELINE / CONSENSUS | ibid. |

**Explicit no-reversal statement (Charter-relevant):** "Specific treatment to reverse the underlying nerve damage in diabetes is currently not available" — direct textual support for the Charter's non-negotiable rule against implying analgesic therapy reverses nerve damage. **Class: GUIDELINE / CONSENSUS.**

**Differential/red-flag statement:** "In all people with diabetes and DPN, causes of neuropathy other than diabetes should be considered, including toxins (e.g., alcohol), neurotoxic medications (e.g., chemotherapy), vitamin B12 [deficiency], hypothyroidism, kidney disease, malignancies…infections (e.g., HIV, hepatitis C)…" and referral is warranted for "acute or subacute presentation, non–length dependent, asymmetric, and/or motor involvement." **Class: GUIDELINE / CONSENSUS.**

⚠️ **Sponsor-bias-relevant finding:** Rec 12.22 recommends gabapentinoids, SNRIs, TCAs, and sodium-channel blockers as a **pooled class-level Grade A** option — it does **not** single out pregabalin (or any one drug) as preferred. This must not be paraphrased into a pregabalin-specific "Grade A" claim in synthesis.

⚠️ **Caveat on this table's own reliability:** Rec 12.19/12.20 wording above was extracted via an automated fetch-and-summarize tool (WebFetch) reading the PMC page, not by this session reading raw PMC HTML/PDF text directly. The DOI and Rec 12.17/12.18/12.21/12.22 core sentences read consistently across two independent tool calls and match the source register's independently-obtained snippets, so confidence is HIGH for those. Rec 12.19 and the exact grade-to-clause mapping in 12.20 are **lower confidence** pending a raw-text re-pull (PMC HTML or journal PDF) before verbatim use in `40_SYNTHESIS/`. Logged here rather than silently smoothed over, per CLAUDE.md's "never silently repair" rule.

---

## Source G2 — AAN 2022 Practice Guideline Update: Oral and Topical Treatment of Painful Diabetic Polyneuropathy

- **Citation:** Price R, Smith D, Franklin G, Gronseth G, Pignone M, David WS, Armon C, Perkins BA, Bril V, Rae-Grant A, Halperin J, Licking N, O'Brien MD, Wessels SR, MacGregor LC, Fink K, Harkless LB, Colbert L, Callaghan BC. "Oral and Topical Treatment of Painful Diabetic Polyneuropathy: Practice Guideline Update Summary: Report of the AAN Guideline Subcommittee." *Neurology.* 2022;98:31–43.
- **DOI:** `10.1212/WNL.0000000000013038`
- **PMID:** 34965987 — confirmed via `paper-search` MCP PubMed search; full author list matches source register lead exactly (previously only "Price/Franklin/Gronseth et al." was corroborated — now complete).
- **Access route:** (a) PubMed abstract (effect sizes, top-line Level B statements) — `ACCESS_VERIFIED`; (b) AAN's own lawfully-hosted clinician summary PDF (`aan.com/Guidelines/home/GetGuidelineContent/1055`), fetched directly, converted locally with `pdftotext`, all 9 numbered recommendations with exact Level grades captured verbatim. **Full PDF stored locally only** at `20_EVIDENCE/guidelines-diagnosis/fulltext-local/AAN-2022-painful-DPN-guideline-summary.pdf` (gitignored) per AAN's "single copy for personal use" redistribution restriction — only short excerpts below are committed, consistent with fair use and CLAUDE.md's full-text policy.
- **Verification tier:** `ACCESS_VERIFIED` (primary record + own-society-published clinician summary, not a press release).

| Rec # | Exact wording (verbatim) | Level |
|---|---|---|
| 1 | "Clinicians should assess patients with diabetes for peripheral neuropathic pain and its effect on these patients' function and quality of life." | B |
| 2 | "When initiating pharmacologic intervention for painful diabetic neuropathy, clinicians should counsel patients that the goal of therapy is to reduce, and not necessarily to eliminate, pain." | B |
| 3 | "Clinicians should assess patients with painful diabetic neuropathy for the presence of concurrent mood and sleep disorders and treat them as appropriate." | B |
| 4 | "In patients with painful diabetic neuropathy, clinicians should offer TCAs, SNRIs, gabapentinoids, and/or sodium channel blockers to reduce pain." | B |
| 4 (cont.) | "Given similar efficacy, clinicians should consider factors other than efficacy, including potential adverse effects, patient comorbidities, cost, and patient preferences, when recommending treatment for painful diabetic neuropathy." | B |
| 4 (cont.) | "In patients of child-bearing potential with painful diabetic neuropathy, clinicians should not offer valproic acid." / "In all patients with painful diabetic neuropathy, clinicians should not prescribe valproic acid given the potential for serious adverse events unless multiple other effective medications have failed." | B |
| 5 | "Clinicians may assess patient preferences for effective oral, topical, nontraditional, and nonpharmacologic interventions for painful diabetic neuropathy." / "…providers may offer topicals (capsaicin, glyceryl trinitrate spray, *Citrullus colocynthis*), nontraditional (ginkgo biloba), and/or nonpharmacologic interventions (CBT, exercise, Tai Chi, mindfulness)." | C |
| 6 | "Clinicians should counsel patients that a series of medications may need to be tried to identify the treatment that most benefits patients with painful diabetic neuropathy." | B |
| 6 (cont.) | "Clinicians should determine that an individual intervention to reduce neuropathic pain is a failure either when the medication has been titrated to a demonstrated efficacious dose for approximately 12 weeks without clinically significant pain reduction or when side effects from the medication outweigh any benefit…" | B |
| 6 (cont.) | "Clinicians should offer patients a trial of a medication from a different effective class when they do not achieve meaningful improvement or if they experience significant adverse effects with the initial therapeutic class." | B |
| 6 (cont.) | "For patients who achieve partial improvement with an initial therapeutic class, clinicians should offer a trial of a medication from a different effective class or combination therapy by adding a medication from a different effective class." | B |
| 7 (opioids) | "Clinicians should not use opioids for the treatment of painful diabetic neuropathy." | B |
| 7 (cont.) | "If patients are currently on opioids for the treatment of painful diabetic neuropathy, clinicians may offer the option of a safe taper off these medications and discuss alternative nonopioid treatment strategies." | C |
| 8 (tramadol/tapentadol) | "Clinicians should not use tramadol and tapentadol (opioids/SNRI dual mechanism agents) for the treatment of painful diabetic neuropathy." | C |
| 8 (cont.) | "If patients are currently on tramadol and tapentadol…clinicians may offer the option of a safe taper off these medications and discuss alternative nonopioid treatment strategies." | C |

**Effect-size data (from PubMed abstract, PMID 34965987, class-pooled, not drug-specific):**
"Gabapentinoids (SMD 0.44; 95% CI, 0.21–0.67), serotonin-norepinephrine reuptake inhibitors (SNRIs) (SMD 0.47; 95% CI, 0.34–0.60), sodium channel blockers (SMD 0.56; 95% CI, 0.25–0.87), and SNRI/opioid dual mechanism agents (SMD 0.62; 95% CI, 0.38–0.86) all have comparable effect sizes just above or just below our cutoff for a medium effect size (SMD 0.5). Tricyclic antidepressants (TCAs) (SMD 0.95; 95% CI, 0.15–1.8) have a large effect size, but this result is tempered by a low confidence in the estimate." **Class: DIRECT EVIDENCE** (meta-analytic synthesis underlying the guideline), reported at the **drug-class** level, not specific to pregabalin within the gabapentinoid class.

⚠️ **Sponsor-bias-relevant finding:** This is the current operative AAN recommendation, and it treats TCAs/SNRIs/gabapentinoids/sodium-channel blockers as an undifferentiated first-line tier (Level B, "offer…and/or"), explicitly stating comparable effect sizes make "recommendations for one [class] over another difficult." No pregabalin-specific superiority claim is supported by this source.

**Renal/edema/comorbidity content in this summary:** gabapentinoid-specific dose/renal-adjustment tables were **not** included in this clinician-summary PDF; this is flagged as a gap for `dpnp-pregabalin-safety` to source from the FDA/product label rather than duplicated here (file-ownership boundary).

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
