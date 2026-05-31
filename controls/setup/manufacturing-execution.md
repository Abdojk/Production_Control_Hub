# Learning records — Manufacturing execution setup (`MES-DEFAULTS`, `MES-PFE`)

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Screen skeleton confidence:** `skeleton-partial`
> **Enrichment status:** NOT STARTED — all controls UNKNOWN.

## Production order defaults (`MES-DEFAULTS`) — Setup > Manufacturing execution > Production order defaults
> Tabs: General, Start, Operations, Report as finished, Quantity validation.
- PC-SETUP-MES-DEFAULTS-001 Skip time adjustments  *(requires feature mgmt flag; affects automatic route consumption — see DEPENDENCIES.md)*
- PC-SETUP-MES-DEFAULTS-002 General job parameter settings (group)
- PC-SETUP-MES-DEFAULTS-003 Start parameters (Start tab)
- PC-SETUP-MES-DEFAULTS-004 Job types requiring registration (Operations tab)  *(must match Route groups Job management)*
- PC-SETUP-MES-DEFAULTS-005 Report as finished parameters
- PC-SETUP-MES-DEFAULTS-006 Quantity validation parameters

## Configure production floor execution (`MES-PFE`) — Setup > Manufacturing execution > Configure production floor execution
- PC-SETUP-MES-PFE-001 Clock in and out only  *(blocks most other options; requires Tab selection emptied)*
- PC-SETUP-MES-PFE-002 Report quantity at clock-out
- PC-SETUP-MES-PFE-003 Lock employee
- PC-SETUP-MES-PFE-004 Use the actual time of registration
- PC-SETUP-MES-PFE-005 Single worker
- PC-SETUP-MES-PFE-006 Tab selection (interface design)
