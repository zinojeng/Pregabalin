# Status

- Updated: 2026-09-03 (Asia/Taipei)
- Current Wave: `2 METHODS/EVIDENCE (guideline, trials, safety)`
- Current Gate: `Gate 1 = READY_WITH_PENDING_ITEMS` (Decision 2026-09-03-05)

## Completed

- Runbook reviewed.
- Target Mac mini/Tailscale identity verified.
- Claude Code authentication verified.
- Public GitHub output repository verified empty at start.
- Research Charter, ownership, source policy, and sponsor-bias guardrail initialized.
- Existing global MCP names inventoried; no credential copied into the repository.
- `academic-research-agents` implementation inspected and classified as architecture-only because core literature/PDF methods contain placeholders.
- Cross-session health check PASSED: all four persistent peers (`dpnp-source-provenance`, `dpnp-guideline-diagnosis`, `dpnp-trials-comparative`, `dpnp-pregabalin-safety`) located via `ListAgents` and confirmed READY. See `90_CROSS-SESSION-LOG/2026-09-03_STARTUP.md`.
- Wave 1 dispatched to and completed by `dpnp-source-provenance`: both MedNote pages captured (`10_SOURCES/MEDNOTE_CAPTURE.md`), source/search register built (`10_SOURCES/SOURCE_REGISTER.md`) covering ADA 2026 Ch.12, AAN 2022 update, 4 trial/SR-MA leads, Toronto Consensus lead; full-text ledger opened (`10_SOURCES/FULLTEXT_LEDGER.md`); `02_SOURCE-INVENTORY.md` updated with a preserved "not yet accepted" framing. No PDFs downloaded/parsed, no Sci-Hub/paywall bypass, no credentials committed.
- Gate 1 declared `READY_WITH_PENDING_ITEMS` (Decision 2026-09-03-05) — sufficient lead coverage to unblock Wave 2 deep verification; real gaps remain (see Open Questions).
- Wave 2 dispatched to `dpnp-guideline-diagnosis`, `dpnp-trials-comparative`, `dpnp-pregabalin-safety`.

## In progress

- `dpnp-source-provenance`: closing remaining gaps in its own scope — Taiwan TFDA and FDA/DailyMed Pregabalin label discovery, ADA Ch.12 DOI confirmation.
- `dpnp-guideline-diagnosis`: open and verify ADA 2026 Ch.12, AAN 2022 update, and Toronto Consensus at their primary records with exact quotations/locators.
- `dpnp-pregabalin-safety`: independently search for the Taiwan/FDA Pregabalin label rather than wait on source-provenance; verify labeling and safety evidence.

## Completed (Wave 2, partial)

- `dpnp-trials-comparative`: Wave 2 evidence table complete (`20_EVIDENCE/trials-comparative/01_EVIDENCE-TABLE.md`) — T1 Freeman 2008, T2 Frontiers 2026 combo SR-MA, T3 Soliman/NeuPSIG 2025, T4 Mallick-Searle 2024 (narrative review), T5 COMBO-DN, T6 OPTION-DM all `ACCESS_VERIFIED` at primary record. Key counter-bias findings recorded (Decision 2026-09-03-06): α2δ-ligand class NNT ranks numerically worst of the three first-line classes per Soliman/NeuPSIG 2025; COMBO-DN found no significant combination-vs-monotherapy superiority; OPTION-DM found no pregabalin-pathway superiority over amitriptyline/duloxetine pathways. Standing by for Gate 2 reconciliation with guideline-diagnosis and pregabalin-safety. `NEEDS_FULLTEXT`/`NEEDS_SOURCE` gaps logged, non-blocking.

## Pending gates

- Gate 1: `READY_WITH_PENDING_ITEMS` (partial — see above).
- Gate 2: guideline, comparative evidence, and safety findings reconciled; challenge round run.
- Gate 3: Traditional Chinese synthesis and exactly 10 QA internally consistent.
- Final Gate: independent read-only QA.

## Blockers

- None hard-blocking; several `NEEDS_SOURCE`/`NEEDS_EVIDENCE` items open (see `04_OPEN-QUESTIONS.md`). No claim may cite MEDNOTE-002's numeric figures (NNT/NNH/discontinuation) until independently sourced to a primary study.
