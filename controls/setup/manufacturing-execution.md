# Learning records — Manufacturing execution setup (`MES-DEFAULTS`, `MES-PFE`)

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Enrichment status:** ENRICHED 2026-05-31.
> **Primary sources (fetched this session):** Tier 1 — Production parameters for manufacturing execution (SOURCES #6); Configure the production floor execution interface (#8); Registration for manufacturing execution (#7).

Format: `ID | control` — **effect** — status.

## Production order defaults (`MES-DEFAULTS`) — Setup > Manufacturing execution > Production order defaults
> Tabs: General, Start, Operations, Report as finished, Quantity validation. Refined to documented fields (was a 6-item stub → 8 fields).
- **PC-SETUP-MES-DEFAULTS-001 Skip time adjustments (General)** — *Yes*: actual-cost calc considers only recorded start/end times; orders can end without supervisor time-adjustment approval. *No*: adjustments from Time and attendance review are applied. (Feature-gated, 10.0.41+.) — **VERIFIED** (#7)
- **PC-SETUP-MES-DEFAULTS-002 Update start on-line (Start)** — *Status*: starting updates status only. *Status + quantity*: starting updates status and quantity (required for start-time BOM consumption). — **VERIFIED** (#6)
- **PC-SETUP-MES-DEFAULTS-003 Automatic BOM consumption — Start** — *Flushing principle* / *Always* / *Never*: whether/how materials are deducted (picking-list posted) at job start. *Always* here requires *Never* on Operations and RAF to avoid double deduction. — **VERIFIED** (#6)
- **PC-SETUP-MES-DEFAULTS-004 Job types requiring registration (Operations)** — Selects which job types (setup, process, transport, …) workers must register. Must match the **Job management** column on Route groups, or jobs become unavailable for registration / operations won't report finished. — **VERIFIED** (#6)
- **PC-SETUP-MES-DEFAULTS-005 Automatic BOM consumption — Operations** — Same three options, applied when an operation is completed (backflush-on-operation). — **VERIFIED** (#6)
- **PC-SETUP-MES-DEFAULTS-006 Update finished report on-line (Report as finished)** — *Status* / *Status + quantity*: what RAF on the last operation updates. — **VERIFIED** (#6)
- **PC-SETUP-MES-DEFAULTS-007 Automatic BOM consumption — Report as finished** — Same three options, applied at RAF (backflush-on-production). — **VERIFIED** (#6)
- **PC-SETUP-MES-DEFAULTS-008 Quantity validation parameters** — Validates start and feedback quantities on production orders. — **VERIFIED** (#6, tab-level)

## Configure production floor execution (`MES-PFE`) — Setup > Manufacturing execution > Configure production floor execution
> Expanded from a 6-item stub to the full documented control set (5 FastTabs + 1 action). All VERIFIED from #8.

### General FastTab
- **PC-SETUP-MES-PFE-001 Clock in and out only** — *Yes*: simplified clock-in/out-only interface; disables most other options; Tab selection must be emptied first. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-002 Report quantity at clock-out** — *Yes*: prompts workers to report feedback on in-progress jobs at clock-out. *No*: no prompt. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-003 Lock employee** — *No*: worker signed out immediately after each registration (returns to sign-in). *Yes*: worker stays signed in; can manually sign out to let another sign in under the same system user account. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-004 Use the actual time of registration** — *Yes*: registration time = exact submit time. *No*: sign-in time is used. Recommended *Yes* when Lock employee/Single worker = Yes. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-005 Single worker** — *Yes*: one worker per device; auto-sets Lock employee = Yes; removes badge/personnel sign-in — worker signs in via a system user account linked to a *time registered worker*. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-007 Suppress numpad keyboard** — On: prevents the numpad opening when entering/changing a quantity. — **VERIFIED** (#8)

### Tab selection FastTab
- **PC-SETUP-MES-PFE-006 Tab selection** — Selects which tabs the interface shows for this configuration; tabs are designed/arranged here (see Design the production floor execution interface). — **VERIFIED** (#8)

### Login FastTab
- **PC-SETUP-MES-PFE-008 Enable numpad (login)** — *Yes*: touch-screen numpad on sign-in for badge/personal number. *No*: hidden. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-009 Allow locking the touchscreen** — *Yes*: adds a "Lock screen for sanitizing" button that temporarily locks the screen with a countdown. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-010 Screen lock duration** — Seconds the touchscreen stays locked for sanitizing (5–120). — **VERIFIED** (#8)

### Main view FastTab
- **PC-SETUP-MES-PFE-011 Enable search** — *Yes*: search field on the jobs list (by job ID / order ID, keypad or bar code). — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-012 Enable search by project ID** — *Yes*: also search by project ID (only when Enable search = Yes). — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-013 Auto-open start dialog** — *Yes*: Start job dialog opens automatically when a job is found via search. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-014 Auto-open report progress dialog** — *Yes*: Report progress dialog opens automatically when a job is found via search. — **VERIFIED** (#8)

### Report progress FastTab
- **PC-SETUP-MES-PFE-015 Skip product selection** — *Yes*: skips the formula-item/co-/by-product selection page; goes straight to quantity/dimensions. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-016 View materials** — *Yes*: workers can view a job's material list from the Report progress dialog (10.0.46+ feature). — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-017 Enable adjust material** — *Yes*: adds the Adjust material button to adjust consumption. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-018 Default remaining quantity** — *Yes*: pre-fills expected remaining quantity. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-019 Default nominal quantity** — *Yes*: pre-populates nominal quantity for catch-weight items. *No*: blank (manual). — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-020 Require existing license plate** — *Yes*: worker must specify an existing LP at RAF. *No*: any LP; created if new. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-021 Generate license plate** — *Yes*: generates a new LP at each RAF (from the Warehouse management parameters number sequence). *No*: must specify existing LP. — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-022 Print label** — *Yes*: prints an LP label at RAF (layout from document routing). — **VERIFIED** (#8)
- **PC-SETUP-MES-PFE-023 Add material line** — *Yes*: allows adding/deleting material lines in the adjust-material dialog. — **VERIFIED** (#8)

### Action
- **PC-SETUP-MES-PFE-024 Clean up client configurations** — Removes device configuration/sign-in records inactive beyond a specified number of days (auto batch job runs at 60 days). — **VERIFIED** (#8)
