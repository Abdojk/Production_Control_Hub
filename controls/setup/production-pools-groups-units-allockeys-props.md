# Learning records — Pools / Groups / Units / Allocation keys / Properties / Tracked components

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Enrichment status:** ENRICHED 2026-05-31 — all 16 controls VERIFIED.
> **Sources:** Tier 1 — Production setup requirements (#1); Operations resources (#28); Allocation keys training unit (#29); Traceability integration with SCM (#12).

## Production groups (`GROUPS`) — Setup > Production groups
- **PC-SETUP-GROUPS-001 Production group (id)** — Identifier of the group; assigned to released products and copied to production orders at creation. — **VERIFIED** (#1)
- **PC-SETUP-GROUPS-002 Name / Description** — Descriptive name. — **VERIFIED** (#1)
- **PC-SETUP-GROUPS-003 Ledger - items / ledger posting accounts** — Defines the material, labor, and WIP ledger accounts for a production process; used to post or group orders for reporting. Active only when PARAMS Ledger posting = *Production groups* (see DEPENDENCIES.md). — **VERIFIED** (#1)

## Production pools (`POOLS`) — Setup > Production pools
- **PC-SETUP-POOLS-001 Production pool (id)** — Identifier used to group production orders. — **VERIFIED** (#1)
- **PC-SETUP-POOLS-002 Name / Description** — Groups production orders so you can process urgent orders, or delete and post groups of orders together. Purely an organisational grouping; no transactional/costing effect. — **VERIFIED** (#1)

## Production units (`UNITS`) — Setup > Production units
> Administrative unit = a collection of resource groups; reflects the physical layout; **no effect on transactions or how they are processed**; used to consolidate and filter production data. Changes apply only to new orders created after master scheduling (existing orders must be changed manually).
- **PC-SETUP-UNITS-001 Production unit (id)** — Identifier of the administrative unit. — **VERIFIED** (#28)
- **PC-SETUP-UNITS-002 Name** — Descriptive name. — **VERIFIED** (#28)
- **PC-SETUP-UNITS-003 Site** — A production unit must be associated with a site. — **VERIFIED** (#28)
- **PC-SETUP-UNITS-004 Picking / storage warehouse (and resource-group membership)** — Optionally assign a picking warehouse and a storage warehouse to the production unit; resource groups are each assigned to one production unit. — **VERIFIED** (#28)

## Allocation keys (`ALLOCKEYS`) — Setup > Allocation keys
> Define how **bundled** job registrations (multiple jobs started together on the Job registration page) allocate the total registered time to the individual jobs. Scope is set by Sites / Production units / Resources / Resource types on the key.
- **PC-SETUP-ALLOCKEYS-001 Allocation key (id)** — Identifier. — **VERIFIED** (#29)
- **PC-SETUP-ALLOCKEYS-002 Description** — Descriptive name. — **VERIFIED** (#29)
- **PC-SETUP-ALLOCKEYS-003 Bundle type** — How total bundle time is split across jobs: *Estimation* (by estimated time), *Jobs* (by total jobs bundled and time spent), *Net time* (equally among jobs in the bundle at any time), *Real time* (actual job time; can cost from actual payroll). *(Re-scoped from the earlier unsourced "Period allocation lines" stub.)* — **VERIFIED** (#29)

## Properties (`PROPS`) — Setup > Properties
- **PC-SETUP-PROPS-001 Property (id)** — Identifier of the property. — **VERIFIED** (#1)
- **PC-SETUP-PROPS-002 Description** — Special attribute assigned to resources to control the order/sequence of productions; connected to the working time template. Used with PARAMS Finite property scheduling. — **VERIFIED** (#1)

## Tracked components policy (`TRACKEDCOMP`) — Setup > Production > Tracked components policy
- **PC-SETUP-TRACKEDCOMP-001 Policy name** — Identifier of the policy, later assigned to finished products/components on Released products. — **VERIFIED** (#12)
- **PC-SETUP-TRACKEDCOMP-002 Use tracked components (toggle)** — *Yes*: enables registering/associating batch/serial numbers of components with the produced product's batch/serial (item traceability). *No*: not tracked. — **VERIFIED** (#12)
