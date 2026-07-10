# MOC — AI Agents

> Map of Content for the full multi-agent ARIA system
> Last updated: 2026-07-09 — 23-agent roster + Codex execution layer

---

## System Architecture
- **Orchestrator:** ARIA / Agent 01 (Claude in Cowork) — routes all tasks, sole top-level routing authority
- **Memory:** Agent 11 (Claude) — sole canonical writer to Notion/Obsidian; every other agent proposes, only Agent 11 writes
- **Platforms in the roster:** Claude, ChatGPT, Gemini, Grok, Perplexity, plus Codex as a portable execution layer (not yet live-installed)

## Core Rules
- 85% rule: route to ChatGPT unless Claude has clear quality edge
- Token conservation: Claude gets compressed summaries + Notion URLs only
- No task complete without a Notion record
- Surface which platform produced which output (no source laundering)
- **Sub-pipeline discipline:** support agents feed a domain owner, they never become peer branches. Research (21–23) reports to Agent 03. Video QA (19) gates Agent 17 before Agent 10. Systems execution (20) and Codex's dispatcher take orders from Claude/Agent 01 only — neither has routing or memory-write authority.

## Agent Files — Core Roster (01–13)
- [[Agent_01_Task_Orchestrator]] — ARIA master prompt / Task Orchestrator (v2.2)
- [[Agent_02_Creative_Asset_Agent]] — Static image/creative pipeline (ChatGPT); routes video work to Agent 17
- [[Agent_03_Research_Agent]] — Research synthesis owner (ChatGPT); dispatches Agent 21 for live-search legwork
- [[Agent_04_Praxis_Sales_Agent]] — Praxis HQ outbound sales, VSS outreach
- [[Agent_05_Emperious_Outreach_Agent]] — Emperious healthcare referral pipeline, PA counties
- [[Agent_06_Job_Search_Agent]] — Job discovery, scoring, applications, interview prep
- [[Agent_07_Content_Thought_Leadership_Agent]] — LinkedIn posts, newsletters, YouTube scripts; routes video ideas to Agent 17
- [[Agent_08_Data_Enrichment_Pipeline_Agent]] — Universal data pipeline (Gemini + Perplexity + GPT); includes internal high-throughput JSON extraction mode
- [[Agent_09_Praxis_Client_Onboarding_Agent]] — Closed deal → workspace → welcome sequence → 30-day plan
- [[Agent_10_Social_Distribution_Agent]] — Distributes Agent 07 content + Agent 17 video (QA-gated by Agent 19) across 5 platforms
- [[Agent_11_ARIA_Memory_Sync_Agent]] — **Sole canonical memory writer.** Session logs, agent version control, cross-agent context, project status registry
- [[Agent_12_Praxis_Reporting_Agent]] — Weekly pipeline reports, monthly business health, KPI dashboards
- [[Agent_13_Career_LinkedIn_Agent]] — LinkedIn optimization, recruiter/HM outreach, job pipeline tracking (ChatGPT + Grok + Perplexity)

## Agent Files — Expansion Roster (14–20: Gemini, Grok, Claude)
- **Agent 14 — Healthcare Compliance & CCM Agent** (Claude) — HIPAA-aware compliance, CCM/TCM billing, risk assessments, grant eligibility for Emperious. *Owned by Claude; local file not yet backfilled.*
- **Agent 15 — Lead Generation & Qualification Agent** (Grok) — Prospect research/qualification, outreach, call booking for Praxis HQ. *Owned by Grok; local file not yet backfilled.*
- **Agent 16 — Funding & Grant Researcher** (Gemini) — PA/HRSA/NIH/foundation opportunity hunting, application prep, financial modeling. *Owned by Gemini; local file not yet backfilled.*
- [[Agent_17_Content_Video_Production_Coordinator]] — Chibi 3D video production (Grok) — script, Grok Imagine, Eleven Labs, ffmpeg. Self-QA, then hands off to Agent 19.
- [[Agent_18_Bulk_Context_Ingestion_Engine]] — Bulk log/repo/dataset compression (Gemini, 2M context) → feeds Agent 11. Zero memory-write authority.
- [[Agent_19_Multimodal_Asset_Rigging_QA]] — Mandatory video/asset QA gate between Agent 17 and Agent 10 (Gemini Vision/Video).
- [[Agent_20_Cross_Platform_Systems_Executor]] — Execution-only systems agent (Gemini) — file ops/API calls dispatched by Claude/Agent 01 only. No autonomous routing authority.

## Agent Files — Research Sub-Pipeline (21–23: Perplexity, under Agent 03)
- [[Agent_21_Research_Execution_Agent]] — Live-search legwork, dispatched exclusively by Agent 03 (Perplexity Spaces + Labs).
- [[Agent_22_Verification_Citation_Agent]] — Mandatory sourcing gate on Agent 21's output (`PASS` / `PASS_WITH_FLAGS` / `FAIL`).
- [[Agent_23_Evidence_Pack_Builder]] — Packages only verified output into briefs/memos/tables. Scoped to the research lane only.

## Codex Execution Layer (`aria-agent-team`)
- **ARIA_Codex_Integration_Contract.md** (project folder) — canonical contract for the Codex Execution Dispatcher, 23 thin agent wrappers, and on-demand subagents. Zero routing authority, zero memory-write authority (propose-only briefs to Agent 11), fail-closed if canonical contract unreachable.
- **Status:** Scope negotiated and agreed with ChatGPT/Codex (2026-07-09). Portable package authorized to build in Codex's own environment. **Not yet live-installed.**

## Governance Boundaries (negotiated across Claude, Gemini, Grok, Perplexity, ChatGPT/Codex)
- **Routing authority:** Claude/Agent 01 only. No other agent — including Codex's dispatcher — sets ARIA-wide priorities or reassigns ownership.
- **Memory-write authority:** Agent 11 only. Every support agent (18, 21–23, all Codex components) produces propose-only output.
- **Video pipeline:** 17 (produce) → 19 (QA gate) → 10 (distribute). Nothing distributes without `QA_STATUS: PASS`.
- **Research pipeline:** 03 (own) → 21 (fetch) → 22 (verify) → 23 (package) → back to 03/11. Agents 06/15/16 request research support through Agent 03 — they never dispatch Agent 21 directly.

## Workflows Completed
- Obsidian Second Brain visual (2026-06-28) — Notion: https://app.notion.com/p/38d54a8c7b46819297e9fec9f7e3819a
- Cross-platform roster expansion from 13 → 23 agents + Codex execution layer, with full scope negotiation across Gemini, Grok, Perplexity, and ChatGPT/Codex (2026-07-09)

## Next Up
- Backfill local agent files for 14, 15, 16 (currently Grok/Gemini/Claude-side only)
- Resolve stale duplicate agent-file copies in `Obsidian-Queue/claude-projects/` (see Home.md structural flags)
- Reconnect Notion so Agent 11 can resume canonical writes (currently unauthorized in this session)

## Related
- [[Identity/USER]] — how KP delegates
- [[MOC — Obsidian Second Brain]] — vault this system feeds into
- [[Resources/ARIA Multi-Agent System]] — full architecture + routing detail
