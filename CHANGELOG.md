# CHANGELOG.md — Map versions, discovered controls, MS page revisions

> **Version lock baseline:** D365 SCM 10.0.47 (build 10.0.2527)

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
