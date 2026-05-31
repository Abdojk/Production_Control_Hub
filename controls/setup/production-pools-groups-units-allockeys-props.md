# Learning records — Pools / Groups / Units / Allocation keys / Properties / Tracked components

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Screen skeleton confidence:** `skeleton-partial` (all forms below — minimal documented field lists)
> **Enrichment status:** NOT STARTED — all controls UNKNOWN.

## Production pools (`POOLS`) — Setup > Production pools
- PC-SETUP-POOLS-001 Production pool (id)
- PC-SETUP-POOLS-002 Name / Description

## Production groups (`GROUPS`) — Setup > Production groups
- PC-SETUP-GROUPS-001 Production group (id)
- PC-SETUP-GROUPS-002 Name / Description
- PC-SETUP-GROUPS-003 Ledger - items / ledger posting accounts  *(referenced by PARAMS Ledger posting = Production groups — see DEPENDENCIES.md)*

## Production units (`UNITS`) — Setup > Production units
- PC-SETUP-UNITS-001 Production unit (id)
- PC-SETUP-UNITS-002 Name
- PC-SETUP-UNITS-003 Site
- PC-SETUP-UNITS-004 Resource group / warehouse association

## Allocation keys (`ALLOCKEYS`) — Setup > Allocation keys
- PC-SETUP-ALLOCKEYS-001 Allocation key (id)
- PC-SETUP-ALLOCKEYS-002 Description
- PC-SETUP-ALLOCKEYS-003 Period allocation lines

## Properties (`PROPS`) — Setup > Properties
- PC-SETUP-PROPS-001 Property (id)
- PC-SETUP-PROPS-002 Description

## Tracked components policy (`TRACKEDCOMP`) — Setup > Production > Tracked components policy
- PC-SETUP-TRACKEDCOMP-001 Policy name
- PC-SETUP-TRACKEDCOMP-002 Use tracked components (toggle)
