# Full-text Acquisition & Parse Ledger

Owner: `dpnp-source-provenance`. Governed by `FULLTEXT_POLICY.md`.

| Source | Lawful route identified | Access status | Downloaded | Parser used | Notes |
|---|---|---|---|---|---|
| MEDNOTE-001 | Public web page | Fetched (WebFetch, rendered markdown) | N/A (not a PDF) | N/A | See `MEDNOTE_CAPTURE.md` |
| MEDNOTE-002 | Public web page | Fetched (WebFetch, rendered markdown) | N/A (not a PDF) | N/A | See `MEDNOTE_CAPTURE.md`; fallback acquisition route not needed |
| B1 ADA Standards of Care 2026 Ch.12 | PMC — https://pmc.ncbi.nlm.nih.gov/articles/PMC12690177 (DOI 10.2337/dc26-S012, PMID 41358886) | Page opened directly; license read | **BLOCKED_LICENSE** — not downloaded/parsed | — | License states "© 2025 by the American Diabetes Association... may not be reproduced, distributed, or used for text or data mining, machine learning, or similar technologies without prior written permission." Running LlamaParse (an ML-based extraction tool) over this PDF without ADA's written permission would breach the stated license — declining per `CLAUDE.md`'s "no unlawful full-text acquisition" and `FULLTEXT_POLICY.md`'s "lawful routes only." Direct human-style reading and short verbatim quotation under the "educational, noncommercial, properly cited, unaltered" clause remains available to `dpnp-guideline-diagnosis` via the PMC page itself. |
| B2 AAN 2022 guideline (Neurology 2022;98:31–43) | Not yet checked for OA status | Not yet located at primary record | No | — | Owned by `dpnp-guideline-diagnosis` per Wave 2 dispatch — not pursued further here |
| B3 Taiwan TFDA Pregabalin label | TFDA/MOHW public pages | 2010 safety-alert page opened directly (HTML, not PDF) | N/A (HTML page, short content, fully captured via WebFetch text extraction — see `SOURCE_REGISTER.md` B3) | N/A | Current 仿單 (package insert) PDF for the marketed product still not located — open gap |
| **B4 FDA Pregabalin (LYRICA) label** | **DailyMed public SPL PDF endpoint** — `https://dailymed.nlm.nih.gov/dailymed/downloadpdffile.cfm?setId=60185c88-ecfd-46f9-adb9-b97c6b00a553` | **Downloaded** | **Yes** | **LlamaParse — FAILED, see below** | US federal regulatory content, no copyright (17 U.S.C. §105) — no TDM/license restriction. File: `fulltext-local/LYRICA_pregabalin_dailymed_60185c88.pdf`, 2,580,850 bytes, PDF v1.4. **SHA-256: `69e1d9136622fbdd94898da954476474446db4f7df540fc11925a5d368bee424`**. Downloaded 2026-09-03 via direct `curl` GET (HTTP 200); confirmed `.gitignore`d (`git check-ignore` verified) — not committed. |
| C1 Freeman 2008 (Diabetes Care) | Not yet checked for OA status | Not yet located at primary record | No | — | Owned by `dpnp-trials-comparative` per Wave 2 dispatch — not pursued further here |
| C2 Soliman 2025 (Lancet Neurol) | Likely subscription; check for author-manuscript/PMC embargo copy | Not yet located at primary record | No | — | Owned by `dpnp-trials-comparative` — do not attempt paywall bypass |
| C3 Mallick-Searle 2024 (J Pain Res) | Dove Press — typically full open access | Not yet located at primary record | No | — | Owned by `dpnp-trials-comparative` |
| C4 Frontiers 2026 combination SR/MA | Frontiers in Endocrinology — full open access (CC-BY typical) | Identified via search snippet, not yet opened directly | No | — | Owned by `dpnp-trials-comparative` — https://www.frontiersin.org/journals/endocrinology/articles/10.3389/fendo.2026.1750441/full |

## B4 LlamaParse attempt log (PI-directed download+parse task)

- PDF downloaded successfully (see row above).
- `mcp__llamaparse__parse_pdf_to_markdown` invoked 3 times against the local file path: attempt 1 → `WriteTimeout`; attempts 2–3 → `ConnectTimeout`. No partial output saved.
- Direct network egress to other hosts was confirmed working in this session (e.g., `dailymed.nlm.nih.gov`, `google.com` via `curl` both succeeded), so this appears to be a LlamaParse-service-specific connectivity issue from this environment, not a general network block — consistent with earlier same-wave Tavily `ETIMEDOUT` failures on unrelated calls.
- **Status: BLOCKED_TOOL_FAILURE** for the parse step only — the download step itself succeeded and the checksum is recorded above. Not retried a 4th time this turn per loop-avoidance guidance; will retry once more in a later turn if re-dispatched, or hand off if the tool remains unavailable.
- Interim mitigation: the label's clinically relevant content (indications, renal dose-adjustment table, boxed-warning status, key warnings, adverse-reaction rates) was already captured via direct WebFetch of the DailyMed HTML page (see `SOURCE_REGISTER.md` B4) and is available to `dpnp-pregabalin-safety` now, pending the LlamaParse markdown as a secondary cross-check against the PDF's exact typesetting/tables.

## Policy compliance notes

- No Sci-Hub, no paywall bypass attempted or used.
- Exactly one PDF downloaded this wave (B4, FDA/public-domain); zero PDFs downloaded for any copyrighted/TDM-restricted source (B1 explicitly declined on license grounds).
- No credentials of any kind written to this repository, prompts, logs, or citations.
- `fulltext-local/` created under this run folder; confirmed covered by the repo's existing `**/fulltext-local/` `.gitignore` rule before and after the download.
