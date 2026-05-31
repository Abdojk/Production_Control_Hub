# KNOWLEDGE_MAP.md — D365 F&O Production Control Knowledge Map (Skeleton)

> **Version lock:** Dynamics 365 Supply Chain Management **10.0.47** (build **10.0.2527**) — GA self-update March 2026 (latest GA as of 2026-05-31). 10.0.48 (build 10.0.2645) is not GA until June 2026.
> **Map version:** v0.1
> **Last updated:** 2026-05-31
> **Purpose:** This map is the *denominator* for all coverage maths. Levels 1–4 below. Every Level-4 control has a unique ID and a status. This session enumerates **Setup** to Level 4; all other groups are **Level 1–3 only (Level 4 deferred)**.

## Status legend
- `UNKNOWN` — not yet learned (business effect not yet recorded).
- `UNCONFIRMED` — logged, low trust (single Tier-2 or any Tier-3 source).
- `VERIFIED` — Microsoft states it directly, or two independent Tier-2 sources agree.

## Skeleton-confidence legend (per screen)
- `skeleton-complete` — Microsoft documents the form's controls well enough to trust the control list.
- `skeleton-partial` — Microsoft under-documents this form; control list is provisional and the denominator for this screen may grow.

---

## Level 1 — Module
**Production control** (Dynamics 365 Supply Chain Management)

## Level 2 — Menu groups (Microsoft navigation buckets)
1. **Setup** — *enumerated to Level 4 this session*
2. **Common / Daily** (Production orders, Batch orders, Kanban) — Level 3 provisional, Level 4 deferred
3. **Journals** — Level 3 provisional, Level 4 deferred
4. **Inquiries and reports** — Level 3 provisional, Level 4 deferred
5. **Periodic tasks** — Level 3 provisional, Level 4 deferred

> Note: "Production control parameters" is a Setup form, not a separate Level-2 bucket; placed under Setup below.

---

# GROUP 1 — SETUP (Level 3 forms → Level 4 controls)

## 1.1 Production control parameters  — `skeleton-partial`
Form code: `PARAMS`. Path: Production control > Setup > Production control parameters.
> Tabs enumerated from Microsoft: General, Journals, Automatic update, Standard update, Status, Inventory dimensions, Unit of measure, Lean manufacturing. **Not yet enumerated:** Documents, Number sequences, full Status matrix → `skeleton-partial`.

### General tab
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMS-001 | Parameter usage (By company / By site) | UNKNOWN |
| PC-SETUP-PARAMS-002 | Profit setting | UNKNOWN |
| PC-SETUP-PARAMS-003 | Reservation (Manual / Estimation / Scheduling / Start) | UNKNOWN |
| PC-SETUP-PARAMS-004 | Ledger posting (Item and resource / Item and category / Production groups) | UNKNOWN |
| PC-SETUP-PARAMS-005 | Maximum job lead time | UNKNOWN |
| PC-SETUP-PARAMS-006 | Route network | UNKNOWN |
| PC-SETUP-PARAMS-007 | Mandatory date | UNKNOWN |
| PC-SETUP-PARAMS-008 | Block removal of approval | UNKNOWN |
| PC-SETUP-PARAMS-009 | Block editing | UNKNOWN |
| PC-SETUP-PARAMS-010 | Post picking list in ledger | UNKNOWN |
| PC-SETUP-PARAMS-011 | Post report as finished in ledger | UNKNOWN |
| PC-SETUP-PARAMS-012 | Post excl. transaction type | UNKNOWN |
| PC-SETUP-PARAMS-013 | Planned order (capacity reservation) | UNKNOWN |
| PC-SETUP-PARAMS-014 | Project (capacity reservation) | UNKNOWN |
| PC-SETUP-PARAMS-015 | Limited work center search | UNKNOWN |
| PC-SETUP-PARAMS-016 | Price calculation | UNKNOWN |
| PC-SETUP-PARAMS-017 | Delete capacity reservations | UNKNOWN |
| PC-SETUP-PARAMS-018 | Use estimated cost price | UNKNOWN |
| PC-SETUP-PARAMS-049 | Default measuring device (dispensing) | UNKNOWN |

### Journals tab
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMS-019 | Default journal — Picking list | UNKNOWN |
| PC-SETUP-PARAMS-020 | Default journal — Route card | UNKNOWN |
| PC-SETUP-PARAMS-021 | Default journal — Job card | UNKNOWN |
| PC-SETUP-PARAMS-022 | Default journal — Report as finished | UNKNOWN |
| PC-SETUP-PARAMS-050 | Default journal — Dispensing tickets | UNKNOWN |
| PC-SETUP-PARAMS-023 | Pick negative | UNKNOWN |
| PC-SETUP-PARAMS-024 | Physical reduction | UNKNOWN |
| PC-SETUP-PARAMS-025 | Inv. managed planned order qty | UNKNOWN |
| PC-SETUP-PARAMS-026 | Accept error | UNKNOWN |
| PC-SETUP-PARAMS-027 | Automatic BOM consumption (journals) | UNKNOWN |
| PC-SETUP-PARAMS-028 | Mandatory cost category for quantity | UNKNOWN |
| PC-SETUP-PARAMS-029 | Mandatory cost category for hours | UNKNOWN |
| PC-SETUP-PARAMS-030 | Automatic report as finished | UNKNOWN |
| PC-SETUP-PARAMS-031 | Update capacity plan | UNKNOWN |

### Automatic update tab
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMS-032 | Scheduling method (Operations scheduling / Job scheduling) | UNKNOWN |
| PC-SETUP-PARAMS-033 | Automatic BOM consumption (Flushing principle / Always / Never) | UNKNOWN |
| PC-SETUP-PARAMS-034 | Automatic route consumption | UNKNOWN |
| PC-SETUP-PARAMS-035 | Group by vendor | UNKNOWN |
| PC-SETUP-PARAMS-036 | Group by purchase agreement | UNKNOWN |
| PC-SETUP-PARAMS-037 | Find purchase agreements | UNKNOWN |

### Standard update tab
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMS-038 | Scrap method | UNKNOWN |
| PC-SETUP-PARAMS-039 | Scrap account | UNKNOWN |
| PC-SETUP-PARAMS-040 | Finite capacity | UNKNOWN |
| PC-SETUP-PARAMS-041 | Finite material | UNKNOWN |
| PC-SETUP-PARAMS-042 | Finite property | UNKNOWN |
| PC-SETUP-PARAMS-043 | Enable dispensing for production | UNKNOWN |
| PC-SETUP-PARAMS-044 | Allow over-dispensing with reverse pick | UNKNOWN |

### Status / Inventory dimensions / Unit of measure / Lean manufacturing tabs
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMS-045 | Status update matrix (per-status allowed-update checkboxes) | UNKNOWN |
| PC-SETUP-PARAMS-046 | Inventory dimensions display selection | UNKNOWN |
| PC-SETUP-PARAMS-047 | Lean time units (Days/Hours/Minutes/Seconds) | UNKNOWN |
| PC-SETUP-PARAMS-048 | Lean manufacturing default parameters | UNKNOWN |

## 1.2 Production control parameters by site  — `skeleton-partial`
Form code: `PARAMSITE`. Path: Production control > Setup > Production control parameters by site.
> Mirrors site-applicable subset of PARAMS (controls flagged "can also apply to sites"). Effective only when PARAMS Parameter usage = By site.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMSITE-001 | Site selector | UNKNOWN |
| PC-SETUP-PARAMSITE-002 | Maximum job lead time (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-003 | Post picking list in ledger (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-004 | Post report as finished in ledger (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-005 | Post excl. transaction type (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-006 | Planned order (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-007 | Project (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-008 | Limited work center search (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-009 | Price calculation (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-010 | Delete capacity reservations (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-011 | Use estimated cost price (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-012 | Default journal — Picking list (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-013 | Default journal — Route card (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-014 | Default journal — Job card (site) | UNKNOWN |
| PC-SETUP-PARAMSITE-015 | Default journal — Report as finished (site) | UNKNOWN |

## 1.3 Production journal names  — `skeleton-partial`
Form code: `JOURNALNAMES`. Path: Production control > Setup > Production journal names.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-JOURNALNAMES-001 | Journal name (Name) | UNKNOWN |
| PC-SETUP-JOURNALNAMES-002 | Description | UNKNOWN |
| PC-SETUP-JOURNALNAMES-003 | Journal type | UNKNOWN |
| PC-SETUP-JOURNALNAMES-004 | Default private user group | UNKNOWN |
| PC-SETUP-JOURNALNAMES-005 | Delete lines after posting | UNKNOWN |
| PC-SETUP-JOURNALNAMES-006 | Default posting summation level | UNKNOWN |
| PC-SETUP-JOURNALNAMES-007 | Voucher number allocation rule | UNKNOWN |
| PC-SETUP-JOURNALNAMES-008 | Voucher number selection rule | UNKNOWN |
| PC-SETUP-JOURNALNAMES-009 | Voucher series / number sequence code | UNKNOWN |
| PC-SETUP-JOURNALNAMES-010 | Dispensing tickets (toggle) | UNKNOWN |

## 1.4 Production pools  — `skeleton-partial`
Form code: `POOLS`. Path: Production control > Setup > Production pools.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-POOLS-001 | Production pool (id) | UNKNOWN |
| PC-SETUP-POOLS-002 | Name / Description | UNKNOWN |

## 1.5 Production groups  — `skeleton-partial`
Form code: `GROUPS`. Path: Production control > Setup > Production groups.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-GROUPS-001 | Production group (id) | UNKNOWN |
| PC-SETUP-GROUPS-002 | Name / Description | UNKNOWN |
| PC-SETUP-GROUPS-003 | Ledger - items / ledger posting accounts | UNKNOWN |

## 1.6 Production units  — `skeleton-partial`
Form code: `UNITS`. Path: Production control > Setup > Production units.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-UNITS-001 | Production unit (id) | UNKNOWN |
| PC-SETUP-UNITS-002 | Name | UNKNOWN |
| PC-SETUP-UNITS-003 | Site | UNKNOWN |
| PC-SETUP-UNITS-004 | Resource group / warehouse association | UNKNOWN |

## 1.7 Allocation keys  — `skeleton-partial`
Form code: `ALLOCKEYS`. Path: Production control > Setup > Allocation keys.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-ALLOCKEYS-001 | Allocation key (id) | UNKNOWN |
| PC-SETUP-ALLOCKEYS-002 | Description | UNKNOWN |
| PC-SETUP-ALLOCKEYS-003 | Period allocation lines | UNKNOWN |

## 1.8 Properties  — `skeleton-partial`
Form code: `PROPS`. Path: Production control > Setup > Properties.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PROPS-001 | Property (id) | UNKNOWN |
| PC-SETUP-PROPS-002 | Description | UNKNOWN |

## 1.9 Tracked components policy  — `skeleton-partial`
Form code: `TRACKEDCOMP`. Path: Production control > Setup > Production > Tracked components policy.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-TRACKEDCOMP-001 | Policy name | UNKNOWN |
| PC-SETUP-TRACKEDCOMP-002 | Use tracked components (toggle) | UNKNOWN |

## 1.10 Manufacturing execution — Production order defaults  — `skeleton-partial`
Form code: `MES-DEFAULTS`. Path: Production control > Setup > Manufacturing execution > Production order defaults.
> Tabs: General, Start, Operations, Report as finished, Quantity validation.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-MES-DEFAULTS-001 | Skip time adjustments (General) | UNKNOWN |
| PC-SETUP-MES-DEFAULTS-002 | General job parameter settings (group) | UNKNOWN |
| PC-SETUP-MES-DEFAULTS-003 | Start parameters (Start tab) | UNKNOWN |
| PC-SETUP-MES-DEFAULTS-004 | Job types requiring registration (Operations tab) | UNKNOWN |
| PC-SETUP-MES-DEFAULTS-005 | Report as finished parameters | UNKNOWN |
| PC-SETUP-MES-DEFAULTS-006 | Quantity validation parameters | UNKNOWN |

## 1.11 Manufacturing execution — Configure production floor execution  — `skeleton-partial`
Form code: `MES-PFE`. Path: Production control > Setup > Manufacturing execution > Configure production floor execution.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-MES-PFE-001 | Clock in and out only | UNKNOWN |
| PC-SETUP-MES-PFE-002 | Report quantity at clock-out | UNKNOWN |
| PC-SETUP-MES-PFE-003 | Lock employee | UNKNOWN |
| PC-SETUP-MES-PFE-004 | Use the actual time of registration | UNKNOWN |
| PC-SETUP-MES-PFE-005 | Single worker | UNKNOWN |
| PC-SETUP-MES-PFE-006 | Tab selection (interface design) | UNKNOWN |

## 1.12 Routes — Operations  — `skeleton-partial`
Form code: `ROUTES-OPS`. Path: Production control > Setup > Routes > Operations.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-ROUTES-OPS-001 | Operation (id) | UNKNOWN |
| PC-SETUP-ROUTES-OPS-002 | Name | UNKNOWN |
| PC-SETUP-ROUTES-OPS-003 | Relations (operation relations) | UNKNOWN |

## 1.13 Routes — Route groups  — `skeleton-partial`
Form code: `ROUTES-RG`. Path: Production control > Setup > Routes > Route groups.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-ROUTES-RG-001 | Route group (id) | UNKNOWN |
| PC-SETUP-ROUTES-RG-002 | Name | UNKNOWN |
| PC-SETUP-ROUTES-RG-003 | Setup time (Estimation and costing) | UNKNOWN |
| PC-SETUP-ROUTES-RG-004 | Run time (Estimation and costing) | UNKNOWN |
| PC-SETUP-ROUTES-RG-005 | Quantity (Estimation and costing) | UNKNOWN |
| PC-SETUP-ROUTES-RG-006 | Job management (per job type) | UNKNOWN |
| PC-SETUP-ROUTES-RG-007 | Automatic route consumption settings | UNKNOWN |

## 1.14 Cost categories  — `skeleton-partial`
Form code: `COSTCAT`. Path: Production control > Setup > Routes > Cost categories.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-COSTCAT-001 | Cost category (id) | UNKNOWN |
| PC-SETUP-COSTCAT-002 | Cost group | UNKNOWN |
| PC-SETUP-COSTCAT-003 | Cost price (per hour) | UNKNOWN |
| PC-SETUP-COSTCAT-004 | Category type (Setup / Run / Quantity) | UNKNOWN |

## 1.15 Cost groups  — `skeleton-partial`
Form code: `COSTGRP`. Path: Production control > Setup > Routes > Cost groups (shared with Cost management).
| ID | Control | Status |
|---|---|---|
| PC-SETUP-COSTGRP-001 | Cost group (id) | UNKNOWN |
| PC-SETUP-COSTGRP-002 | Cost group type | UNKNOWN |
| PC-SETUP-COSTGRP-003 | Profit setting association | UNKNOWN |

## 1.16 Routes — Routes / Route version  — `skeleton-partial`
Form code: `ROUTES-ROUTE`. Path: Production control > Setup > Routes > Routes (and Route versions).
| ID | Control | Status |
|---|---|---|
| PC-SETUP-ROUTES-ROUTE-001 | Route number | UNKNOWN |
| PC-SETUP-ROUTES-ROUTE-002 | Route version | UNKNOWN |
| PC-SETUP-ROUTES-ROUTE-003 | Approve / Activate | UNKNOWN |

**Setup group control count: 123** (see COVERAGE_STATE.md for the authoritative tally).

---

# GROUP 2 — COMMON / DAILY  (Level 3 provisional — `skeleton-partial`, Level 4 deferred)
| Form | Status |
|---|---|
| Production orders (All production orders) | Level 4 deferred |
| Batch orders (All batch orders) | Level 4 deferred |
| Kanban board for process jobs | Level 4 deferred |
| Kanban board for transfer jobs | Level 4 deferred |
| Kanban quantity calculations | Level 4 deferred |
| Production floor execution (interface) | Level 4 deferred |

# GROUP 3 — JOURNALS  (Level 3 provisional — `skeleton-partial`, Level 4 deferred)
| Form | Status |
|---|---|
| Picking list | Level 4 deferred |
| Route card | Level 4 deferred |
| Job card | Level 4 deferred |
| Report as finished | Level 4 deferred |

# GROUP 4 — INQUIRIES AND REPORTS  (Level 3 provisional — `skeleton-partial`, Level 4 deferred)
| Form | Status |
|---|---|
| Production order inquiries/reports (BOM, route, jobs, etc.) | Level 4 deferred |

# GROUP 5 — PERIODIC TASKS  (Level 3 provisional — `skeleton-partial`, Level 4 deferred)
| Form | Status |
|---|---|
| Update (schedule / release / start / report as finished / end) | Level 4 deferred |
| Clean up | Level 4 deferred |

---

## Provenance & caveats
- All Setup control names sourced from Microsoft Learn / Microsoft Docs (Tier 1) — see SOURCES.md.
- Forms marked `skeleton-partial`: Microsoft does not exhaustively list every field; control lists are provisional and may grow during enrichment (Mission 2). New controls discovered are added here and logged in CHANGELOG.md.
- Non-Setup groups (2–5): Level-3 form lists are **provisional** and must be reconciled against the live Production control navigation before their Level-4 enumeration begins.
