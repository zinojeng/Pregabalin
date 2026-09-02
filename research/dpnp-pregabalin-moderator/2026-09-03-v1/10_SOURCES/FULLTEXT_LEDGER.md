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
- `mcp__llamaparse__parse_pdf_to_markdown` invoked 4 times total against the local file path across two turns: attempt 1 → `WriteTimeout`; attempts 2–4 → `ConnectTimeout`. No partial output saved on any attempt.

### Remediation-turn diagnosis (no credentials read or exposed)

- Confirmed the MCP's actual API host from `server.py` (code only, not the key file): `BASE_URL = "https://api.cloud.llamaindex.ai/api/v1/parsing"`, `REQUEST_TIMEOUT = httpx.Timeout(60.0, connect=15.0)`. The 15s connect-timeout / 60s overall-timeout configuration is reasonable and not the cause — the connection itself never completes within that window.
- No `HTTP_PROXY`/`HTTPS_PROXY`/`NO_PROXY` environment variables are set that could be misrouting or blocking traffic.
- DNS resolves correctly: `api.cloud.llamaindex.ai` → a Traefik/Kubernetes ELB (`k8s-traefik-...us-east-1.elb.amazonaws.com`) at multiple IPs (e.g., `35.173.170.221`).
- **Unauthenticated connectivity test** (bare `curl` GET, no API key, no file payload) to `https://api.cloud.llamaindex.ai/`: TCP connect can complete (`time_connect≈3.3s` when pinned to a specific resolved IP via `--resolve`) but **zero bytes are ever received afterward**, timing out after 15s with no TLS/HTTP response. A second run without pinning an IP timed out even at the connect stage (`curl: (28) Connection timed out`).
- By contrast, `curl` to `dailymed.nlm.nih.gov` and `google.com` succeeded normally in the same session (HTTP 200, sub-2s).
- **Conclusion:** this is a categorical network-egress block/stall specific to `api.cloud.llamaindex.ai` from this sandboxed environment — not a file-size, upload-size, or PDF-content issue, and not an application-level timeout misconfiguration. The identical stall reproduces on a bare unauthenticated GET carrying no payload at all, which rules out "smaller PDF" as a fix: any request to this host stalls the same way regardless of what is sent. On this basis, source-provenance did not spend a further download+attempt cycle on the Frontiers 2026 SR-MA PDF as a size-based mitigation, since the diagnostic step already isolates the failure to network reachability of the destination host, independent of payload — happy to run that specific file anyway if the Director/PI wants the confirming data point for the record.
- One bounded LlamaParse retry was executed this turn on the already-downloaded FDA PDF (no re-download) per Director dispatch: result `ConnectTimeout`, consistent with the diagnosis above.

- **Status: BLOCKED_NETWORK** (upgraded from `BLOCKED_TOOL_FAILURE` now that root cause is isolated) — the download step succeeded and the checksum is recorded above; the parse step cannot succeed from this environment until network egress to `api.cloud.llamaindex.ai` is restored (this is outside `dpnp-source-provenance`'s remediation scope — it is an environment/infrastructure condition, not a source-provenance or file-provenance defect). No local parser (e.g., `pdftotext`) was substituted as a stand-in for "LlamaParse-parsed," per Director instruction — the PI named that specific tool.
- Interim mitigation (unchanged): the label's clinically relevant content (indications, renal dose-adjustment table, boxed-warning status, key warnings, adverse-reaction rates) was already captured via direct WebFetch of the DailyMed HTML page (see `SOURCE_REGISTER.md` B4) and is available to `dpnp-pregabalin-safety` now.

## Policy compliance notes

- No Sci-Hub, no paywall bypass attempted or used.
- Exactly one PDF downloaded this wave (B4, FDA/public-domain); zero PDFs downloaded for any copyrighted/TDM-restricted source (B1 explicitly declined on license grounds).
- No credentials of any kind written to this repository, prompts, logs, or citations.
- `fulltext-local/` created under this run folder; confirmed covered by the repo's existing `**/fulltext-local/` `.gitignore` rule before and after the download.
