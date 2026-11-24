# Six independent forecasting agents for Microsoft Copilot Studio

Built 20 October 2026. Each agent is standalone: one instruction file, one self-contained knowledge file, one config and test file. No agent calls, references, or needs another agent, a router, or a shared file. Deploy any one alone.

| # | Agent | Folder | Instructions (chars) | Knowledge (chars) | Optional workbook |
|---|---|---|---|---|---|
| 1 | Probability of Success and Catalyst Forecaster | 1_Probability_of_Success_and_Catalyst | 5,295 | 13,390 | forecast_pos_workbook.xlsx |
| 2 | Loss of Exclusivity and Erosion Forecaster | 2_Loss_of_Exclusivity_and_Erosion | 4,895 | 12,353 | forecast_loe_workbook.xlsx |
| 3 | Net Price and Access Policy Forecaster | 3_Net_Price_and_Access_Policy | 4,821 | 12,153 | forecast_netprice_workbook.xlsx |
| 4 | Competitive War Game and Response Forecaster | 4_Competitive_War_Game_and_Response | 4,921 | 10,429 | none (matrices built in chat) |
| 5 | Scenario Planning and Strategic Signposts Analyst | 5_Scenario_Planning_and_Signposts | 5,097 | 11,543 | none (matrices built in chat) |
| 6 | Market Sizing and Revenue Forecast Analyst | 6_Market_Sizing_and_Revenue | 5,217 | 11,506 | forecast_market_workbook.xlsx |
Copilot Studio instruction limit is 8,000 characters. Every instruction file is under 5,400.

## What makes them more powerful than the earlier versions
1. Built-in knowledge, not placeholders: dated, sourced benchmarks and policy facts read on 20 Oct 2026 (development success rates, FDA review clocks, complete response letter evidence, US negotiation timeline, most-favored-nation agreements, generic price erosion, biosimilar uptake, EU reform status). Each is tagged [S, playbook] with source and a "verify newer edition" rule.
2. Commands for a terse workflow: /forecast, /update, /clock, /calendar, /protect, /entry, /erode, /waterfall, /policy, /event, /profile, /ach, /game, /payoff, /drivers, /scenarios, /stress, /funnel, /uptake, /revenue, /sensitivity, /redteam, /explain. Quick, standard, and deep modes.
3. Arithmetic in the chat: odds updates, stage chains, FDA clock dates, channel-blended net price, erosion revenue bridges, competing-hypotheses scoring, payoff and regret matrices, robustness scores, logistic and Bass uptake curves, one-at-a-time sensitivity. Worked examples in each playbook let you check outputs.
4. Fixed output cards with range, label, confidence, signposts, decision trigger, pre-mortem, and a log line.
5. A built-in self-check before every answer.
6. 18 tests per agent (5 common traps, up to 13 specific, many with golden numeric answers).
7. Four optional workbooks with live formulas (recalculated, zero errors). Agents work without them.

## Research that went in (see Sources_and_Research_Log.md)
- Development success: BIO, Informa, QLS 2011 to 2020 (LOA 7.9%, Phase II 28.9%, area and biomarker splits) and Citeline 2014 to 2023 (LOA 6.7%; Phases I to III 47%, 28%, 55%). Provider methods differ; the playbook shows both.
- FDA: PDUFA VII and VIII cohort goals (10 or 6 months after the 60-day filing date for NME and original BLA), complete response letter evidence from openFDA reporting and three analyses.
- US negotiation programme: cycle 3 timeline (ends 31 Oct 2026; prices from 1 Jan 2028), orphan exclusion change, generic determination rule.
- Most-favored-nation agreements: 26 manufacturers by 31 Aug 2026; Medicaid extension 18 Sep 2026; terms not public.
- Generic price erosion by number of producers (FDA 2019) and biosimilar uptake (adalimumab, ustekinumab; company-reported).
- EU pharma package: Council position 28 Sep 2026, Parliament vote pending, not yet law.

## Corrections to earlier packages (act on these)
- The earlier CI Brief Analyst playbook describes EU protection only as 8+2(+1). The reform (8 years data protection plus 1 year market protection with extensions, 11-year cap) is not yet law, but add the status note.
- The earlier playbook gave 458 CRL records as of 13 Aug 2026; a later secondary count shows about 459 (446 typed as CRL). Immaterial, but update.
- The Phase 3 and Phase 4 forecasting agents (13 to 20) depend on shared files and a router. These six replace agents 13 to 17 as independent versions.

## Setup (per agent)
1. Create the agent in Copilot Studio and paste the Description from CONFIG_AND_TESTS.
2. Paste INSTRUCTIONS.
3. Upload the one KNOWLEDGE file. If .md is rejected, save as .docx or .txt.
4. Apply settings. Add web search on the listed official domains if your tenant allows.
5. Run the 18 tests three times each. All trap tests must pass all three runs. Check golden numbers against the playbook.
6. Publish to the intended group only.
Suggested order: 1, 6, 2, 3, 5, 4.

## Not done, and caveats
- No agent was run in Copilot Studio. Tests are written, not executed.
- Playbook facts come from agency documents and secondary sources (law firms, trade press, company-reported market reports). All are marked verify. Review every 90 days.
- Benchmarks are not forecasts. Provider datasets disagree; the agents state the dataset.
- Statutory structures for US small molecules, biologics, Medicaid, and Part D are from general knowledge and marked verify; they were not re-read from statute in this session.
- Not trading, legal, or medical advice.
