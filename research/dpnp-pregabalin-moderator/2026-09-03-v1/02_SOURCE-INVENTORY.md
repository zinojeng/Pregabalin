# Source Inventory

Last updated: 2026-09-03 (Asia/Taipei)

| Source ID | Source | Type | Status | Role / notes |
|---|---|---|---|---|
| RUNBOOK-001 | `Claude_Code_Cross-Session_Research_完整建議與經驗_Runbook.md` | local SOP | VERIFIED_IDENTITY | Cross-session research governance |
| MEDNOTE-001 | [糖尿病神經病變 臨床表現與診斷評估](https://mednote.zeabur.app/lectures/77f3524a-73dc-4ce9-993c-d0cd33d17686) | derivative lecture summary/slides, dated 2026-03-23 | ACCESS_VERIFIED; CLAIMS_UNVERIFIED | diagnostic context; speaker Chi-Chao Chao; not a primary guideline |
| MEDNOTE-002 | [糖尿病神經病變管理：藥物與非藥物治療策略](https://mednote.zeabur.app/lectures/5b2e209e-e069-459f-835a-52a5974c3fcb) | derivative lecture summary/slides, dated 2026-03-23 | ACCESS_VERIFIED; CLAIMS_UNVERIFIED | treatment context; speaker Wang Yan-Feng, Taipei VGH Neurology/NYCU; direct WebFetch succeeded, fallback acquisition not needed; full capture in `10_SOURCES/MEDNOTE_CAPTURE.md` |
| ARCH-001 | [zinojeng/academic-research-agents](https://github.com/zinojeng/academic-research-agents) | architecture/code reference | INSPECTED | Literature/PDF implementations include placeholders; do not use as evidence engine without validation |
| REPO-001 | [zinojeng/Pregabalin](https://github.com/zinojeng/Pregabalin) | public output repository | VERIFIED_EMPTY_AT_START | this run's durable knowledge plane |

## Authoritative sources to acquire and verify

The following are source classes/search targets, not yet accepted citations:

- Current ADA Standards of Care section(s) relevant to diabetic neuropathy and neuropathic pain.
- Current neurology/pain society guideline on treatment of painful diabetic polyneuropathy.
- Current national/regulatory Pregabalin label and safety communications relevant to Taiwan and/or major regulators.
- Recent systematic reviews/network meta-analyses and pivotal or clinically important head-to-head/combination RCTs.
- Current diagnostic consensus/guidance for DSPN and small-fiber neuropathy, including atypical/red-flag work-up.

Acceptance requires exact bibliographic metadata, direct source access, relevant quotation/section locator, and evidence classification.

### Wave 1 discovery leads (not yet accepted citations)

`dpnp-source-provenance` has identified candidate records for each class above via discovery MCPs; none are accepted until the owning specialist opens the primary record directly and logs a locator/quotation. Full detail, verification tier, and open gaps are in `10_SOURCES/SOURCE_REGISTER.md`:

- ADA Standards of Care in Diabetes—2026, Ch.12 (Retinopathy, Neuropathy, and Foot Care) — `IDENTIFIED_MULTI_SNIPPET`, DOI not yet fully confirmed.
- AAN 2022 practice guideline update on painful diabetic polyneuropathy (*Neurology* 2022;98:31–43) — `IDENTIFIED_MULTI_SNIPPET`.
- Taiwan TFDA and FDA Pregabalin label/safety communications — `NOT_YET_SEARCHED` (search interrupted/failed this wave; retry pending).
- Candidate trials/SR-MA: Freeman et al. 2008 (*Diabetes Care*, pregabalin 7-RCT pooled analysis), Soliman et al. 2025 (*Lancet Neurol*, pharmacotherapy/neuromodulation SR-MA), Mallick-Searle & Adler 2024 (*J Pain Res*, guideline-landscape review), a 2026 Frontiers in Endocrinology pregabalin+duloxetine combination SR-MA — all `IDENTIFIED_SECONDARY_CITATION` or `IDENTIFIED_MULTI_SNIPPET`, none opened at primary record yet.
- Toronto Consensus (Tesfaye et al. 2010) remains the leading candidate for the DSPN/small-fiber-neuropathy diagnostic-consensus source; not yet independently verified.
