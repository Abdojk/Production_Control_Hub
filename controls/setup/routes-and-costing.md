# Learning records — Routes & costing setup (`ROUTES-OPS`, `ROUTES-RG`, `COSTCAT`, `COSTGRP`, `ROUTES-ROUTE`)

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Screen skeleton confidence:** `skeleton-partial`
> **Enrichment status:** PARTIAL — ROUTES-RG 7/7 VERIFIED; ROUTES-OPS, COSTCAT, COSTGRP, ROUTES-ROUTE still UNKNOWN.
> **Scope note:** Routes/cost categories/cost groups are shared with Routes and Cost management. Recorded here only for their Production-control setup role.

## Operations (`ROUTES-OPS`) — Setup > Routes > Operations
- PC-SETUP-ROUTES-OPS-001 Operation (id)
- PC-SETUP-ROUTES-OPS-002 Name
- PC-SETUP-ROUTES-OPS-003 Relations (operation relations)

## Route groups (`ROUTES-RG`) — Setup > Routes > Route groups
> **Enriched 2026-05-31 — 7/7 VERIFIED.** Sources: Tier 1 — Production postings (#3), Registration for manufacturing execution (#7), Configure production floor execution (#8).
- **PC-SETUP-ROUTES-RG-001 Route group (id)** — Identifier assigned to each route operation line; drives which costing/registration rules apply to that operation. — **VERIFIED** (#3)
- **PC-SETUP-ROUTES-RG-002 Name** — Descriptive name. — **VERIFIED** (#3)
- **PC-SETUP-ROUTES-RG-003 Setup time (Estimation and costing)** — Enabled: setup time is used for costing and creates a GL voucher when posting Route/Job card. Disabled: no voucher for setup time. — **VERIFIED** (#3)
- **PC-SETUP-ROUTES-RG-004 Run time (Estimation and costing)** — *Yes*: at job start, generate a route card journal with the **estimated** operation time. *No*: at job stop/complete, generate a job card journal with the worker's **actual** time. Also gates whether run time creates a GL voucher. — **VERIFIED** (#3, #7)
- **PC-SETUP-ROUTES-RG-005 Quantity (Estimation and costing)** — Enabled: quantity-based time is used for costing and creates a GL voucher. Disabled: no voucher for quantity time. — **VERIFIED** (#3)
- **PC-SETUP-ROUTES-RG-006 Job management (per job type)** — Per job type: if selected, that job type is reported as finished on the order when its job is reported finished; when all Job-management job types on an operation are finished, the operation is reported finished. Must match MES-DEFAULTS registration job types. — **VERIFIED** (#6)
- **PC-SETUP-ROUTES-RG-007 Complete secondary operation with primary** — When enabled on the route group of a secondary operation, that secondary operation auto-completes when its primary operation is completed in the production floor execution interface, recording matching time (10.0.46+ feature). *(Re-scoped from the earlier unsourced "Automatic route consumption settings" stub.)* — **VERIFIED** (#8)

## Cost categories (`COSTCAT`) — Setup > Routes > Cost categories
- PC-SETUP-COSTCAT-001 Cost category (id)
- PC-SETUP-COSTCAT-002 Cost group
- PC-SETUP-COSTCAT-003 Cost price (per hour)
- PC-SETUP-COSTCAT-004 Category type (Setup / Run / Quantity)

## Cost groups (`COSTGRP`) — Setup > Routes > Cost groups
- PC-SETUP-COSTGRP-001 Cost group (id)
- PC-SETUP-COSTGRP-002 Cost group type
- PC-SETUP-COSTGRP-003 Profit setting association

## Routes / Route version (`ROUTES-ROUTE`) — Setup > Routes > Routes
- PC-SETUP-ROUTES-ROUTE-001 Route number
- PC-SETUP-ROUTES-ROUTE-002 Route version
- PC-SETUP-ROUTES-ROUTE-003 Approve / Activate
