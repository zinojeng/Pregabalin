# DPNP Pregabalin Cross-session Research

PROJECT_ID: `dpnp-pregabalin-moderator`

Current run: `research/dpnp-pregabalin-moderator/2026-09-03-v1/`

Before substantive work, read in order:

1. `Claude_Code_Cross-Session_Research_完整建議與經驗_Runbook.md`
2. `research/dpnp-pregabalin-moderator/2026-09-03-v1/00_RUN-MANIFEST.md`
3. `01_RESEARCH-CHARTER.md`
4. `02_SOURCE-INVENTORY.md`
5. `03_DECISION-LOG.md`
6. `04_OPEN-QUESTIONS.md`
7. `05_STATUS.md`

## Non-negotiable rules

- Cross-session outside, workflow inside. Existing persistent peers must be reached with `ListAgents` and `SendMessage`; do not silently replace an unreachable peer.
- Repository files are the durable source of truth. Chat messages are the control plane only.
- Work by Wave and Gate. Do not draft final synthesis before sources and claims are verified.
- Preserve exact numeric tokens, recommendation identifiers, and grades. Preserve exact guideline wording only in lawful local-only source notes or short attributed excerpts; use faithful paraphrase in public-repository tables when redistribution terms are restrictive. Flag discrepancies; never silently repair them.
- Every important claim must be traceable to a primary source with DOI, PMID, stable URL, publication date, access date, and page/table/section when available.
- Separate `DIRECT EVIDENCE`, `INDIRECT EVIDENCE`, `GUIDELINE / CONSENSUS`, `OBSERVATIONAL EVIDENCE`, `MECHANISTIC SUPPORT`, `EXPERT INTERPRETATION`, and `INSUFFICIENT EVIDENCE`.
- Use Traditional Chinese for narrative outputs where practical. Keep drug names, scales, guideline names, trial acronyms, and technical terms in original English when that is clearer.
- This is a Pregabalin-sponsored moderator project. Explicitly manage sponsor bias: no unsupported superiority claim, class-wide extrapolation, selective safety reporting, or omission of reasonable alternatives.
- Compare Pregabalin fairly with other guideline-supported drug classes and non-pharmacologic/multidisciplinary care.
- State that treatment goals are pain, sleep, function, and quality of life; do not imply that analgesic therapy reverses nerve damage unless direct evidence supports it.
- No patient-specific medical advice. Highlight red flags, differential diagnosis, renal dose adjustment, CNS depression/falls, edema/weight gain, withdrawal/tapering, misuse/dependence, and combination-risk considerations where evidence supports them.

## Literature and full-text policy

- Preferred discovery: PubMed/NCBI, Crossref, OpenAlex, guideline organizations, regulatory agencies, trial registries, and the configured `paper-search`, `google-scholar`, `research_hub`, `openevidence`, or equivalent MCPs.
- Discovery tools are leads, not evidence. Verify every included claim against the primary publication or authoritative guideline.
- Full text may be obtained only through lawful routes: PubMed Central, publisher/open-access links, author manuscripts, institutional/library access already authorized for the user, or files supplied by the user.
- Do not use Sci-Hub, bypass paywalls, evade authentication, or commit restricted/copyrighted full text to this public repository.
- The globally configured `llamaparse` MCP may parse lawfully acquired PDFs. Never place its API key or any other credential in the repository, prompts, logs, or citations.
- Store local-only PDFs under an ignored `fulltext-local/` directory. Commit only metadata, extraction notes, quotations within fair-use limits, and evidence tables unless redistribution rights are verified.
- `zinojeng/academic-research-agents` is an architecture reference only. Its local literature search/PDF parsing implementations were found to contain placeholders; do not treat its outputs as evidence without independent validation.

## Persistent roles and file ownership

| Role | Owned paths |
|---|---|
| `dpnp-research-director` | manifest, charter, decision log, open questions, status, cross-session log, final integration |
| `dpnp-guideline-diagnosis` | `20_EVIDENCE/guidelines-diagnosis/` |
| `dpnp-trials-comparative` | `20_EVIDENCE/trials-comparative/` |
| `dpnp-pregabalin-safety` | `20_EVIDENCE/pregabalin-safety/` |
| `dpnp-source-provenance` | `10_SOURCES/`, source register, full-text acquisition and parse ledger |
| Independent auditor | `99_FINAL-QA.md` only |
| One-time primary integrator (orchestration layer; not a persistent peer) | `98_CLAUDE-REVIEW.md` only |

The Director may integrate approved outputs into `40_SYNTHESIS/`. Specialists must not edit another role's owned files.
The one-time primary integrator is the external orchestration layer that runs the read-only review and records its disposition; it is ephemeral and must not be addressed through `ListAgents` or `SendMessage`.

## Cross-session message schema

Every message must include:

```text
[PROJECT] dpnp-pregabalin-moderator
[RUN] 2026-09-03-v1
[FROM]
[TO]
[TYPE]
[QUESTION or FINDING]
[IMPACT]
[ACTION]
[OUTPUT_PATHS]
[CONFIDENCE]
[STATUS]
```

Valid status values include `READY`, `READY_FOR_NEXT_WAVE`, `READY_WITH_PENDING_ITEMS`, `BLOCKED_FOR_SOURCE`, `BLOCKED_FOR_PI`, `BLOCKED_FOR_EVIDENCE`, and `PASS`.
