# Full-text Acquisition & Parse Ledger

Owner: `dpnp-source-provenance`. Governed by `FULLTEXT_POLICY.md`. No PDFs have been downloaded or parsed this wave — this ledger records identified lawful routes only, per source in `SOURCE_REGISTER.md`.

| Source | Lawful route identified | Access status | Downloaded | Parser used | Notes |
|---|---|---|---|---|---|
| MEDNOTE-001 | Public web page | Fetched (WebFetch, rendered markdown) | N/A (not a PDF) | N/A | See `MEDNOTE_CAPTURE.md` |
| MEDNOTE-002 | Public web page | Fetched (WebFetch, rendered markdown) | N/A (not a PDF) | N/A | See `MEDNOTE_CAPTURE.md`; fallback acquisition route not needed |
| B1 ADA Standards of Care 2026 Ch.12 | PMC (open access, NIH public repository) — https://pmc.ncbi.nlm.nih.gov/articles/PMC12690177 | Identified, not yet opened directly | No | — | Diabetes Care/ADA typically deposits Standards of Care to PMC as open access; verify license on direct open |
| B2 AAN 2022 guideline (Neurology 2022;98:31–43) | To be checked: AAN.com guideline summary page (likely free) vs Neurology journal (may be subscription) vs PMC | Not yet located at primary record | No | — | Check PMC/PubMed Central first for OA status before assuming paywall |
| B3 Taiwan TFDA Pregabalin label | TFDA 藥物許可證 / 仿單 public database (public regulatory record) | Not yet searched | No | — | Search interrupted this wave |
| B4 FDA Pregabalin label | DailyMed (dailymed.nlm.nih.gov) — public NIH mirror of FDA label | Not yet opened | No | — | Preferred over accessdata.fda.gov for fetch reliability |
| C1 Freeman 2008 (Diabetes Care) | To be checked: PMC / journal OA status | Not yet located at primary record | No | — | Currently only known via ADA 2026 chapter's reference list |
| C2 Soliman 2025 (Lancet Neurol) | Likely subscription (Lancet Neurology); check for author manuscript/PMC embargo copy | Not yet located at primary record | No | — | Do not attempt paywall bypass; if no lawful OA copy exists, register as abstract-only |
| C3 Mallick-Searle 2024 (J Pain Res) | Dove Press — typically full open access | Not yet located at primary record | No | — | J Pain Res is a Dove Medical Press OA journal; expect freely available PDF |
| C4 Frontiers 2026 combination SR/MA | Frontiers in Endocrinology — full open access (CC-BY typical) | Identified via search snippet, not yet opened directly | No | — | https://www.frontiersin.org/journals/endocrinology/articles/10.3389/fendo.2026.1750441/full |

## Policy compliance notes

- No Sci-Hub, no paywall bypass attempted or used this wave.
- No LlamaParse invocation this wave (no PDFs acquired yet).
- No credentials of any kind written to this repository.
- `fulltext-local/` not yet created; will be added (and must be confirmed `.gitignore`d) only once a PDF is actually downloaded.
