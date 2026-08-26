# DEPENDENCIES.md — Cross-screen dependency layer (directed links)

> **Version lock:** D365 SCM 10.0.47 (build 10.0.2527)
> **Last updated:** 2026-05-31
> Directed links between controls: `requires` / `blocks` / `affects`. Populated during Mission 2 enrichment; seeded here with links Microsoft states directly (Tier 1) while building the Setup skeleton.
> Format: `<source control id>` — relation — `<target>` | note | trust | source

## Seeded links (Tier 1, from skeleton build)

- `PC-SETUP-PARAMS-010` (Post picking list in ledger) — **requires** — Item model groups *Post physical inventory* (Inventory management) AND Inventory posting profile *Estimated cost of materials consumed* / *…WIP* main accounts. | Picking-list journal will not post to GL unless all three are set. | VERIFIED | Tier 1: production-posting (finance/general-ledger)
- `PC-SETUP-PARAMS-011` (Post report as finished in ledger) — **requires** — Item model groups *Post physical inventory* AND Inventory posting profile *Estimated manufactured cost* / *…WIP* main accounts. | RAF journal will not post to GL otherwise. | VERIFIED | Tier 1: production-posting
- `PC-SETUP-PARAMS-004` (Ledger posting) — **affects** — source of GL posting accounts: *Item and resource* → resource/resource group; *Item and category* → cost categories; *Production groups* → `PC-SETUP-GROUPS-003`. | Determines which master drives WIP/time postings. | VERIFIED | Tier 1: production-posting
- `PC-SETUP-PARAMS-004 = Production groups` — **requires** — `PC-SETUP-GROUPS-003` (Production groups ledger accounts) configured, and a production group assigned to released products. | VERIFIED | Tier 1: production-posting
- `PC-SETUP-PARAMSITE-001` (site parameters) — **requires** — `PC-SETUP-PARAMS-001` (Parameter usage) = *By site*. | Site-level parameters take effect only when company Parameter usage = By site; otherwise company values apply. | VERIFIED | Tier 1: production-control-parameters training unit
- `PC-SETUP-PARAMS-043` (Enable dispensing for production) — **requires** — Feature management *Advanced quality management* + *Dispense management* (on by default from 10.0.47); `PC-SETUP-PARAMS-050` (Dispensing tickets journal) set; `PC-SETUP-PARAMS-049` (Default measuring device) set. | VERIFIED | Tier 1: quality-production-dispensing
- `PC-SETUP-PARAMS-050` (Dispensing tickets journal) — **requires** — `PC-SETUP-JOURNALNAMES-010` (Dispensing tickets toggle = Yes on a journal name). | VERIFIED | Tier 1: quality-production-dispensing
- `PC-SETUP-MES-DEFAULTS-004` (Job types requiring registration) — **affects** — must match `PC-SETUP-ROUTES-RG-006` (Job management per job type). | Mismatch → jobs unavailable for registration / operations not reported finished. | VERIFIED | Tier 1: production-parameters-manufacturing-execution
- `PC-SETUP-ROUTES-RG-004` (Run time) — **affects** — whether route/job card time generates a GL voucher; *No* → job card journal with actual time; *Yes* → route card journal with estimated time. | VERIFIED | Tier 1: registration-manufacturing-execution + production-posting
- `PC-SETUP-MES-DEFAULTS-001` (Skip time adjustments) — **requires** — Feature management *Skip time adjustments when calculating actual cost per production order* (10.0.41+); **affects** automatic route consumption for route groups using estimated time. | VERIFIED | Tier 1: registration-manufacturing-execution
- `PC-SETUP-MES-PFE-001` (Clock in and out only) — **blocks** — most other MES-PFE options; **requires** Tab selection emptied first. | VERIFIED | Tier 1: production-floor-execution-configure

## Added v0.4 (enrichment batch 2)
- `PC-SETUP-MES-PFE-005` (Single worker) — **requires/forces** — `PC-SETUP-MES-PFE-003` (Lock employee) auto-set to Yes; also removes badge/personnel sign-in (needs a system user account linked to a time-registered worker). | VERIFIED | Tier 1: production-floor-execution-configure (#8)
- `PC-SETUP-MES-PFE-021` (Generate license plate) — **requires** — a license-plate number sequence on the Warehouse management parameters page. | VERIFIED | #8
- `PC-SETUP-MES-PFE-001` (Clock in and out only) — **requires** — Tab selection FastTab emptied before it can be enabled. | VERIFIED | #8
- `PC-SETUP-ROUTES-RG-007` (Complete secondary operation with primary) — **requires** — feature *Auto-complete secondary operation with primary* (10.0.46+). | VERIFIED | #8
- `PC-SETUP-MES-DEFAULTS-003/005/007` (Automatic BOM consumption Start/Operations/RAF) — **blocks** — must not overlap: *Always* on one stage requires *Never* on the others; *Flushing principle* on Start requires the same on Operations or RAF. Contradictory settings double-deduct or skip material. | VERIFIED | Tier 1: production-parameters-manufacturing-execution (#6)

## Added v0.5 (enrichment batch 3 — Setup complete)
- `PC-SETUP-PARAMS-042` (Finite property scheduling) — **requires** — `PC-SETUP-PROPS-*` (Properties) defined and assigned to resources via the working time template. | VERIFIED | Tier 1: production-set-up-requirements (#1)
- `PC-SETUP-ALLOCKEYS-003` (Bundle type) — **affects** — how bundled job-registration time is allocated to individual jobs (Estimation/Jobs/Net time/Real time); scoped by Site/Production unit/Resource/Resource type. | VERIFIED | Tier 1: allocation-keys (#29)
- `PC-SETUP-UNITS-003/004` (Production unit site/warehouse) — **affects** — used only to consolidate/filter production data; **no transactional effect**; changes apply to new orders after master scheduling only. | VERIFIED | Tier 1: operations-resources (#28)
- `PC-SETUP-COSTGRP-003` (Cost group ↔ profit setting) — **requires** — used by `PC-SETUP-PARAMS-002` (Profit setting) to derive sales price from consumption. | VERIFIED | Tier 1: production-control-parameters (#5)

> Enrichment will expand this file control-by-control. Unconfirmed links must carry trust=LOW and the "sandbox-test before relying" flag.
