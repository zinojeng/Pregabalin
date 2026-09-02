# Taiwan 利瑞卡膠囊 (Lyrica hard Capsule, pregabalin) 仿單 — Verified Extraction

Owner: `dpnp-pregabalin-safety`. Verification status: `ACCESS_VERIFIED` — this session opened and read the PDF directly, page by page (image/OCR render), on 2026-09-03.

## Source identity and a provenance caveat

- Document title: 利瑞卡膠囊75毫克 / Lyrica hard Capsule 75mg（同一仿單另列150mg、300mg規格）
- Drug license: **衛署藥輸字第024995號**（須由醫師處方使用）
- **版本日期 (version date): 2024-11-30**（民國113年11月30日, printed as "113.11.30" watermark on every page with a 衛生福利部食品藥物管理署 騎縫章 perforation stamp）
- Hosting URL actually fetched: https://ksph.kcg.gov.tw/7/dfiles_pdf/Lyrica.pdf (高雄市立岡山醫院/高雄市政府衛生局 mirror of the manufacturer-submitted, TFDA-stamped package insert)
- Access date: 2026-09-03
- **Provenance gap, logged per CLAUDE.md discrepancy-flagging rule:** this session attempted to reach TFDA's own 藥品許可證查詢 system directly (https://www.fda.gov.tw/tc/siteContent.aspx?sid=1740) to cross-check license 衛署藥輸字第024995號 at the primary regulator's own database, and that page returned "目前並無相關資料" (no data at that endpoint/section). The document actually used carries the TFDA 騎縫章 stamp and license number and is treated as `ACCESS_VERIFIED` on that basis, but it is a hospital-hosted mirror, not a direct TFDA.gov.tw page. `dpnp-source-provenance` or a later session should still attempt the correct TFDA 藥證查詢 URL/search path if an independent primary-regulator confirmation is required for the final synthesis.
- **Taiwan controlled-drug (管制藥品) schedule status: NOT CONFIRMED.** This package insert does not state a 管制藥品分級 anywhere in the text captured. A Taipei Veterans General Hospital patient-education leaflet for pregabalin (https://wd.vghtpe.gov.tw/anes/files/衛教資訊/疼痛控制科止痛藥物說明書-pregabalin.pdf) likewise does not state a controlled-drug schedule. A web search for the official 衛生福利部食品藥物管理署 管制藥品品項一覽表 entry for pregabalin did not resolve to a directly citable primary listing in this session. **Do not state or imply a Taiwan controlled-drug schedule for pregabalin in `40_SYNTHESIS/` until a primary TFDA 管制藥品 list/公告 is opened directly.** [NEEDS_SOURCE — flagging for `04_OPEN-QUESTIONS.md` via the Director.]
- **HLA-B\*1502 note — flagged as likely institutional-template artifact, not a pregabalin-specific requirement.** The VGHTPE patient leaflet above states: "有抗癲癇藥物過敏病史，請務必告訴醫護人員，我們將進行 HLA-B\*1502 基因檢測，以確保用藥安全" ("if you have a history of antiepileptic drug allergy, please inform staff — we will perform HLA-B\*1502 genetic testing to ensure medication safety"). HLA-B\*1502 is an established pharmacogenomic risk marker for **carbamazepine/oxcarbazepine**-induced Stevens-Johnson syndrome/toxic epidermal necrolysis in Han Chinese populations, not a marker with an established mechanistic or regulatory link to pregabalin specifically. This sentence appears in a pregabalin-labeled document, most likely because the hospital's AED patient-leaflet template is shared across antiepileptic drugs. Preserved verbatim here per the "flag discrepancies, never silently repair" rule; **do not present this as a pregabalin-specific genetic-testing requirement in synthesis** without independent confirmation.

## 適應症 Indications (仿單 §2, p.1)

> "帶狀疱疹後神經痛　成人局部癲癇的輔助治療　纖維肌痛 (fibromyalgia)　糖尿病周邊神經病變所引起的神經性疼痛　脊髓損傷所引起的神經性疼痛"

(Postherpetic neuralgia; adjunctive therapy for adult partial-onset epilepsy; fibromyalgia; neuropathic pain due to diabetic peripheral neuropathy; neuropathic pain due to spinal cord injury.) Same five indications as the current FDA label (`LABELING_FDA.md` §1) — concordant.

## 用法用量 Dosage and administration (仿單 §3, pp.1–3)

General instructions (§3.1): oral, with or without food; taper over a minimum of 1 week when stopping ("停止服用LYRICA時，應以至少一週的時間逐漸減量"); dose adjustment required in renal impairment.

**§3.1.1 糖尿病周邊神經病變引起之神經性疼痛 (DPN):**
> "對於肌酸酐清除率60 mL/min 以上的病人，LYRICA的最高建議劑量是150 mg每兩次或100 mg 每天三次 (300 mg/天)。應從75 mg 每天兩次或50 mg 每天三次 (150 mg/天) 開始給藥，根據療效和耐受性可在一週之內將劑量增加到 300 mg/天。LYRICA雖然也在600 mg/天的劑量下做過研究，但沒有證據顯示這個劑量能提供額外的顯著效益，病人對這個劑量的耐受度也較差。由於劑量相關的不良反應，故不建議用超過300 mg/天的劑量治療。"

Numerically identical to the FDA label's Section 2.2 (150→300 mg/day titration within 1 week, 300 mg/day ceiling for CLcr ≥60 mL/min, 600 mg/day studied but not recommended). Note a minor wording artifact in the Chinese text ("150 mg每兩次" appears to mean 150 mg twice-daily-equivalent phrasing/OCR of "75mg BID"; preserved verbatim as printed — flagged rather than silently corrected).

Other indications' dosing (§3.1.2–3.1.5: PHN 150–300 mg/day, up to 600 mg/day in non-responders; epilepsy adjunct 150–600 mg/day; fibromyalgia 300–450 mg/day, up to 600 mg studied but not recommended above 450; spinal cord injury 150–600 mg/day) captured in full in the source PDF for completeness but out of this role's core DPN-safety focus.

## 腎功能不全成人劑量 Renal impairment dosing (仿單 §3.1.6, Table 1, p.3)

Cockcroft-Gault formula given verbatim (identical to FDA label). **表1 根據腎功能調整Pregabalin劑量:**

| 肌酸酐清除率 CLcr (mL/min) | Pregabalin 每日總劑量 (mg/天) | 用法 |
|---|---|---|
| 大於或等於60 | 150 / 300 / 450 / 600 | BID或TID |
| 30–60 | 75 / 150 / 225 / 300 | BID 或 TID |
| 15–30 | 25–50 / 75 / 100–150 / 150 | QD 或 BID |
| 小於15 | 25 / 25–50 / 50–75 / 75 | QD |

Hemodialysis supplemental dose (single extra dose after each 4-hour session): 25 mg QD → 25 or 50 mg; 25–50 mg QD → 50 or 75 mg; 50–75 mg QD → 75 or 100 mg; 75 mg QD → 100 or 150 mg.

**Cross-source concordance:** this table is numerically identical, mg-for-mg, to FDA label Table 2 (`LABELING_FDA.md`). No discrepancy found; not independently re-derived from a third source.

## 禁忌 Contraindications (仿單 §4, p.4)

> "LYRICA禁用於已知對pregabalin或本品其他任何成分過敏的病人。曾有使用pregabalin的病人發生血管性水腫與過敏的現象。"

## 警語及注意事項 Warnings and Precautions (仿單 §5, pp.4–8)

- **§5.1.1 血管性水腫 (Angioedema):** face/mouth/tongue/lips/gums/neck(throat/larynx) swelling reported; life-threatening angioedema with respiratory compromise requiring emergency care; discontinue immediately; caution with prior angioedema history or concurrent ACE-inhibitor use.
- **§5.1.2 過敏 (Hypersensitivity):** skin redness, blisters, hives, rash, dyspnea, wheezing; discontinue immediately.
- **§5.1.3 自殺行為與自殺意圖 (Suicidal behavior/ideation):** pooled analysis of 199 placebo-controlled trials across 11 AEDs — RR 1.8 (95% CI 1.2–2.7); incidence 0.43% (27,863 AED-treated) vs 0.24% (16,029 placebo); ≈1 additional case per 530 treated; 4 suicides in drug-treated arms, 0 in placebo arms in these trials (numbers too small for conclusions). **表2** reproduces the same by-indication risk table as FDA label Table 3 (Epilepsy/Psychiatric/Other/Total, per-1000-patient event rates, RR, risk difference) — numerically identical.
- **§5.1.4 呼吸抑制 (Respiratory depression):** "從病例報告、人體試驗和動物研究所得證據顯示，LYRICA與中樞神經系統 (CNS) 抑制劑（包括鴉片類藥物）同時給藥，或有潛在呼吸障礙的背景情況下，會導致嚴重、危及生命或致死性的呼吸抑制。當決定LYRICA與另一種CNS抑制劑（尤其是鴉片類藥物）同時開立處方時，或對有潛在呼吸障礙的病人開立LYRICA處方時，應監測病人的呼吸抑制和鎮靜症狀，並考慮以低劑量LYRICA開始。" Matches FDA Section 5.5 essentially verbatim in translation. Not a boxed warning in this insert either.
- **§5.1.5 頭暈和嗜睡 (Dizziness/somnolence):** dizziness 30% LYRICA vs 8% placebo; somnolence 23% vs 8%; led to withdrawal in 4% each; among those affected, dizziness persisted to last dose in 30%, somnolence in 42%. Matches FDA Section 5.6 exactly.
- **§5.1.6 突然或快速停藥導致不良反應風險增加 (Withdrawal):** taper over a minimum of 1 week; reported abrupt-discontinuation symptoms: insomnia, nausea, headache, anxiety, hyperhidrosis, diarrhea.
- **§5.1.7 周邊水腫 (Peripheral edema):** incidence 6% LYRICA vs 2% placebo; 0.5% vs 0.2% withdrew. Thiazolidinedione co-use data: peripheral edema 3% (2/60) thiazolidinedione-only vs 8% (69/859) LYRICA-only vs 19% (23/120) both; weight gain 0% (0/60) vs 4% (35/859) vs 7.5% (9/120) respectively. **Heart failure caution:** "因為關於心臟功能屬於紐約心臟學會 (NYHA) 分類第三級或第四級的充血性心衰竭病人資料有限，因此LYRICA應慎用於這些病人。" — matches FDA Section 5.7 NYHA III/IV caution.
- **§5.1.8 體重增加 (Weight gain):** ≥7% baseline weight gain in 9% LYRICA vs 2% placebo (≤14-week trials); diabetic patients: mean +1.6 kg (range −16 to 16 kg) LYRICA vs +0.3 kg (range −10 to 9 kg) placebo; 333 diabetic patients treated ≥2 years averaged +5.2 kg; "並未造成血糖失去控制 (由測量HbA1C得知)" (did not cause loss of glycemic control by HbA1c) in open-label longer-term trials — numerically identical to FDA label.
- **§5.1.9 致腫瘤可能性 (Tumorigenic potential):** hemangiosarcoma in two mouse strains in lifetime studies; 57 new/worsening-tumor reports among ~6396 patient-years (>12 years old); clinical significance/background-rate comparison unavailable.
- **§5.1.10 對眼睛的影響 (Ophthalmological):** blurred vision 7% vs 2%; prospective testing (>3600 patients): visual acuity reduced 7% vs 5%, visual field changes 13% vs 12%, funduscopic changes 2% vs 2%.
- **§5.1.11 肌酸激酶升高 (CK elevation):** mean 60 U/L (LYRICA) vs 28 U/L (placebo); 1.5% vs 0.7% ≥3× ULN; 3 rhabdomyolysis reports premarketing. **Locally added data not present in the FDA label:** "日本A0081208研究：在日本A0081208研究中，觀察到肌酸激酶(creatine kinase)升高的現象，升高的比例為pregabalin組4.0% (n=250) vs 安慰劑組0.4% (n=248)" — a Japan-specific post-marketing/regional study cited only in the Taiwan insert; treat as a Taiwan/Japan-label-specific addition, not yet independently verified against the primary Japanese study report.
- **§5.1.12 血小板計數減少 (Decreased platelets):** mean maximal decrease 20×10³/µL (LYRICA) vs 11×10³/µL (placebo); 3% vs 2% clinically significant decrease; 1 severe thrombocytopenia case; no increased bleeding-related adverse reactions.
- **§5.1.13 PR間期延長 (PR prolongation):** mean +3–6 msec at ≥300 mg/day; no increased risk of ≥25% PR increase, PR >200 msec, or 2nd/3rd-degree AV block identified (limited subgroup analysis).
- **§5.2 藥物濫用及依賴性 (Abuse and dependence):** not known to act at receptor sites associated with drugs of abuse; recreational-user study (N=15): 450 mg single dose rated similarly to diazepam 30 mg on "好」感/「快感(high)」/「喜好(liking)」; euphoria reported by 4% LYRICA-treated vs 1% placebo-treated (>5500 patients), ranging 1–12% in some populations; dependence — abrupt/rapid discontinuation symptoms (insomnia, nausea, headache/diarrhea) plus postmarketing reports of seizures, anxiety, hyperhidrosis (physiological dependence pattern).

## 特殊族群注意事項 Special populations (仿單 §6, pp.9–10)

- **§6.1 懷孕 (Pregnancy):** overall major-birth-defect rate possibly slightly increased, no specific pattern identified; miscarriage/other outcomes not clearly attributable. Animal data: fetal structural abnormalities at AUC ≥16× human MRD exposure (rat/rabbit organogenesis studies); pre/postnatal rat study — lethality, growth retardation, neuro/reproductive impairment in offspring; gestation prolongation/dystocia at ≥50× human MRD AUC exposure.
- **§6.2 哺乳 (Lactation):** pregabalin detected in breast milk at ~76% of maternal plasma concentration; estimated infant dose 0.31 mg/kg/day (~7% of maternal weight-adjusted dose, 10-subject PK study, 150 mg q12h ×4 doses); milk-production and breastfed-infant effects not evaluated; "由於有導致腫瘤生成的潛在風險，因此不建議於LYRICA治療期間哺餵母乳" (breastfeeding not recommended, due to tumorigenicity risk) — matches FDA 8.2.
- **§6.3 有生育能力的女性與男性 (Reproductive potential) — 男性精子生成:** RCT (≤600 mg/day, n=111 vs placebo n=109, 13 weeks + 13-week washout): ~9% (6/65) pregabalin PP-population vs 3% (2/62) placebo had ≥50% sperm-concentration reduction at Week 26; within pre-specified 20% non-inferiority margin; reversible in most by 3 months off-drug (one subject still reduced at 9 and 12 months — clinical relevance unknown).
- **§6.4 小兒 (Pediatric):** safety/effectiveness not established generally; fibromyalgia RCT (107 patients, age 12–17, 15 weeks, 75–450 mg/day): numerically greater pain-score improvement vs placebo, not statistically significant; adverse reactions similar profile to adults (dizziness, nausea, headache, weight gain, fatigue most common).
- **§6.5 老年人 (Geriatric):** DPN trials 246 (65–74y) + 73 (≥75y); PHN trials 282 (65–74y) + 379 (≥75y); epilepsy trials only 10 (65–74y) + 2 (≥75y); "並未觀察到安全性與療效的總體差異" between older and younger patients (pooled statement). Fibromyalgia ≥65y (106 patients): more frequent neurological adverse reactions — dizziness, blurred vision, balance disorder, tremor, confusion, coordination abnormality, somnolence. Renal clearance decline with age → dose adjustment per §3.1.
- **§6.6–6.7 腎功能不全 (Renal impairment):** dose adjustment required per §3.1/Table 1; not studied in pediatric renal impairment.

## 交互作用 Drug interactions (仿單 §7, p.11)

Negligible metabolism (<2% recovered as metabolites in urine), no plasma protein binding → low pharmacokinetic interaction potential; no PK interaction demonstrated with carbamazepine, valproic acid, lamotrigine, phenytoin, phenobarbital, topiramate. Pharmacodynamic: co-administration with oxycodone, lorazepam, or ethanol showed no PK interaction but additive cognitive/motor impairment; "對呼吸沒有臨床上重要的影響" (no clinically important respiratory effect) — same PK/PD study as FDA label; same caution applies not to over-read this as contradicting the general respiratory-depression warning (§5.1.4), which rests on broader case-report/postmarketing evidence.

## 副作用/不良反應 Adverse reactions — DPN-specific table (仿単 §8, Table 3, pp.12–13)

**表3 在糖尿病周邊神經病變引起神經性疼痛的對照性試驗中不良反應的發生率** (75/150/300/600 mg/天 + 所有PGB[N=979] + 安慰劑[N=459]):
- 導致停藥: 9% LYRICA vs 4% 安慰劑; 最常導致停藥者為頭暈(3%)與嗜睡(2%)。
- Selected 所有PGB% vs 安慰劑%: 頭暈 21 vs 5；嗜睡 12 vs 3；周邊水腫 9 vs 2；體重增加 4 vs 0；水腫 2 vs 0；運動失調 3 vs 1；視力模糊 4 vs 2；口乾 5 vs 1；精神紊亂 2 vs 1；低血糖症 2 vs 1 — numerically identical to FDA Table 4.

Bridging PHN-trial narrative (same page range, not DPN-specific — flagged to avoid misattribution as in the FDA-label file): 12.4% pregabalin-treated vs 9.0% placebo-treated had ≥1 severe adverse reaction; 8% vs 4.3% had ≥1 severe treatment-related adverse reaction.
