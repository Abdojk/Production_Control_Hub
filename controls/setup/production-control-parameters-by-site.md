# Learning records — Production control parameters by site (`PARAMSITE`)

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Path:** Production control > Setup > Production control parameters by site
> **Enrichment status:** ENRICHED 2026-05-31 — 15/15 VERIFIED.
> **Gating:** Site parameters take effect only when PARAMS `Parameter usage` (PC-SETUP-PARAMS-001) = *By site*; otherwise company-level values apply, and undefined site rows fall back to company values. See DEPENDENCIES.md.
> **Source:** Tier 1 — Production control parameters training unit (#5), which states the by-site page follows the same tab pattern and lists the parameters that "can also apply to sites". Each control below carries the same business effect as its company-level twin (already VERIFIED in production-control-parameters.md), scoped to the selected site.

- **PC-SETUP-PARAMSITE-001 Site selector** — Selects the site whose parameter overrides are being edited. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-002 Maximum job lead time (site)** — Site-scoped twin of PARAMS-005. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-003 Post picking list in ledger (site)** — Twin of PARAMS-010. — **VERIFIED** (#5, #3)
- **PC-SETUP-PARAMSITE-004 Post report as finished in ledger (site)** — Twin of PARAMS-011. — **VERIFIED** (#5, #3)
- **PC-SETUP-PARAMSITE-005 Post excl. transaction type (site)** — Twin of PARAMS-012. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-006 Planned order (site)** — Twin of PARAMS-013. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-007 Project (site)** — Twin of PARAMS-014. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-008 Limited work center search (site)** — Twin of PARAMS-015. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-009 Price calculation (site)** — Twin of PARAMS-016. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-010 Delete capacity reservations (site)** — Twin of PARAMS-017. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-011 Use estimated cost price (site)** — Twin of PARAMS-018. — **VERIFIED** (#5, #3)
- **PC-SETUP-PARAMSITE-012 Default journal — Picking list (site)** — Twin of PARAMS-019. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-013 Default journal — Route card (site)** — Twin of PARAMS-020. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-014 Default journal — Job card (site)** — Twin of PARAMS-021. — **VERIFIED** (#5)
- **PC-SETUP-PARAMSITE-015 Default journal — Report as finished (site)** — Twin of PARAMS-022. — **VERIFIED** (#5)
