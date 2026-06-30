# MOC — AI Agents

> Map of Content for the full multi-agent ARIA system

---

## System Architecture
- **Orchestrator:** ARIA (Claude in Cowork) — routes all tasks
- **Agent 02:** Creative Asset Agent (ChatGPT GPT-4o)
- **Agent 03:** Research Agent (ChatGPT GPT-4o)
- **Specialist:** Perplexity — quick web research
- **Specialist:** Gemini Deep Research — comprehensive research
- **Specialist:** Grok Build / Aurora — image + video generation
- **Specialist:** NotebookLM — knowledge base synthesis

## Core Rules
- 85% rule: route to ChatGPT unless Claude has clear quality edge
- Token conservation: Claude gets compressed summaries + Notion URLs only
- No task complete without a Notion record
- Surface which platform produced which output (no source laundering)

## Agent Files
- [[Agent_01_Task_Orchestrator]] — ARIA master prompt (v2.1)
- [[Agent_02_Creative_Asset_Agent]] — ChatGPT creative agent
- [[Agent_03_Research_Agent]] — ChatGPT research agent
- [[Agent_04_Praxis_Sales_Agent]] — Praxis HQ outbound sales, VSS outreach
- [[Agent_05_Emperious_Outreach_Agent]] — Emperious healthcare referral pipeline, PA counties
- [[Agent_06_Job_Search_Agent]] — Job discovery, scoring, applications, interview prep
- [[Agent_07_Content_Thought_Leadership_Agent]] — LinkedIn posts, newsletters, YouTube scripts from daily ARIA work
- [[Agent_08_Data_Enrichment_Pipeline_Agent]] — Universal data pipeline: any book of business → enriched, scored, segmented (Gemini + Perplexity + GPT)
- [[Agent_09_Praxis_Client_Onboarding_Agent]] — Closed deal → Notion workspace → welcome sequence → kickoff prep → 30-day plan
- [[Agent_10_Social_Distribution_Agent]] — Agent 07 content → LinkedIn, Instagram, Facebook, TikTok, YouTube
- [[Agent_11_ARIA_Memory_Sync_Agent]] — Session logs, agent version control, cross-agent context, project status registry
- [[Agent_12_Praxis_Reporting_Agent]] — Weekly pipeline reports, monthly business health, client health, KPI dashboards
- [[Agent_13_Career_LinkedIn_Agent]] — LinkedIn profile optimization, recruiter/HM outreach, job pipeline tracking, interview prep, salary negotiation (ChatGPT + Grok + Perplexity)

## Workflows Completed
- Obsidian Second Brain visual (2026-06-28) — Notion: https://app.notion.com/p/38d54a8c7b46819297e9fec9f7e3819a

## Next Up
- Test Agent 13 end-to-end
- Agent 14+ TBD based on next phase of growth

## Related
- [[Identity/USER]] — how KP delegates
- [[MOC — Obsidian Second Brain]] — vault this system feeds into
