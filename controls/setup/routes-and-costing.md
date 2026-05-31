# Learning records — Routes & costing setup (`ROUTES-OPS`, `ROUTES-RG`, `COSTCAT`, `COSTGRP`, `ROUTES-ROUTE`)

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Screen skeleton confidence:** `skeleton-partial`
> **Enrichment status:** NOT STARTED — all controls UNKNOWN.
> **Scope note:** Routes/cost categories/cost groups are shared with Routes and Cost management. Recorded here only for their Production-control setup role.

## Operations (`ROUTES-OPS`) — Setup > Routes > Operations
- PC-SETUP-ROUTES-OPS-001 Operation (id)
- PC-SETUP-ROUTES-OPS-002 Name
- PC-SETUP-ROUTES-OPS-003 Relations (operation relations)

## Route groups (`ROUTES-RG`) — Setup > Routes > Route groups
- PC-SETUP-ROUTES-RG-001 Route group (id)
- PC-SETUP-ROUTES-RG-002 Name
- PC-SETUP-ROUTES-RG-003 Setup time (Estimation and costing)
- PC-SETUP-ROUTES-RG-004 Run time (Estimation and costing)  *(controls estimated vs actual time journal — see DEPENDENCIES.md)*
- PC-SETUP-ROUTES-RG-005 Quantity (Estimation and costing)
- PC-SETUP-ROUTES-RG-006 Job management (per job type)  *(must match MES-DEFAULTS job types)*
- PC-SETUP-ROUTES-RG-007 Automatic route consumption settings

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
