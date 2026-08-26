# KNOWLEDGE_MAP.md — D365 F&O Production Control Knowledge Map (Skeleton)

> **Version lock:** Dynamics 365 Supply Chain Management **10.0.47** (build **10.0.2527**) — GA self-update March 2026 (latest GA as of 2026-05-31). 10.0.48 (build 10.0.2645) is not GA until June 2026.
> **Map version:** v0.4
> **Last updated:** 2026-05-31
> **Mission 2 progress:** Setup forms PARAMS (49/50), PARAMSITE (15/15), JOURNALNAMES (4/10), ROUTES-RG (7/7), MES-DEFAULTS (8/8), MES-PFE (24/24) enriched. Denominator grew to 210 (MES-DEFAULTS +2, MES-PFE +18). Verified-knowledge = 107/210 = 51.0%.
> **Purpose:** This map is the *denominator* for all coverage maths. Levels 1–4 below. Every Level-4 control has a unique ID and a status. **All five groups are now enumerated to Level 4** (Setup `skeleton-partial`; Groups 2–5 operational/inquiry forms are `skeleton-partial` and partial by nature — Microsoft does not list every Action Pane button). Skeleton completeness is tracked in COVERAGE_STATE.md and is distinct from the verified-knowledge % (a Mission 2 measure, currently 51.0%).

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
1. **Setup** — Level 4 (16 forms, `skeleton-partial`)
2. **Common / Daily** (Production orders, Batch orders, Kanban) — Level 4 (`skeleton-partial`)
3. **Journals** — Level 4 (`skeleton-partial`)
4. **Inquiries and reports** — Level 4 provisional (`skeleton-partial`)
5. **Periodic tasks** — Level 4 (`skeleton-partial`)

> Note: "Production control parameters" is a Setup form, not a separate Level-2 bucket; placed under Setup below.

---

# GROUP 1 — SETUP (Level 3 forms → Level 4 controls)

## 1.1 Production control parameters  — `skeleton-partial`
Form code: `PARAMS`. Path: Production control > Setup > Production control parameters.
> Tabs enumerated from Microsoft: General, Journals, Automatic update, Standard update, Status, Inventory dimensions, Unit of measure, Lean manufacturing. **Not yet enumerated:** Documents, Number sequences, full Status matrix → `skeleton-partial`.

### General tab
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMS-001 | Parameter usage (By company / By site) | VERIFIED |
| PC-SETUP-PARAMS-002 | Profit setting | VERIFIED |
| PC-SETUP-PARAMS-003 | Reservation (Manual / Estimation / Scheduling / Start) | VERIFIED |
| PC-SETUP-PARAMS-004 | Ledger posting (Item and resource / Item and category / Production groups) | VERIFIED |
| PC-SETUP-PARAMS-005 | Maximum job lead time | VERIFIED |
| PC-SETUP-PARAMS-006 | Route network | VERIFIED |
| PC-SETUP-PARAMS-007 | Mandatory date | VERIFIED |
| PC-SETUP-PARAMS-008 | Block removal of approval | VERIFIED |
| PC-SETUP-PARAMS-009 | Block editing | VERIFIED |
| PC-SETUP-PARAMS-010 | Post picking list in ledger | VERIFIED |
| PC-SETUP-PARAMS-011 | Post report as finished in ledger | VERIFIED |
| PC-SETUP-PARAMS-012 | Post excl. transaction type | VERIFIED |
| PC-SETUP-PARAMS-013 | Planned order (capacity reservation) | VERIFIED |
| PC-SETUP-PARAMS-014 | Project (capacity reservation) | VERIFIED |
| PC-SETUP-PARAMS-015 | Limited work center search | VERIFIED |
| PC-SETUP-PARAMS-016 | Price calculation | VERIFIED |
| PC-SETUP-PARAMS-017 | Delete capacity reservations | VERIFIED |
| PC-SETUP-PARAMS-018 | Use estimated cost price | VERIFIED |
| PC-SETUP-PARAMS-049 | Default measuring device (dispensing) | VERIFIED |

### Journals tab
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMS-019 | Default journal — Picking list | VERIFIED |
| PC-SETUP-PARAMS-020 | Default journal — Route card | VERIFIED |
| PC-SETUP-PARAMS-021 | Default journal — Job card | VERIFIED |
| PC-SETUP-PARAMS-022 | Default journal — Report as finished | VERIFIED |
| PC-SETUP-PARAMS-050 | Default journal — Dispensing tickets | VERIFIED |
| PC-SETUP-PARAMS-023 | Pick negative | VERIFIED |
| PC-SETUP-PARAMS-024 | Physical reduction | VERIFIED |
| PC-SETUP-PARAMS-025 | Inv. managed planned order qty | VERIFIED |
| PC-SETUP-PARAMS-026 | Accept error | VERIFIED |
| PC-SETUP-PARAMS-027 | Automatic BOM consumption (journals) | VERIFIED |
| PC-SETUP-PARAMS-028 | Mandatory cost category for quantity | VERIFIED |
| PC-SETUP-PARAMS-029 | Mandatory cost category for hours | VERIFIED |
| PC-SETUP-PARAMS-030 | Automatic report as finished | VERIFIED |
| PC-SETUP-PARAMS-031 | Update capacity plan | VERIFIED |

### Automatic update tab
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMS-032 | Scheduling method (Operations scheduling / Job scheduling) | VERIFIED |
| PC-SETUP-PARAMS-033 | Automatic BOM consumption (Flushing principle / Always / Never) | VERIFIED |
| PC-SETUP-PARAMS-034 | Automatic route consumption | VERIFIED |
| PC-SETUP-PARAMS-035 | Group by vendor | VERIFIED |
| PC-SETUP-PARAMS-036 | Group by purchase agreement | VERIFIED |
| PC-SETUP-PARAMS-037 | Find purchase agreements | VERIFIED |

### Standard update tab
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMS-038 | Scrap method | VERIFIED |
| PC-SETUP-PARAMS-039 | Scrap account | VERIFIED |
| PC-SETUP-PARAMS-040 | Finite capacity | VERIFIED |
| PC-SETUP-PARAMS-041 | Finite material | VERIFIED |
| PC-SETUP-PARAMS-042 | Finite property | VERIFIED |
| PC-SETUP-PARAMS-043 | Enable dispensing for production | VERIFIED |
| PC-SETUP-PARAMS-044 | Allow over-dispensing with reverse pick | VERIFIED |

### Status / Inventory dimensions / Unit of measure / Lean manufacturing tabs
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMS-045 | Status update matrix (per-status allowed-update checkboxes) | VERIFIED |
| PC-SETUP-PARAMS-046 | Inventory dimensions display selection | VERIFIED |
| PC-SETUP-PARAMS-047 | Lean time units (Days/Hours/Minutes/Seconds) | VERIFIED |
| PC-SETUP-PARAMS-048 | Lean manufacturing default parameters | UNKNOWN |

## 1.2 Production control parameters by site  — `skeleton-partial`
Form code: `PARAMSITE`. Path: Production control > Setup > Production control parameters by site.
> Mirrors site-applicable subset of PARAMS (controls flagged "can also apply to sites"). Effective only when PARAMS Parameter usage = By site.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-PARAMSITE-001 | Site selector | VERIFIED |
| PC-SETUP-PARAMSITE-002 | Maximum job lead time (site) | VERIFIED |
| PC-SETUP-PARAMSITE-003 | Post picking list in ledger (site) | VERIFIED |
| PC-SETUP-PARAMSITE-004 | Post report as finished in ledger (site) | VERIFIED |
| PC-SETUP-PARAMSITE-005 | Post excl. transaction type (site) | VERIFIED |
| PC-SETUP-PARAMSITE-006 | Planned order (site) | VERIFIED |
| PC-SETUP-PARAMSITE-007 | Project (site) | VERIFIED |
| PC-SETUP-PARAMSITE-008 | Limited work center search (site) | VERIFIED |
| PC-SETUP-PARAMSITE-009 | Price calculation (site) | VERIFIED |
| PC-SETUP-PARAMSITE-010 | Delete capacity reservations (site) | VERIFIED |
| PC-SETUP-PARAMSITE-011 | Use estimated cost price (site) | VERIFIED |
| PC-SETUP-PARAMSITE-012 | Default journal — Picking list (site) | VERIFIED |
| PC-SETUP-PARAMSITE-013 | Default journal — Route card (site) | VERIFIED |
| PC-SETUP-PARAMSITE-014 | Default journal — Job card (site) | VERIFIED |
| PC-SETUP-PARAMSITE-015 | Default journal — Report as finished (site) | VERIFIED |

## 1.3 Production journal names  — `skeleton-partial`
Form code: `JOURNALNAMES`. Path: Production control > Setup > Production journal names.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-JOURNALNAMES-001 | Journal name (Name) | VERIFIED |
| PC-SETUP-JOURNALNAMES-002 | Description | VERIFIED |
| PC-SETUP-JOURNALNAMES-003 | Journal type | VERIFIED |
| PC-SETUP-JOURNALNAMES-004 | Default private user group | UNKNOWN |
| PC-SETUP-JOURNALNAMES-005 | Delete lines after posting | UNKNOWN |
| PC-SETUP-JOURNALNAMES-006 | Default posting summation level | UNKNOWN |
| PC-SETUP-JOURNALNAMES-007 | Voucher number allocation rule | UNKNOWN |
| PC-SETUP-JOURNALNAMES-008 | Voucher number selection rule | UNKNOWN |
| PC-SETUP-JOURNALNAMES-009 | Voucher series / number sequence code | UNKNOWN |
| PC-SETUP-JOURNALNAMES-010 | Dispensing tickets (toggle) | VERIFIED |

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
> Tabs: General, Start, Operations, Report as finished, Quantity validation. Refined to documented fields (v0.4).
| ID | Control | Status |
|---|---|---|
| PC-SETUP-MES-DEFAULTS-001 | Skip time adjustments (General) | VERIFIED |
| PC-SETUP-MES-DEFAULTS-002 | Update start on-line (Start) | VERIFIED |
| PC-SETUP-MES-DEFAULTS-003 | Automatic BOM consumption — Start | VERIFIED |
| PC-SETUP-MES-DEFAULTS-004 | Job types requiring registration (Operations) | VERIFIED |
| PC-SETUP-MES-DEFAULTS-005 | Automatic BOM consumption — Operations | VERIFIED |
| PC-SETUP-MES-DEFAULTS-006 | Update finished report on-line (Report as finished) | VERIFIED |
| PC-SETUP-MES-DEFAULTS-007 | Automatic BOM consumption — Report as finished | VERIFIED |
| PC-SETUP-MES-DEFAULTS-008 | Quantity validation parameters | VERIFIED |

## 1.11 Manufacturing execution — Configure production floor execution  — `skeleton-partial`
Form code: `MES-PFE`. Path: Production control > Setup > Manufacturing execution > Configure production floor execution.
> Expanded v0.4 from 6 → 24 controls (5 FastTabs + 1 action) after enrichment surfaced the full documented control set.
| ID | Control | Status |
|---|---|---|
| PC-SETUP-MES-PFE-001 | Clock in and out only (General) | VERIFIED |
| PC-SETUP-MES-PFE-002 | Report quantity at clock-out (General) | VERIFIED |
| PC-SETUP-MES-PFE-003 | Lock employee (General) | VERIFIED |
| PC-SETUP-MES-PFE-004 | Use the actual time of registration (General) | VERIFIED |
| PC-SETUP-MES-PFE-005 | Single worker (General) | VERIFIED |
| PC-SETUP-MES-PFE-007 | Suppress numpad keyboard (General) | VERIFIED |
| PC-SETUP-MES-PFE-006 | Tab selection | VERIFIED |
| PC-SETUP-MES-PFE-008 | Enable numpad (Login) | VERIFIED |
| PC-SETUP-MES-PFE-009 | Allow locking the touchscreen (Login) | VERIFIED |
| PC-SETUP-MES-PFE-010 | Screen lock duration (Login) | VERIFIED |
| PC-SETUP-MES-PFE-011 | Enable search (Main view) | VERIFIED |
| PC-SETUP-MES-PFE-012 | Enable search by project ID (Main view) | VERIFIED |
| PC-SETUP-MES-PFE-013 | Auto-open start dialog (Main view) | VERIFIED |
| PC-SETUP-MES-PFE-014 | Auto-open report progress dialog (Main view) | VERIFIED |
| PC-SETUP-MES-PFE-015 | Skip product selection (Report progress) | VERIFIED |
| PC-SETUP-MES-PFE-016 | View materials (Report progress) | VERIFIED |
| PC-SETUP-MES-PFE-017 | Enable adjust material (Report progress) | VERIFIED |
| PC-SETUP-MES-PFE-018 | Default remaining quantity (Report progress) | VERIFIED |
| PC-SETUP-MES-PFE-019 | Default nominal quantity (Report progress) | VERIFIED |
| PC-SETUP-MES-PFE-020 | Require existing license plate (Report progress) | VERIFIED |
| PC-SETUP-MES-PFE-021 | Generate license plate (Report progress) | VERIFIED |
| PC-SETUP-MES-PFE-022 | Print label (Report progress) | VERIFIED |
| PC-SETUP-MES-PFE-023 | Add material line (Report progress) | VERIFIED |
| PC-SETUP-MES-PFE-024 | Clean up client configurations (action) | VERIFIED |

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
| PC-SETUP-ROUTES-RG-001 | Route group (id) | VERIFIED |
| PC-SETUP-ROUTES-RG-002 | Name | VERIFIED |
| PC-SETUP-ROUTES-RG-003 | Setup time (Estimation and costing) | VERIFIED |
| PC-SETUP-ROUTES-RG-004 | Run time (Estimation and costing) | VERIFIED |
| PC-SETUP-ROUTES-RG-005 | Quantity (Estimation and costing) | VERIFIED |
| PC-SETUP-ROUTES-RG-006 | Job management (per job type) | VERIFIED |
| PC-SETUP-ROUTES-RG-007 | Complete secondary operation with primary | VERIFIED |

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

**Setup group control count: 143** (see COVERAGE_STATE.md for the authoritative tally). *(v0.4: MES-DEFAULTS 6→8, MES-PFE 6→24.)*

---

# GROUP 2 — COMMON / DAILY (Level 4 — all forms `skeleton-partial`)
> Operational forms; Microsoft documents the main Action Pane operations but not every button. Control lists are partial.

## 2.1 All production orders (`PORD`) — Production control > Production orders > All production orders
| ID | Control | Status |
|---|---|---|
| PC-COMMON-PORD-001 | New production order | UNKNOWN |
| PC-COMMON-PORD-002 | Estimate | UNKNOWN |
| PC-COMMON-PORD-003 | Schedule — Operations scheduling | UNKNOWN |
| PC-COMMON-PORD-004 | Schedule — Job scheduling | UNKNOWN |
| PC-COMMON-PORD-005 | Release (+ print Job card / Route job / Route card) | UNKNOWN |
| PC-COMMON-PORD-006 | Start (From oper. no., Auto route/BOM consumption, Post now, Print picking list) | UNKNOWN |
| PC-COMMON-PORD-007 | Report as finished (Good qty, Error qty, Error cause, End job, Accept error) | UNKNOWN |
| PC-COMMON-PORD-008 | End (Date, Scrap method) | UNKNOWN |
| PC-COMMON-PORD-009 | View > Picking list | UNKNOWN |
| PC-COMMON-PORD-010 | View > Reported as finished | UNKNOWN |
| PC-COMMON-PORD-011 | Manage costs > View cost comparison | UNKNOWN |

## 2.2 All batch orders (`BORD`) — Production control > Batch orders > All batch orders
| ID | Control | Status |
|---|---|---|
| PC-COMMON-BORD-001 | New batch order | UNKNOWN |
| PC-COMMON-BORD-002 | Estimate | UNKNOWN |
| PC-COMMON-BORD-003 | Schedule | UNKNOWN |
| PC-COMMON-BORD-004 | Release | UNKNOWN |
| PC-COMMON-BORD-005 | Start | UNKNOWN |
| PC-COMMON-BORD-006 | Report as finished / End | UNKNOWN |

## 2.3 Kanban board for process jobs (`KPROC`) — Production control > Kanban > Kanban board for process jobs
| ID | Control | Status |
|---|---|---|
| PC-COMMON-KPROC-001 | Prioritize | UNKNOWN |
| PC-COMMON-KPROC-002 | Pick | UNKNOWN |
| PC-COMMON-KPROC-003 | Manufacture (report) | UNKNOWN |
| PC-COMMON-KPROC-004 | Bar code scanning | UNKNOWN |

## 2.4 Kanban board for transfer jobs (`KTRANS`) — Production control > Kanban > Kanban board for transfer jobs
| ID | Control | Status |
|---|---|---|
| PC-COMMON-KTRANS-001 | Filters (Production flow / Activity / From-To warehouse-location) | UNKNOWN |
| PC-COMMON-KTRANS-002 | Start | UNKNOWN |
| PC-COMMON-KTRANS-003 | Complete | UNKNOWN |
| PC-COMMON-KTRANS-004 | Job quantity (capped to kanban rule) | UNKNOWN |

## 2.5 Kanban schedule board / Kanban job scheduling (`KSCHED`) — Production control > Kanban
| ID | Control | Status |
|---|---|---|
| PC-COMMON-KSCHED-001 | Schedule unplanned job | UNKNOWN |
| PC-COMMON-KSCHED-002 | Reschedule job to period | UNKNOWN |
| PC-COMMON-KSCHED-003 | Change job status | UNKNOWN |

## 2.6 Production floor execution interface — runtime (`PFE-RUN`)
| ID | Control | Status |
|---|---|---|
| PC-COMMON-PFE-RUN-001 | Clock in / clock out | UNKNOWN |
| PC-COMMON-PFE-RUN-002 | Start / stop job (job bundling) | UNKNOWN |
| PC-COMMON-PFE-RUN-003 | Report feedback / report as finished | UNKNOWN |

# GROUP 3 — JOURNALS (Level 4 — all forms `skeleton-partial`)
## 3.1 Picking list (`J-PICK`)
| ID | Control | Status |
|---|---|---|
| PC-JOURNALS-J-PICK-001 | Lines (item consumption) | UNKNOWN |
| PC-JOURNALS-J-PICK-002 | Consumption quantity | UNKNOWN |
| PC-JOURNALS-J-PICK-003 | Proposal (BOM) | UNKNOWN |
| PC-JOURNALS-J-PICK-004 | Post | UNKNOWN |

## 3.2 Route card (`J-ROUTE`)
| ID | Control | Status |
|---|---|---|
| PC-JOURNALS-J-ROUTE-001 | Lines (operations) | UNKNOWN |
| PC-JOURNALS-J-ROUTE-002 | Hours / Good qty / Error qty | UNKNOWN |
| PC-JOURNALS-J-ROUTE-003 | Proposal | UNKNOWN |
| PC-JOURNALS-J-ROUTE-004 | Post | UNKNOWN |

## 3.3 Job card (`J-JOB`)
| ID | Control | Status |
|---|---|---|
| PC-JOURNALS-J-JOB-001 | Lines (jobs) | UNKNOWN |
| PC-JOURNALS-J-JOB-002 | Hours / Good qty / Error qty | UNKNOWN |
| PC-JOURNALS-J-JOB-003 | Proposal | UNKNOWN |
| PC-JOURNALS-J-JOB-004 | Post | UNKNOWN |

## 3.4 Report as finished (`J-RAF`)
| ID | Control | Status |
|---|---|---|
| PC-JOURNALS-J-RAF-001 | Lines (finished qty) | UNKNOWN |
| PC-JOURNALS-J-RAF-002 | Good qty / Error qty / Error cause | UNKNOWN |
| PC-JOURNALS-J-RAF-003 | End job | UNKNOWN |
| PC-JOURNALS-J-RAF-004 | Post | UNKNOWN |

# GROUP 4 — INQUIRIES AND REPORTS (Level 4 provisional — `skeleton-partial`)
> Microsoft under-documents the SCM Production control report catalogue; this Level-4 list is provisional and will grow.
| ID | Control | Status |
|---|---|---|
| PC-INQUIRY-RPT-001 | Production order list report (filters: period / location / status) | UNKNOWN |
| PC-INQUIRY-RPT-002 | Price calculation inquiry | UNKNOWN |
| PC-INQUIRY-RPT-003 | Cost comparison inquiry | UNKNOWN |
| PC-INQUIRY-RPT-004 | Production journals inquiry | UNKNOWN |

# GROUP 5 — PERIODIC TASKS (Level 4 — all forms `skeleton-partial`)
## 5.1 Kanban quantity calculation (`KANBANCALC`) — Periodic tasks > Kanban quantity calculation > Calculate kanban quantity
| ID | Control | Status |
|---|---|---|
| PC-PERIODIC-KANBANCALC-001 | Name / Policy | UNKNOWN |
| PC-PERIODIC-KANBANCALC-002 | Rule active as of date | UNKNOWN |
| PC-PERIODIC-KANBANCALC-003 | Fulfilled demand period (start/end) | UNKNOWN |
| PC-PERIODIC-KANBANCALC-004 | Demand period (start/end) | UNKNOWN |
| PC-PERIODIC-KANBANCALC-005 | Generate / Calculate / Update | UNKNOWN |

## 5.2 Kanban rules (`KANBANRULES`) — reachable via Periodic tasks > Kanban quantity calculation > Kanban rules (primary home: PIM > Lean manufacturing)
| ID | Control | Status |
|---|---|---|
| PC-PERIODIC-KANBANRULES-001 | Type (Manufacturing / Withdrawal) | UNKNOWN |
| PC-PERIODIC-KANBANRULES-002 | Replenishment strategy (Fixed / Scheduled / Event) | UNKNOWN |
| PC-PERIODIC-KANBANRULES-003 | Automatic planning quantity | UNKNOWN |

## 5.3 Update — batch lifecycle (`UPDATE`)
| ID | Control | Status |
|---|---|---|
| PC-PERIODIC-UPDATE-001 | Estimate (batch) | UNKNOWN |
| PC-PERIODIC-UPDATE-002 | Schedule (batch) | UNKNOWN |
| PC-PERIODIC-UPDATE-003 | Release (batch) | UNKNOWN |
| PC-PERIODIC-UPDATE-004 | Start (batch) | UNKNOWN |
| PC-PERIODIC-UPDATE-005 | Report as finished / End (batch) | UNKNOWN |

## 5.4 Clean up (`CLEANUP`)
| ID | Control | Status |
|---|---|---|
| PC-PERIODIC-CLEANUP-001 | Production journals cleanup | UNKNOWN |
| PC-PERIODIC-CLEANUP-002 | Production orders cleanup / archive | UNKNOWN |
| PC-PERIODIC-CLEANUP-003 | Calculation cleanup | UNKNOWN |

---

## Provenance & caveats
- All Setup control names sourced from Microsoft Learn / Microsoft Docs (Tier 1) — see SOURCES.md.
- Forms marked `skeleton-partial`: Microsoft does not exhaustively list every field; control lists are provisional and may grow during enrichment (Mission 2). New controls discovered are added here and logged in CHANGELOG.md.
- Non-Setup groups (2–5): Level-3 form lists are **provisional** and must be reconciled against the live Production control navigation before their Level-4 enumeration begins.
