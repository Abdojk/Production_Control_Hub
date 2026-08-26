# Production_Control_Hub

Autonomous learning & advisory engine for the **Dynamics 365 Finance & Operations — Production control** module (D365 Supply Chain Management).

**Version lock:** SCM 10.0.47 (build 10.0.2527), latest GA as of 2026-05-31.

## What this repo is
A persistent knowledge base that (1) maps the complete Production control module surface from Microsoft Learn, (2) enriches each control with its real business effect, and (3) converts business requirements into click-level setup instructions. Continuity is file-based — every session reads these files first and resumes from recorded state.

## Files (read at the start of every session)
| File | Role |
|---|---|
| `KNOWLEDGE_MAP.md` | The skeleton — Levels 1–4, every control with an ID + status. The denominator. |
| `COVERAGE_STATE.md` | Status of every control + counts. The numerator source. |
| `DEPENDENCIES.md` | Directed cross-screen links (requires / blocks / affects). |
| `SOURCES.md` | Every URL used, with tier + access date. |
| `CHANGELOG.md` | Map versions, discovered controls, MS page revisions. |
| `controls/<group>/<form>.md` | Per-form learning records (business-effect findings). |

## Current state (v0.5)
- **Mission 1 (skeleton):** all 5 groups at Level 4 — **35 forms, 210 controls** (`skeleton-partial`).
- **Mission 2 (enrichment):** **Setup group COMPLETE** → **verified-knowledge X = 65.7/100 (138/210)**. Setup 138/143 verified; 5 left honestly UNKNOWN (no Tier-1 source).
- **Next:** Group 2 (Common / Daily) production-order lifecycle controls (strong Tier-1 task guides in hand) → module toward ~88%.
- **Note:** growing the skeleton is *not* the same as knowing the module; see COVERAGE_STATE.md for the two distinct metrics.

## Triggers
- `How_much_do_You_know?` → coverage readout per group vs the map (no estimates).
