# CHANGELOG.md — Map versions, discovered controls, MS page revisions

> **Version lock baseline:** D365 SCM 10.0.47 (build 10.0.2527)

## v0.3 — 2026-05-31  (Mission 2 begins)
- **Enriched the Production control parameters (`PARAMS`) form:** 49 of 50 controls taken to
  **VERIFIED** with ON/OFF (or per-value) business effects, grounded in Tier-1 Microsoft sources
  (parameters training unit #5; production-posting #3/#4; dispensing #9).
- `PC-SETUP-PARAMS-048` (Lean manufacturing default parameters) left **UNKNOWN** — Microsoft does
  not enumerate per-state effects on this page; "Insufficient data to verify".
- **Verified-knowledge moved 0.0% → 25.8%** (49/190). This is the first real movement on the
  knowledge axis; prior versions only grew the skeleton.
- Full per-control records in `controls/setup/production-control-parameters.md`.

## v0.2 — 2026-05-31
- **Mission 1 extended to all groups.** Enumerated Groups 2–5 to Level 4 (`skeleton-partial`):
  Common/Daily (6 forms, 31 controls), Journals (4 forms, 16), Inquiries and reports
  (1 provisional bucket, 4), Periodic tasks (4 forms, 16). Module denominator now **190 controls**
  across **35 forms**; all UNKNOWN.
- Grounded in Tier-1 production-order lifecycle task guides, batch balancing, lean/kanban articles,
  and the ProdBatchOrderHeaderEntity CDM entity (SOURCES.md #15–27).
- **Discarded** Business Central search hits (different product); SCM/fin-ops only.
- **Clarification recorded:** "≈80%" is a Mission 2 (verified-knowledge) target, not a Mission 1
  (skeleton) measure. COVERAGE_STATE.md now separates *skeleton completeness* from
  *verified-knowledge %*. Verified-knowledge remains **0%** — no enrichment performed.
- Operational/inquiry Level-4 lists are partial: Microsoft does not document every Action Pane
  button or report; full enumeration of those needs sandbox/AOT inspection.

## v0.1 — 2026-05-31
- **Engine bootstrapped.** Created the knowledge directory per the standing instruction:
  KNOWLEDGE_MAP.md, COVERAGE_STATE.md, DEPENDENCIES.md, SOURCES.md, CHANGELOG.md, and
  `/controls/setup/` learning-record stubs.
- **Version stamped:** confirmed latest GA = 10.0.47 (build 10.0.2527) as of 2026-05-31
  (10.0.48 not GA until June 2026). Source #13/#14 in SOURCES.md.
- **Mission 1 — Setup group skeleton built to Level 4:** 16 forms, 123 controls, all status
  UNKNOWN. All Setup forms flagged `skeleton-partial` (Microsoft under-documents complete
  field lists).
- **Mission 1 — Levels 1–3 for non-Setup groups (Common/Daily, Journals, Inquiries and
  reports, Periodic tasks):** provisional form lists only; Level 4 deferred.
- **DEPENDENCIES.md seeded** with 11 Tier-1 directed links surfaced during the skeleton build
  (ledger posting prerequisites, site-parameter gating, dispensing chain, MES job-type matching).
- **No enrichment performed** (Mission 2 not started) — per agreed session scope.

### Known provisional items (to reconcile in later sessions)
- Non-Setup group Level-3 form lists are provisional — reconcile against live Production
  control navigation before Level-4 enumeration.
- PARAMS tabs not yet enumerated: Documents, Number sequences, and the full per-status
  update matrix on the Status tab.
- Setup forms POOLS / PROPS / UNITS / ALLOCKEYS / GROUPS have minimal documented field lists;
  expect the denominator to grow during enrichment.
