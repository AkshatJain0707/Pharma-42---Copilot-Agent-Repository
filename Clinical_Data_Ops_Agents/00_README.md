# Clinical Data Operations Analytics Pack (Agents 35 to 39)

Built 20 October 2026. Same file set as earlier phases: instructions, playbook, volatile context file, config and tests. Numbering continues from agent 34. The strategic forecasting set was parked; it is not in this pack.

| Folder | Agent | Instructions (chars, limit 8,000) | Volatile file cadence |
|---|---|---|---|
| 35_data_management_plan_flow | Clinical Data Management Plan and Data Flow Architect | 5,813 | 30 days |
| 36_rbqm_central_monitoring | RBQM and Central Monitoring Analyst | 5,551 | 30 days |
| 37_data_quality_query_lock | Data Quality, Query and Database Lock Readiness Analyst | 5,621 | 30 days |
| 38_ops_performance_enrollment | Clinical Operations Performance and Enrollment Analytics Analyst | 5,654 | 30 days |
| 39_data_standards_submission | Clinical Data Standards and Submission Readiness Analyst | 5,937 | 30 days |

Also in this pack:
- `01_router_catalogue_additions.md`: rows and routes to add to the Engagement Router knowledge file.
- `02_tracker_additions_for_agent22.md`: rows for the Policy and Reimbursement Monitor tracker.
- `03_qa_notes_for_agent7.md`: what the QA and Red Team agent should check.

## How the five fit together

| Stage | Agent |
|---|---|
| Plan the data | 35 Data Management Plan and Data Flow Architect |
| Protect quality while the study runs | 36 RBQM and Central Monitoring Analyst |
| Clean and reach lock | 37 Data Quality, Query and Database Lock Readiness Analyst |
| Keep the timeline | 38 Operations Performance and Enrollment Analytics Analyst |
| Standardise and submit | 39 Data Standards and Submission Readiness Analyst |

## Signature methods

| Agent | Method |
|---|---|
| 35 | Critical Data Register tied to critical-to-quality factors, Data Flow Map with a blinding column, Vendor Oversight Matrix, Gate Plan |
| 36 | CtQ-to-KRI Ladder (separating study-level tolerance limits from site-level indicators), Signal Triage Card with competing explanations, Site Risk View by components |
| 37 | Query Analytics Lens, query hygiene rules (no leading queries), Reconciliation Tracker, Lock Readiness Scorecard with Ready, At risk, Blocked per item |
| 38 | Enrollment Funnel and Low-Base-High forecast, Site Performance Scorecard by components, Recovery Options Matrix |
| 39 | Standards Selection Record per study (catalogue row plus start date), Traceability Chain, separate Submission Gates |

## Guardrails shared by all five

These are in each agent's hard rules and trap tests:
- Never advise changing, backdating or fabricating data, or removing audit trails. Refer to quality assurance.
- Never use or request unblinded data or randomisation lists.
- Never process identifiable patient data.
- Never certify GCP compliance, system validation, inspection readiness or regulator acceptance.
- Never make safety or medical decisions; those go to the investigator, medical monitor and pharmacovigilance.
- Never accuse a site or person of misconduct from analytics.

## Research findings that shaped the files

1. **ICH E6(R3).** Principles and Annex 1: ICH Step 4 on 6 January 2025, effective in the EU, UK and Switzerland 23 July 2025, FDA final guidance 8 September 2025 (non-binding). Annex 2 (decentralised, pragmatic, real-world data trials): ICH Step 4 on 3 June 2026, CHMP adoption 25 June 2026, effective in the EU 15 January 2027; an FDA final Annex 2 was not found. One source says FDA published an Annex 2 draft in December 2024, so the FDA position is marked verify.
2. **Quality management content.** Annex 1 includes a data governance section (with blinding safeguards) and quality tolerance limits described as predefined acceptable ranges for critical trial metrics. The quality tolerance limit wording comes from a secondary summary, so verify it in the guideline text.
3. **CDISC and FDA.** Version choice is a catalogue row decision by study start date. SDTMIG 3.4 is reported for studies starting on or after 15 March 2025; XPT v5 was still specified as of a September 2026 summary; Dataset-JSON is under evaluation. Sources disagree on the Dataset-JSON v1.1 release date (December 2024 versus December 2025), flagged in the file.
4. **Enrollment benchmarks.** About 11 percent of ready sites enrol nobody (older Tufts analysis); another summary says 48 percent enrol none or under-enrol; a 27 percent figure circulates and is unverified. All are marked secondary and context only. A vendor-sponsored direct-to-patient study is tagged company-reported.

## Setup

Same steps as the Phase 3 README. Agent 39 benefits most from web search, because catalogue rows and versions change. Make sure the Engagement Router knowledge file is updated with `01_router_catalogue_additions.md`.

## Date note

Earlier packs (Phases 3 to 6) were stamped "18 October 2026" because the sandbox clock showed that date. Today is 20 October 2026. Treat their refresh dates as two days later: tracker 3 November 2026, volatile files 19 November 2026, playbooks 18 January 2027. This pack uses the correct date.

## Refresh calendar

| Item | Cadence | Next due |
|---|---|---|
| Agent 22 master tracker (add the new rows first) | 14 days | 3 November 2026 |
| Volatile files, agents 35 to 39 | 30 days | 19 November 2026 |
| Playbook files, agents 35 to 39 | 90 days | 18 January 2027 |
| Router catalogue | 30 days or on any agent change | 19 November 2026 |

Dates to diary: 15 January 2027 (E6(R3) Annex 2 effective in the EU); 13 November 2026 (India data protection phase, verify); the next FDA Data Standards Catalog and technical conformance guide releases.

## Items to verify before go-live

- FDA position on E6(R3) Annex 2.
- Exact quality tolerance limit wording in E6(R3) section 3.10.
- Current FDA Data Standards Catalog row, technical conformance guide version and transport format.
- Dataset-JSON v1.1 release date and FDA acceptance status.
- Current dictionary versions for coding, and current regulator guidance on computerised systems, Part 11 and decentralised elements (no source in this build).
- Every "Items to verify" list at the end of each volatile file.
