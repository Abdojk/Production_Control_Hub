# Learning records — Production journal names (`JOURNALNAMES`)

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Path:** Production control > Setup > Production journal names
> **Screen skeleton confidence:** `skeleton-partial`
> **Enrichment status:** PARTIAL 2026-05-31 — 6/10 VERIFIED, 4 UNKNOWN.
> **Sources:** Tier 1 — Production setup requirements (#1), Production dispensing (#9), ProductionJournalNameEntity CDM (#11, confirms field existence only), One voucher / journal-names voucher framework (#30), General journal processing / number sequences (#31).

- **PC-SETUP-JOURNALNAMES-001 Journal name** — Identifier of the journal name used to record and post production transactions; referenced as the default journal on the parameters page and on order lines. — **VERIFIED** (#1)
- **PC-SETUP-JOURNALNAMES-002 Description** — Free-text description. — **VERIFIED** (#1)
- **PC-SETUP-JOURNALNAMES-003 Journal type** — Classifies the journal (picking list / route card / job card / report as finished, etc.), determining where it can be used. — **VERIFIED** (#1)
- **PC-SETUP-JOURNALNAMES-010 Dispensing tickets (toggle)** — *Yes*: marks the journal name as the dispensing pick journal, making it selectable as the Dispensing tickets default on the parameters page. — **VERIFIED** (#9)
- **PC-SETUP-JOURNALNAMES-004 Default private user group** — Field exists (CDM). Per-state effect not yet grounded. — **UNKNOWN — Insufficient data to verify.**
- **PC-SETUP-JOURNALNAMES-005 Delete lines after posting** — Field exists (CDM `WillPostingDeleteLinesByDefault`). — **UNKNOWN — Insufficient data to verify.**
- **PC-SETUP-JOURNALNAMES-006 Default posting summation level** — Field exists (CDM). — **UNKNOWN — Insufficient data to verify.**
- **PC-SETUP-JOURNALNAMES-007 Voucher number allocation rule** — Field exists (CDM). — **UNKNOWN — Insufficient data to verify.**
- **PC-SETUP-JOURNALNAMES-008 Voucher number selection rule (New voucher)** — Controls how voucher numbers are assigned to journal lines: e.g. *One voucher number only* (all lines share one voucher) vs *In connection with balance* (a new voucher starts when the running balance is zero). Governs how production journal transactions group into vouchers in the ledger. — **VERIFIED** (#30, journal-names voucher framework)
- **PC-SETUP-JOURNALNAMES-009 Voucher series / number sequence code** — The number sequence that supplies voucher numbers for the journal; can be continuous or non-continuous (non-continuous with preallocation improves posting performance). — **VERIFIED** (#31)
