# Run Manifest

- PROJECT_ID: `dpnp-pregabalin-moderator`
- RUN_ID: `2026-09-03-v1`
- Started: `2026-09-03` (Asia/Taipei)
- Host: `Anders-Mac-mini.local` / Tailscale `anders-mac-mini`
- Working path: `/Users/ander/Documents/medical/diabetes/neuropathy/DPNP`
- Git branch: `main`
- Git commit at initialization: `UNBORN`
- Git remote: `https://github.com/zinojeng/Pregabalin.git`
- Previous run: none identified
- Current Wave: `4 INDEPENDENT AUDIT — complete` (Waves 0-4 all complete; see `05_STATUS.md` for full gate history)
- Current Gate: **`READY_WITH_EXTERNAL_BLOCKER`** (Decision 2026-09-03-17 in `03_DECISION-LOG.md`) — research/synthesis/audit complete with `PASS_WITH_MINOR_ISSUES` (both findings fixed); NOT marked `FINAL` because the LlamaParse network blocker (Decision 2026-09-03-15) remains open per explicit Human PI instruction not to waive it.

## Persistent session topology

```text
Human PI
  └─ dpnp-research-director
       ├─ dpnp-source-provenance
       ├─ dpnp-guideline-diagnosis
       ├─ dpnp-trials-comparative
       └─ dpnp-pregabalin-safety

After integration only:
  └─ temporary independent read-only auditor
```

## Input identity

| Input | Size | Modified | SHA-256 | Role |
|---|---:|---|---|---|
| `Claude_Code_Cross-Session_Research_完整建議與經驗_Runbook.md` | 38,726 bytes | 2026-09-03T05:32:35+0800 | `73137596b86f012d847c3c5602a1700a2d81a7da6195d6380c178b03e046f639` | operating SOP |

## Output folders

- `10_SOURCES/`: source register, lawful full-text and parse ledger
- `20_EVIDENCE/guidelines-diagnosis/`: diagnostic/guideline review
- `20_EVIDENCE/trials-comparative/`: RCT, meta-analysis, comparative treatment evidence
- `20_EVIDENCE/pregabalin-safety/`: dose, safety, special populations, implementation
- `30_METHODS/`: search methods, inclusion criteria, evidence grading
- `40_SYNTHESIS/`: Director-approved Traditional Chinese briefing and 10 QA
- `90_CROSS-SESSION-LOG/`: concise routing/health records
- `99_FINAL-QA.md`: auditor-only report

## Source guardrails

- Do not commit secrets or restricted full text.
- Do not use unauthorized paywall bypass routes.
- Do not treat AI-generated summaries, search snippets, or MedNote derivative summaries as primary evidence.
- Record publication date and search/access date separately.
