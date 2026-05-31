# Learning records — Production control parameters (`PARAMS`)

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Path:** Production control > Setup > Production control parameters
> **Screen skeleton confidence:** `skeleton-partial` (Documents / Number sequences tabs + full Status matrix still to enumerate)
> **Enrichment status:** ENRICHED 2026-05-31 — 49/50 VERIFIED, 1 UNKNOWN.
> **Primary sources (fetched this session):** Tier 1 — Production control parameters training unit (SOURCES #5); Production postings, Finance/GL (#3) and Cost management (#4); Production dispensing (#9).

Format: `ID | control` — **ON/value effect** — **OFF/unset effect** — status.

## General tab
- **PC-SETUP-PARAMS-001 Parameter usage** — *By company*: system always uses company-wide parameters. *By site*: system uses site-specific parameters where defined, else falls back to company parameters. — n/a (enum) — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-002 Profit setting** — Selected profit setting (linked via cost groups → cost categories) is used by default to determine the item sales price; establishes the reference between item consumption, route consumption and profit. — No default profit reference for price determination. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-003 Reservation** — *Manual*: no automatic reservation. *Estimation*: auto-reserves raw material at estimation. *Scheduling*: auto-reserves at scheduling. *Start*: auto-reserves at start. — *Manual* = unset behaviour. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-004 Ledger posting** — Sets the source of GL posting accounts for production: *Item and resource* → WIP/time accounts from the costing resource/resource group on the route operation (most granular); *Item and category* → from the cost categories on route lines; *Production groups* → from the Production groups page (copied to order at creation). Value is copied to the order's **Ledger** field at creation. — n/a (enum, mandatory) — **VERIFIED** (#3, #4)
- **PC-SETUP-PARAMS-005 Maximum job lead time** — If a production order's lead time exceeds this many days when Operations/Job scheduling runs, scheduling does not occur. — 0/blank = no lead-time cap enforced. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-006 Route network** — ON: enables complex networks (parallel branches started independently; internal sequence built manually; simultaneous operations share the operation number). OFF: simple sequential operations only; no manual network needed. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-007 Mandatory date** — ON: a route validity period must be entered; route becomes invalid once its start date expires. OFF: no validity period required. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-008 Block removal of approval** — ON: route status cannot be changed once approved. OFF: approval can be removed. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-009 Block editing** — ON: routes cannot be edited. OFF: routes editable. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-010 Post picking list in ledger** — ON: inventory transactions from picking-list posting are posted to the ledger (subject to Item model group *Post physical inventory* + inventory posting profile accounts — see DEPENDENCIES.md). OFF: picking list does not post to GL. — **VERIFIED** (#3)
- **PC-SETUP-PARAMS-011 Post report as finished in ledger** — ON: RAF postings reach the ledger (subject to same prerequisites). OFF: RAF does not post to GL. — **VERIFIED** (#3)
- **PC-SETUP-PARAMS-012 Post excl. transaction type** — ON: the transaction type is excluded from ledger transactions when they are totalled and created during production posting. OFF: not excluded. *(Tier-1 statement is terse.)* — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-013 Planned order** — ON: capacity reserved for planned orders is included during production scheduling. OFF: excluded. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-014 Project** — ON: capacity reserved for projects is included during production scheduling. OFF: excluded. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-015 Limited work center search** — ON: scheduling picks the first work center meeting the required date/time (faster). OFF: scheduling searches for the work center giving the shortest lead time (slower, optimised). — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-016 Price calculation** — ON: estimated cost price is calculated during estimation (viewable on Price calculation page). OFF: no estimate-time calculation. Realised cost price is computed on journal posting regardless. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-017 Delete capacity reservations** — ON: capacity reservations are deleted when orders are reported as finished. OFF: retained. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-018 Use estimated cost price** — ON: estimated cost price determines the physical value at RAF. OFF: standard cost (defined for the product) is used at RAF. — **VERIFIED** (#5, #3)
- **PC-SETUP-PARAMS-049 Default measuring device** — Sets the device shown by default on the Dispensing ticket page. — Unset = no default device. — **VERIFIED** (#9)

## Journals tab
- **PC-SETUP-PARAMS-019/020/021/022 Default journals (Picking list / Route card / Job card / Report as finished)** — The chosen journal name is used by default to record the respective consumption/feedback when nothing is specified on the production order line. — Unset = must specify a journal per order. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-050 Default journal — Dispensing tickets** — Default journal for dispensed products. — Unset = no default dispensing journal. — **VERIFIED** (#9)
- **PC-SETUP-PARAMS-023 Pick negative** — ON: allows negative picking in physical inventory when posting. OFF: blocked. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-024 Physical reduction** — ON: automatically reduces item consumption to physical inventory when items are out of stock. OFF: no auto reduction. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-025 Inv. managed planned order qty** — ON: the default (planned) quantity in the picking list journal controls and records the corresponding inventory transactions. OFF: the consumption quantity in the picking list journal controls/records them. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-026 Accept error** — ON: system accepts missing feedback on work-center and item consumption. OFF: missing feedback not accepted. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-027 Automatic BOM consumption (journals)** — ON: system automatically picking-list-updates BOM consumption for the current production. OFF: manual. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-028 Mandatory cost category for quantity** — ON: a quantity category must be associated before the order can be started; otherwise start is blocked. OFF: not mandatory. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-029 Mandatory cost category for hours** — ON: an hour category must be associated before start; otherwise start is blocked. OFF: not mandatory. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-030 Automatic report as finished** — ON: system auto-reports feedback as finished for the last operation. OFF: manual RAF. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-031 Update capacity plan** — ON: on Route/Job card posting, the operation is auto-rescheduled backward from the current end date/time and reserved capacity is adjusted to the remaining quantity. OFF: no auto reschedule. — **VERIFIED** (#5)

## Automatic update tab
- **PC-SETUP-PARAMS-032 Scheduling method** — *Operations scheduling*: rough start/end dates from resource-group capacity. *Job scheduling*: creates jobs and computes precise start/end per job/operation. — n/a (enum) — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-033 Automatic BOM consumption** — *Flushing principle* / *Always* / *Never*: controls auto BOM consumption (picking-list posting) when the order is updated. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-034 Automatic route consumption** — Sets auto route consumption when an automatic Start runs because a mandatory update was skipped (e.g. RAF run before Start). — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-035 Group by vendor** — ON: auto-created purchases (at estimation) are grouped by supplier. OFF: one purchase with one line per planned purchase order. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-036 Group by purchase agreement** — Controls grouping of auto-created purchases by purchase agreement during estimation. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-037 Find purchase agreements** — ON: searches for purchase agreements during estimation and copies price/discount to PO lines. OFF: no search. — **VERIFIED** (#5)

## Standard update tab
- **PC-SETUP-PARAMS-038 Scrap method** — Selects how item/work-center consumption for error-reported quantity is posted: *Allocation* (scrap cost added to good finished goods) vs *Scrap account* (posted to a dedicated account). — **VERIFIED** (#4, #5)
- **PC-SETUP-PARAMS-039 Scrap account** — Ledger account to which scrap is posted when method = Scrap account. — **VERIFIED** (#4)
- **PC-SETUP-PARAMS-040 Finite capacity** — ON: scheduling observes capacity limitations. OFF: infinite capacity assumed. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-041 Finite material** — ON: scheduling treats material availability as critical, using estimated futures dates for components. OFF: materials assumed available / immediately procurable. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-042 Finite property** — ON: scheduling observes property requirements (e.g. sequential same-property operations skip setup time in job scheduling). OFF: properties ignored. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-043 Enable dispensing for production** — ON: production dispensing can be used in a production flow. OFF: dispensing disabled. (Requires Advanced quality management + Dispense management features — see DEPENDENCIES.md.) — **VERIFIED** (#9)
- **PC-SETUP-PARAMS-044 Allow over-dispensing with reverse pick** — ON: material may be over-dispensed/over-picked, with the remainder returned to inventory via an automatically generated pick list. OFF: over-dispensing blocked. — **VERIFIED** (#9)

## Status / Inventory dimensions / Unit of measure / Lean tabs
- **PC-SETUP-PARAMS-045 Status update matrix** — Per-status checkboxes indicate whether a given update can run on a production order at that status; clearing a box blocks that update at that stage. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-046 Inventory dimensions display selection** — Selects which inventory dimensions appear in journals, lines and tables. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-047 Lean time units** — Defines the units (Days/Hours/Minutes/Seconds) used as time units in lean production-flow activities. — **VERIFIED** (#5)
- **PC-SETUP-PARAMS-048 Lean manufacturing default parameters** — Per-field business effect not enumerated by Microsoft on this page (points to the lean learning path). **Status: UNKNOWN — Insufficient data to verify per-state effects; revisit with lean-manufacturing sources.**
