# COVERAGE_STATE.md — Numerator source for coverage maths

> **Version lock:** D365 SCM 10.0.47 (build 10.0.2527)
> **Map version tracked:** KNOWLEDGE_MAP.md v0.3
> **Last updated:** 2026-05-31
> Every percentage in a `How_much_do_You_know?` readout must trace to the counts below. No estimates.
>
> **Two distinct metrics — do not conflate:**
> - **Skeleton completeness (Mission 1):** how much of the map is enumerated. Growing this is *not* "knowing" the module.
> - **Verified-knowledge % (Mission 2):** VERIFIED controls / total. This is the standing-instruction coverage metric and the basis of any "80%" target.

## Mission 1 — skeleton completeness
- Groups enumerated to Level 4: **5 / 5** (all groups)
- Forms enumerated: **35** (Setup 16, Common 6, Journals 4, Inquiries 1 bucket, Periodic 4)
- Controls enumerated (denominator): **190**
- All 35 forms flagged `skeleton-partial` — denominator is provisional and expected to grow during enrichment.

## Mission 2 — verified-knowledge (the "80%" target metric)
- Verified: **49 / 190 = 25.8%**
- Unconfirmed: **0 / 190 = 0.0%**
- Unknown: **141 / 190 = 74.2%**
- On a /100 scale: **X = 25.8 / 100** (49 controls verified).

## Per-group tally

| Group | Total controls | Verified | Unconfirmed | Unknown | Level-4? |
|---|---|---|---|---|---|
| 1. Setup | 123 | 49 | 0 | 74 | Yes |
| 2. Common / Daily | 31 | 0 | 0 | 31 | Yes |
| 3. Journals | 16 | 0 | 0 | 16 | Yes |
| 4. Inquiries and reports | 4 | 0 | 0 | 4 | Yes (provisional) |
| 5. Periodic tasks | 16 | 0 | 0 | 16 | Yes |
| **Total** | **190** | **49** | **0** | **141** | |

## Setup group — per-form tally (denominator = 123)

| Form code | Form | Controls | Unknown |
|---|---|---|---|
| PARAMS | Production control parameters | 50 | 1 (49 VERIFIED) |
| PARAMSITE | Production control parameters by site | 15 | 15 |
| JOURNALNAMES | Production journal names | 10 | 10 |
| POOLS | Production pools | 2 | 2 |
| GROUPS | Production groups | 3 | 3 |
| UNITS | Production units | 4 | 4 |
| ALLOCKEYS | Allocation keys | 3 | 3 |
| PROPS | Properties | 2 | 2 |
| TRACKEDCOMP | Tracked components policy | 2 | 2 |
| MES-DEFAULTS | Production order defaults | 6 | 6 |
| MES-PFE | Configure production floor execution | 6 | 6 |
| ROUTES-OPS | Operations | 3 | 3 |
| ROUTES-RG | Route groups | 7 | 7 |
| COSTCAT | Cost categories | 4 | 4 |
| COSTGRP | Cost groups | 3 | 3 |
| ROUTES-ROUTE | Routes / Route version | 3 | 3 |

## Common / Journals / Inquiries / Periodic — per-form tally
| Group | Form code | Controls |
|---|---|---|
| Common | PORD (All production orders) | 11 |
| Common | BORD (All batch orders) | 6 |
| Common | KPROC (Kanban board for process jobs) | 4 |
| Common | KTRANS (Kanban board for transfer jobs) | 4 |
| Common | KSCHED (Kanban schedule board) | 3 |
| Common | PFE-RUN (Production floor execution runtime) | 3 |
| Journals | J-PICK / J-ROUTE / J-JOB / J-RAF | 4 each = 16 |
| Inquiries | RPT (provisional bucket) | 4 |
| Periodic | KANBANCALC | 5 |
| Periodic | KANBANRULES | 3 |
| Periodic | UPDATE | 5 |
| Periodic | CLEANUP | 3 |

## Screens flagged `skeleton-partial`
All 35 enumerated forms. Highest-value skeleton-completion candidates: PARAMS, PARAMSITE (Documents / Number sequences / full Status matrix tabs not yet enumerated); PORD (full Action Pane).

## Resume pointer
- **Mission 1 (skeleton):** all 5 groups at Level 4 (`skeleton-partial`).
- **Mission 2 (enrichment):** IN PROGRESS. PARAMS form done (49/50 VERIFIED; PARAMS-048 lean defaults left UNKNOWN). **Next batch:** `JOURNALNAMES` (10) + `ROUTES-RG` (7) + `MES-DEFAULTS` (6) + `MES-PFE` (6) — all have Tier-1 material already fetched this session.
