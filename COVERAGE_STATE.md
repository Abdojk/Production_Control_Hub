# COVERAGE_STATE.md — Numerator source for coverage maths

> **Version lock:** D365 SCM 10.0.47 (build 10.0.2527)
> **Map version tracked:** KNOWLEDGE_MAP.md v0.4
> **Last updated:** 2026-05-31
> Every percentage in a `How_much_do_You_know?` readout must trace to the counts below. No estimates.
>
> **Two distinct metrics — do not conflate:**
> - **Skeleton completeness (Mission 1):** how much of the map is enumerated.
> - **Verified-knowledge % (Mission 2):** VERIFIED controls / total. This is the "80%" target metric.

## Mission 1 — skeleton completeness
- Groups enumerated to Level 4: **5 / 5**
- Forms enumerated: **35**
- Controls enumerated (denominator): **210** (grew from 190: MES-DEFAULTS 6→8, MES-PFE 6→24 during enrichment)
- All forms remain `skeleton-partial` — denominator may still grow.

## Mission 2 — verified-knowledge (the "80%" target metric)
- Verified: **107 / 210 = 51.0%**
- Unconfirmed: **0 / 210 = 0.0%**
- Unknown: **103 / 210 = 49.0%**
- On a /100 scale: **X = 51.0 / 100** (107 controls verified).

## Per-group tally

| Group | Total controls | Verified | Unconfirmed | Unknown | Level-4? |
|---|---|---|---|---|---|
| 1. Setup | 143 | 107 | 0 | 36 | Yes |
| 2. Common / Daily | 31 | 0 | 0 | 31 | Yes |
| 3. Journals | 16 | 0 | 0 | 16 | Yes |
| 4. Inquiries and reports | 4 | 0 | 0 | 4 | Yes (provisional) |
| 5. Periodic tasks | 16 | 0 | 0 | 16 | Yes |
| **Total** | **210** | **107** | **0** | **103** | |

## Setup group — per-form tally (denominator = 143)

| Form code | Form | Controls | Verified | Unknown |
|---|---|---|---|---|
| PARAMS | Production control parameters | 50 | 49 | 1 |
| PARAMSITE | Production control parameters by site | 15 | 15 | 0 |
| JOURNALNAMES | Production journal names | 10 | 4 | 6 |
| POOLS | Production pools | 2 | 0 | 2 |
| GROUPS | Production groups | 3 | 0 | 3 |
| UNITS | Production units | 4 | 0 | 4 |
| ALLOCKEYS | Allocation keys | 3 | 0 | 3 |
| PROPS | Properties | 2 | 0 | 2 |
| TRACKEDCOMP | Tracked components policy | 2 | 0 | 2 |
| MES-DEFAULTS | Production order defaults | 8 | 8 | 0 |
| MES-PFE | Configure production floor execution | 24 | 24 | 0 |
| ROUTES-OPS | Operations | 3 | 0 | 3 |
| ROUTES-RG | Route groups | 7 | 7 | 0 |
| COSTCAT | Cost categories | 4 | 0 | 4 |
| COSTGRP | Cost groups | 3 | 0 | 3 |
| ROUTES-ROUTE | Routes / Route version | 3 | 0 | 3 |
| **Setup total** | | **143** | **107** | **36** |

## Common / Journals / Inquiries / Periodic — per-form tally (all UNKNOWN)
| Group | Form code | Controls |
|---|---|---|
| Common | PORD / BORD / KPROC / KTRANS / KSCHED / PFE-RUN | 31 |
| Journals | J-PICK / J-ROUTE / J-JOB / J-RAF | 16 |
| Inquiries | RPT (provisional) | 4 |
| Periodic | KANBANCALC / KANBANRULES / UPDATE / CLEANUP | 16 |

## Screens flagged `skeleton-partial`
All 35 enumerated forms. Note: PARAMS still has Documents / Number sequences / full Status matrix tabs unenumerated; JOURNALNAMES has 6 voucher/posting fields awaiting a Tier-1 source.

## Resume pointer
- **Mission 2 (enrichment):** IN PROGRESS — **X = 51.0/100 (107/210)**.
- **Setup remaining (36 unknown):** JOURNALNAMES voucher fields (6), POOLS (2), GROUPS (3), UNITS (4), ALLOCKEYS (3), PROPS (2), TRACKEDCOMP (2), ROUTES-OPS (3), COSTCAT (4), COSTGRP (3), ROUTES-ROUTE (3), PARAMS-048 (1).
- **Next batch options:** finish Setup group (→ ~68% module) via the small remaining forms + a journal-names source; or start Group 2 (Common) production-order lifecycle controls (strong Tier-1 task guides already fetched).
