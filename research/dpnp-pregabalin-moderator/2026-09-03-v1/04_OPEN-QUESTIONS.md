# Open Questions

- [NEEDS_SOURCE] What is the newest accessible ADA Standards of Care wording specifically addressing painful diabetic neuropathy as of 2026-09-03?
- [NEEDS_SOURCE] Which current AAN or other major society recommendations remain operative, and have newer updates superseded them?
- [NEEDS_SOURCE] What Taiwan-specific Pregabalin labeling, reimbursement, controlled-drug, or safety requirements should be included for the intended audience?
- [NEEDS_SOURCE] Can MEDNOTE-002 be fully exported or captured with its slide images and article text?
- [NEEDS_EVIDENCE] Is there robust direct evidence for choosing Pregabalin based on sleep disturbance, anxiety, renal function, age/frailty, edema/heart failure risk, or concurrent CNS depressants?
- [NEEDS_EVIDENCE] What is the best-supported clinical sequence after partial response: titrate, switch drug class, or combine therapies?
- [NEEDS_PI] Intended talk duration, audience mix, and whether QA should be phrased as panel questions, audience questions, or both.
- [NEEDS_PI] Whether Taiwan local formulary/reimbursement detail is required in the final brief.

- [NEEDS_SOURCE] PI requirement (Decision 2026-09-03-07): at least one lawful full-text PDF (guideline or regulator document) must be downloaded and LlamaParse-parsed before Final Gate. Dispatched to `dpnp-source-provenance`. Best current candidates per `10_SOURCES/FULLTEXT_LEDGER.md`: ADA Standards of Care 2026 Ch.12 (PMC OA) or FDA Pregabalin label (DailyMed).

## Wave 1 gaps (from `dpnp-source-provenance`, 2026-09-03, see `10_SOURCES/SOURCE_REGISTER.md` §D)

- [NEEDS_SOURCE] Taiwan TFDA Pregabalin/Lyrica label and safety communications — search interrupted, not yet completed. Owner for closing: `dpnp-source-provenance` and/or `dpnp-pregabalin-safety`.
- [NEEDS_SOURCE] FDA Pregabalin (Lyrica) prescribing information via DailyMed — search failed on tool timeout, not retried. Owner: `dpnp-source-provenance` and/or `dpnp-pregabalin-safety`.
- [NEEDS_SOURCE] Full/exact DOI for ADA Standards of Care in Diabetes—2026, Ch.12 — truncated in all snippets obtained so far. Owner: `dpnp-guideline-diagnosis`.
- [NEEDS_SOURCE] Direct primary-record confirmation (not press release/citing-reference-list) for: AAN 2022 update (*Neurology* 2022;98:31–43), Freeman 2008 (*Diabetes Care*), Soliman 2025 (*Lancet Neurol*), Mallick-Searle 2024 (*J Pain Res*). Owner: `dpnp-guideline-diagnosis` (AAN 2022) and `dpnp-trials-comparative` (Freeman/Soliman/Mallick-Searle).
- [NEEDS_SOURCE] Toronto Consensus (Tesfaye et al. 2010, *Diabetes Care*) primary citation — appears as a lead in 3 independent places but not yet independently opened. Owner: `dpnp-guideline-diagnosis`.
- [RESOLVED 2026-09-03 by dpnp-trials-comparative] ~~COMBO-DN and OPTION-DM trials (named in MEDNOTE-002) not yet located at their own primary publications.~~ Both located and `ACCESS_VERIFIED` at primary record: COMBO-DN (Tesfaye et al., *Pain* 2013;154:2616-25, PMID 23732189); OPTION-DM (Tesfaye et al., *Lancet* 2022;400:680-90, PMID 36007534, + HTA companion PMID 36259684 + protocol PMID 30348206). See `20_EVIDENCE/trials-comparative/01_EVIDENCE-TABLE.md` T5/T6.
- [NEEDS_EVIDENCE] MEDNOTE-002 numeric claims (incidence/prevalence/NNT/NNH/discontinuation figures) have no primary citation yet and were flagged by `dpnp-source-provenance` as a sponsor-bias risk point — do not carry these numbers into synthesis until independently sourced to a primary study, and preserve the exact original tokens if/when sourced.
- [NEEDS_SOURCE] No systematic search yet run for a current (2020s) DSPN/small-fiber-neuropathy diagnostic consensus statement distinct from the 2010 Toronto Consensus. Owner: `dpnp-guideline-diagnosis`.

## Wave 2 gaps (from `dpnp-trials-comparative`, 2026-09-03, see `20_EVIDENCE/trials-comparative/01_EVIDENCE-TABLE.md`)

- [NEEDS_FULLTEXT] Funding/COI statements and individual-trial risk-of-bias detail for T1 (Freeman 2008), T2 (Frontiers 2026 combo SR — esp. the QI 2022 included trial), and T3's DPN-relevant subset (Soliman/NeuPSIG 2025).
- [NEEDS_FULLTEXT] OPTION-DM site-count discrepancy: Lancet main paper reports 13 centres, HTA companion monograph reports 21 secondary-care centres — not yet reconciled, flagged not silently resolved.
- [NEEDS_SOURCE] No post-2025 network meta-analysis directly comparing pregabalin, gabapentin, duloxetine, amitriptyline, and sodium-channel blockers head-to-head across DPN-specific trials identified yet; Soliman/NeuPSIG 2025 (T3) is the closest available synthesis but pools pregabalin+gabapentin as "α2δ-ligands" and is mixed-etiology, not DPN-specific.

### Key counter-bias findings to carry into synthesis (sponsor-bias guardrail — do not omit)

- Soliman/NeuPSIG 2025: α2δ-ligands (gabapentin+pregabalin pooled) NNT 8.9 (95% CI 7.4–11.10) is numerically worse than TCAs (NNT 4.6) and SNRIs (NNT 7.4), despite equal "strong, first-line" guideline grading across all three classes. This is class-pooled/mixed-etiology (`INDIRECT EVIDENCE` for pregabalin/DPN specifically), not a pregabalin-only or DPN-only estimate.
- COMBO-DN (T5): combination (duloxetine+pregabalin) was **not** significantly superior to high-dose monotherapy for the primary outcome (P=0.370); an uncorrected exploratory analysis favored duloxetine 60mg over pregabalin 300mg (P<0.001) — must not be overstated as a proven duloxetine-superiority finding, but also must not be omitted as a counter-balance to pregabalin-favorable framing.
- OPTION-DM (T6): all three pathways (amitriptyline-based, pregabalin-based, duloxetine-based) showed similar efficacy at week 16 (no pathway comparison reached significance) — no pregabalin-pathway superiority over amitriptyline- or duloxetine-based regimens.
- Combination therapy evidence (T2, T5, T6) is consistently modest/uncertain (GRADE low-certainty and/or non-significant primary outcomes), not proven synergy.
