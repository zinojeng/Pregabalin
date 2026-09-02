# Research Charter

PROJECT_ID: `dpnp-pregabalin-moderator`

RUN_ID: `2026-09-03-v1`

## Primary purpose

為一場由 Pregabalin 藥品贊助、主題為「Diabetic Peripheral Neuropathic Pain（DPNP）的診斷與治療 guideline」的主持／moderation 工作，建立截至 2026-09-03 的可追溯 evidence briefing，並產出繁體中文的詳細重點整理與 10 組有見解、能引發講者深入討論的 QA。

## Primary questions

1. 在 diabetes 患者出現 distal pain、burning、allodynia 或 numbness 時，如何先確認 neuropathic pain phenotype、建立 DPN/DSPN 的臨床診斷，並辨識 atypical features、可逆原因與需轉介／檢查的 red flags？
2. 最新 guideline 如何定義以 patient-centered goals 選擇 DPNP 治療，並如何定位 Pregabalin 與其他有效 drug classes？
3. Pregabalin 的 efficacy、dose/titration、time-to-assess、renal adjustment、common/serious harms、withdrawal、misuse/dependence 與重要 interaction，哪些由直接 evidence 支持？
4. RCT、network meta-analysis、head-to-head 或 real-world evidence 是否支持特定族群優先選 Pregabalin？哪些只是合理但未證實的 extrapolation？
5. 在 sponsor context 下，主持人應如何精準呈現 benefit、uncertainty、alternatives 與 shared decision-making，而不成為 product promotion？

## PICO/decision frame

- Population: adults with painful diabetic peripheral neuropathy / painful DSPN; note where studies include mixed neuropathic pain etiologies.
- Intervention: Pregabalin, including clinically used dosing/titration and renal adjustment.
- Comparators: placebo; Duloxetine/SNRI; Gabapentin/gabapentinoids; Amitriptyline/other TCA; sodium-channel blockers where guideline-supported; topical treatments; combination or sequential strategies; non-pharmacologic/multidisciplinary care.
- Outcomes: pain reduction (including ≥30%/≥50% responder outcomes), sleep interference, function, quality of life, patient global impression, adverse events, discontinuation, falls/cognitive effects, edema/weight, misuse/dependence, and feasibility.
- Time horizon: current evidence/guidelines available through 2026-09-03, with older landmark evidence retained when still decision-relevant.

## Required deliverables

1. `40_SYNTHESIS/DPNP_Pregabalin_Moderator_Brief_zh-TW.md`
   - executive summary
   - diagnosis and differential pathway
   - current guideline comparison
   - treatment algorithm and patient-selection logic
   - Pregabalin efficacy/safety/implementation
   - controversies, evidence gaps, sponsor-bias guardrail
   - claim-level citations and evidence labels
2. `40_SYNTHESIS/DPNP_10_Insightful_QA_zh-TW.md`
   - exactly 10 moderator questions
   - each with why it matters, model answer, evidence/uncertainty, and suggested follow-up probe
3. Search strategy, source inventory, evidence tables, full-text/parse ledger, and final independent QA report.

## Source of truth

Authoritative guideline documents, regulators, peer-reviewed primary studies/systematic reviews, registered trials, and traceable evidence tables in this repository. The two MedNote lecture pages are context/reference inputs, not final authorities.

## Success conditions

- Recency claim is supported by recorded search dates and explicit coverage.
- Every substantive recommendation is cited and classified by evidence type.
- Pregabalin is discussed with balanced alternatives and sponsor disclosure.
- Ten QA are clinically discriminating rather than factual trivia or promotional prompts.
- Independent auditor returns `PASS` or `PASS_WITH_MINOR_ISSUES`.
- No secrets or non-redistributable full text are committed.

## Stop/block conditions

- Missing primary source for a key claim → `BLOCKED_FOR_SOURCE`.
- Conflicting guideline wording or trial numeric values → `SOURCE_CONFLICT`; preserve both until resolved.
- Sponsor preference would require an unsupported claim → `BLOCKED_FOR_PI` rather than guessing or embellishing.
