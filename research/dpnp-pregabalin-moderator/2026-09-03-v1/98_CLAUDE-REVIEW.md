# Post-integration Claude CLI Review

- Date: 2026-09-03 (Asia/Taipei)
- Mode: independent, read-only branch review against `origin/main`
- Scope: all research artifacts added by the Claude Code cross-session run
- Critical findings: none
- Disposition: all high-confidence major/minor findings corrected before push

## Findings and disposition

1. **Restricted-source excerpt volume** — The AAN 2022 evidence table reproduced nearly every recommendation verbatim despite the recorded single-copy/personal-use restriction. **Fixed:** replaced with concise paraphrases while retaining Rec numbers, Level grades, DOI/PMID, and the local-only source path.
2. **Wrong PDF designated for LlamaParse retry** — The four earlier attempts used a superseded DailyMed 06/2020 PDF, whereas current safety evidence came from FDA Rev. 04/2025. **Fixed:** downloaded the actual FDA 04/2025/Reference ID 5578761 PDF, confirmed identity, recorded its SHA-256, and designated it as the only future retry target. A Human-PI-authorized Claude CLI attempt on the correct file returned `ConnectTimeout` and created no output, corroborating the network diagnosis. The 2020 file is explicitly historical.
3. **Unlocated dose-stratified adverse-event figures** — `SAFETY_TOPICS.md` retained 600 mg/day figures not transcribed with a primary-table locator, including one inconsistent ataxia value. **Fixed:** removed all three dose-stratified clauses; retained verified All-PGB comparisons and primary section/table references.
4. **OPTION-DM sample funnel** — QA Q3 omitted the intermediate 130 participants who started a pathway. **Fixed:** restored N=140 randomised → 130 started → 84 completed at least two pathways.
5. **Audience-facing internal reference** — The moderator brief pointed readers to the repository's audit file. **Fixed:** retained the evidentiary caveat but removed the internal audit reference.
6. **Stale status section** — `05_STATUS.md` still listed Wave 2 work as in progress. **Fixed:** removed the obsolete section.

## Final assessment

The clinical conclusions and sponsor-bias guardrails remain unchanged. The research package is suitable for use subject to the separately tracked infrastructure condition: the current FDA 04/2025 PDF was submitted once to LlamaParse but returned `ConnectTimeout`, so no parsed Markdown exists while outbound connectivity to `api.cloud.llamaindex.ai` remains blocked. The run must therefore remain `READY_WITH_EXTERNAL_BLOCKER`, not `FINAL`.
