# Learning records — Common: Production orders, Batch orders, Kanban boards

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Screen skeleton confidence:** `skeleton-partial` (operational forms — Action Pane not exhaustively documented)
> **Enrichment status:** NOT STARTED — all controls UNKNOWN.

## All production orders (`PORD`) — Production control > Production orders > All production orders
- PC-COMMON-PORD-001 New production order
- PC-COMMON-PORD-002 Estimate
- PC-COMMON-PORD-003 Schedule — Operations scheduling
- PC-COMMON-PORD-004 Schedule — Job scheduling
- PC-COMMON-PORD-005 Release (print Job card / Route job / Route card)
- PC-COMMON-PORD-006 Start (From oper. no.; Automatic route/BOM consumption; Post now; Print picking list)
- PC-COMMON-PORD-007 Report as finished (Good qty; Error qty; Error cause; End job; Accept error)
- PC-COMMON-PORD-008 End (Date; Scrap method)
- PC-COMMON-PORD-009 View > Picking list
- PC-COMMON-PORD-010 View > Reported as finished
- PC-COMMON-PORD-011 Manage costs > View cost comparison

## All batch orders (`BORD`) — Production control > Batch orders > All batch orders
- PC-COMMON-BORD-001 New batch order
- PC-COMMON-BORD-002 Estimate
- PC-COMMON-BORD-003 Schedule
- PC-COMMON-BORD-004 Release
- PC-COMMON-BORD-005 Start
- PC-COMMON-BORD-006 Report as finished / End
> Batch balancing for active-ingredient formulas runs from **Cost management > Batch orders > Batch balancing** (cross-module dependency).

## Kanban board for process jobs (`KPROC`)
- PC-COMMON-KPROC-001 Prioritize
- PC-COMMON-KPROC-002 Pick
- PC-COMMON-KPROC-003 Manufacture (report)
- PC-COMMON-KPROC-004 Bar code scanning

## Kanban board for transfer jobs (`KTRANS`)
- PC-COMMON-KTRANS-001 Filters (Production flow / Activity / From-To warehouse-location)
- PC-COMMON-KTRANS-002 Start
- PC-COMMON-KTRANS-003 Complete
- PC-COMMON-KTRANS-004 Job quantity (capped to kanban rule original quantity)

## Kanban schedule board / Kanban job scheduling (`KSCHED`)
- PC-COMMON-KSCHED-001 Schedule unplanned job
- PC-COMMON-KSCHED-002 Reschedule job to period
- PC-COMMON-KSCHED-003 Change job status

## Production floor execution interface — runtime (`PFE-RUN`)
- PC-COMMON-PFE-RUN-001 Clock in / clock out
- PC-COMMON-PFE-RUN-002 Start / stop job (job bundling)
- PC-COMMON-PFE-RUN-003 Report feedback / report as finished
