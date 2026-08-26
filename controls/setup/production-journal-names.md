# Learning records — Production journal names (`JOURNALNAMES`)

> **D365 version:** SCM 10.0.47 (build 10.0.2527)
> **Path:** Production control > Setup > Production journal names
> **Screen skeleton confidence:** `skeleton-partial`
> **Enrichment status:** PARTIAL 2026-05-31 — 4/10 VERIFIED, 6 UNKNOWN (need a dedicated Tier-1 journal-name/voucher source).
> **Sources:** Tier 1 — Production setup requirements (#1), Production dispensing (#9), ProductionJournalNameEntity CDM (#11, confirms field existence only).

- **PC-SETUP-JOURNALNAMES-001 Journal name** — Identifier of the journal name used to record and post production transactions; referenced as the default journal on the parameters page and on order lines. — **VERIFIED** (#1)
- **PC-SETUP-JOURNALNAMES-002 Description** — Free-text description. — **VERIFIED** (#1)
- **PC-SETUP-JOURNALNAMES-003 Journal type** — Classifies the journal (picking list / route card / job card / report as finished, etc.), determining where it can be used. — **VERIFIED** (#1)
- **PC-SETUP-JOURNALNAMES-010 Dispensing tickets (toggle)** — *Yes*: marks the journal name as the dispensing pick journal, making it selectable as the Dispensing tickets default on the parameters page. — **VERIFIED** (#9)
- **PC-SETUP-JOURNALNAMES-004 Default private user group** — Field exists (CDM). Per-state effect not yet grounded. — **UNKNOWN — Insufficient data to verify.**
- **PC-SETUP-JOURNALNAMES-005 Delete lines after posting** — Field exists (CDM `WillPostingDeleteLinesByDefault`). — **UNKNOWN — Insufficient data to verify.**
- **PC-SETUP-JOURNALNAMES-006 Default posting summation level** — Field exists (CDM). — **UNKNOWN — Insufficient data to verify.**
- **PC-SETUP-JOURNALNAMES-007 Voucher number allocation rule** — Field exists (CDM). — **UNKNOWN — Insufficient data to verify.**
- **PC-SETUP-JOURNALNAMES-008 Voucher number selection rule** — Field exists (CDM). — **UNKNOWN — Insufficient data to verify.**
- **PC-SETUP-JOURNALNAMES-009 Voucher series / number sequence code** — Field exists (CDM). — **UNKNOWN — Insufficient data to verify.**
