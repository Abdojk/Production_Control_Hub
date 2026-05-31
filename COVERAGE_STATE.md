# COVERAGE_STATE.md — Numerator source for coverage maths

> **Version lock:** D365 SCM 10.0.47 (build 10.0.2527)
> **Map version tracked:** KNOWLEDGE_MAP.md v0.1
> **Last updated:** 2026-05-31
> Every percentage in a `How_much_do_You_know?` readout must trace to the counts below. No estimates.

## Per-group tally

| Group | Total controls | Verified | Unconfirmed | Unknown | Level-4 enumerated? |
|---|---|---|---|---|---|
| 1. Setup | 123 | 0 | 0 | 123 | Yes |
| 2. Common / Daily | — | 0 | 0 | — | No (Level 4 deferred) |
| 3. Journals | — | 0 | 0 | — | No (Level 4 deferred) |
| 4. Inquiries and reports | — | 0 | 0 | — | No (Level 4 deferred) |
| 5. Periodic tasks | — | 0 | 0 | — | No (Level 4 deferred) |

## Setup group — per-form tally (denominator = 123)

| Form code | Form | Controls | Verified | Unconfirmed | Unknown |
|---|---|---|---|---|---|
| PARAMS | Production control parameters | 50 | 0 | 0 | 50 |
| PARAMSITE | Production control parameters by site | 15 | 0 | 0 | 15 |
| JOURNALNAMES | Production journal names | 10 | 0 | 0 | 10 |
| POOLS | Production pools | 2 | 0 | 0 | 2 |
| GROUPS | Production groups | 3 | 0 | 0 | 3 |
| UNITS | Production units | 4 | 0 | 0 | 4 |
| ALLOCKEYS | Allocation keys | 3 | 0 | 0 | 3 |
| PROPS | Properties | 2 | 0 | 0 | 2 |
| TRACKEDCOMP | Tracked components policy | 2 | 0 | 0 | 2 |
| MES-DEFAULTS | Production order defaults | 6 | 0 | 0 | 6 |
| MES-PFE | Configure production floor execution | 6 | 0 | 0 | 6 |
| ROUTES-OPS | Operations | 3 | 0 | 0 | 3 |
| ROUTES-RG | Route groups | 7 | 0 | 0 | 7 |
| COSTCAT | Cost categories | 4 | 0 | 0 | 4 |
| COSTGRP | Cost groups | 3 | 0 | 0 | 3 |
| ROUTES-ROUTE | Routes / Route version | 3 | 0 | 0 | 3 |
| **Total** | | **123** | **0** | **0** | **123** |

## Module roll-up (weighted by enumerated control count)
- Enumerated controls (Setup only this session): **123**
- Verified: **0 / 123 = 0.0%**
- Unconfirmed: **0 / 123 = 0.0%**
- Unknown: **123 / 123 = 100.0%**
- Groups 2–5 are not yet enumerated to Level 4, so they are excluded from the denominator and reported separately as "skeleton-only".

## Screens flagged `skeleton-partial`
All 16 Setup forms are currently `skeleton-partial` (Microsoft does not exhaustively document every field). PARAMS and PARAMSITE are the highest-priority candidates for skeleton completion during enrichment.

## Resume pointer
- **Mission 1 (Setup skeleton):** COMPLETE for this session's scope.
- **Mission 2 (enrichment):** NOT STARTED. Next control to learn: `PC-SETUP-PARAMS-004` (Ledger posting) — highest business impact, strong Tier-1 coverage already located.
- **Pending Level-4 work:** Groups 2–5; full enumeration of `skeleton-partial` Setup forms.
