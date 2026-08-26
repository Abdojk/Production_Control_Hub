# COVERAGE_STATE.md — Numerator source for coverage maths

> **Version lock:** D365 SCM 10.0.47 (build 10.0.2527)
> **Map version tracked:** KNOWLEDGE_MAP.md v0.5
> **Last updated:** 2026-05-31
> Every percentage in a `How_much_do_You_know?` readout must trace to the counts below. No estimates.
>
> **Two distinct metrics — do not conflate:**
> - **Skeleton completeness (Mission 1):** how much of the map is enumerated.
> - **Verified-knowledge % (Mission 2):** VERIFIED controls / total. This is the "80%" target metric.

## Mission 1 — skeleton completeness
- Groups enumerated to Level 4: **5 / 5**
- Forms enumerated: **35**
- Controls enumerated (denominator): **210**
- All forms remain `skeleton-partial` — denominator may still grow.

## Mission 2 — verified-knowledge (the "80%" target metric)
- Verified: **138 / 210 = 65.7%**
- Unconfirmed: **0 / 210 = 0.0%**
- Unknown: **72 / 210 = 34.3%**
- On a /100 scale: **X = 65.7 / 100** (138 controls verified).
- **Setup group: COMPLETE** — 138/143 verified; the 5 remaining are honestly UNKNOWN (no Tier-1 source).

## Per-group tally

| Group | Total controls | Verified | Unconfirmed | Unknown | Level-4? |
|---|---|---|---|---|---|
| 1. Setup | 143 | 138 | 0 | 5 | Yes |
| 2. Common / Daily | 31 | 0 | 0 | 31 | Yes |
| 3. Journals | 16 | 0 | 0 | 16 | Yes |
| 4. Inquiries and reports | 4 | 0 | 0 | 4 | Yes (provisional) |
| 5. Periodic tasks | 16 | 0 | 0 | 16 | Yes |
| **Total** | **210** | **138** | **0** | **72** | |

## Setup group — per-form tally (denominator = 143; VERIFIED 138 / UNKNOWN 5)

| Form code | Form | Controls | Verified | Unknown |
|---|---|---|---|---|
| PARAMS | Production control parameters | 50 | 49 | 1 |
| PARAMSITE | Production control parameters by site | 15 | 15 | 0 |
| JOURNALNAMES | Production journal names | 10 | 6 | 4 |
| POOLS | Production pools | 2 | 2 | 0 |
| GROUPS | Production groups | 3 | 3 | 0 |
| UNITS | Production units | 4 | 4 | 0 |
| ALLOCKEYS | Allocation keys | 3 | 3 | 0 |
| PROPS | Properties | 2 | 2 | 0 |
| TRACKEDCOMP | Tracked components policy | 2 | 2 | 0 |
| MES-DEFAULTS | Production order defaults | 8 | 8 | 0 |
| MES-PFE | Configure production floor execution | 24 | 24 | 0 |
| ROUTES-OPS | Operations | 3 | 3 | 0 |
| ROUTES-RG | Route groups | 7 | 7 | 0 |
| COSTCAT | Cost categories | 4 | 4 | 0 |
| COSTGRP | Cost groups | 3 | 3 | 0 |
| ROUTES-ROUTE | Routes / Route version | 3 | 3 | 0 |
| **Setup total** | | **143** | **138** | **5** |

The 5 Setup UNKNOWNs (no Tier-1 source describes their effect):
- `PARAMS-048` Lean manufacturing default parameters
- `JOURNALNAMES-004` Default private user group
- `JOURNALNAMES-005` Delete lines after posting
- `JOURNALNAMES-006` Default posting summation level
- `JOURNALNAMES-007` Voucher number allocation rule

## Common / Journals / Inquiries / Periodic — per-form tally (all UNKNOWN)
| Group | Form code | Controls |
|---|---|---|
| Common | PORD / BORD / KPROC / KTRANS / KSCHED / PFE-RUN | 31 |
| Journals | J-PICK / J-ROUTE / J-JOB / J-RAF | 16 |
| Inquiries | RPT (provisional) | 4 |
| Periodic | KANBANCALC / KANBANRULES / UPDATE / CLEANUP | 16 |

## Screens flagged `skeleton-partial`
All 35 enumerated forms remain provisional. Setup is content-complete for the documented fields; PARAMS still has Documents / Number sequences / full Status matrix tabs unenumerated.

## Resume pointer
- **Setup group: DONE** (138/143 VERIFIED, 5 honest UNKNOWN). Stop point reached per plan.
- **Next (new instruction needed):** begin Group 2 (Common / Daily) — production-order lifecycle controls (PORD 11) have strong Tier-1 task guides already fetched (create/release/start/RAF/end). Enriching Common+Journals would take the module toward ~88%.
- To clear the 5 Setup UNKNOWNs: need a dedicated Tier-1 source for production journal-name posting/voucher fields and the lean-manufacturing parameter defaults.
