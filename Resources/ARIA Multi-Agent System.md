# ARIA Multi-Agent System

> Autonomous Routing & Intelligence Agent — KP's personal AI operating system.
> Built in Cowork (Claude). Routes tasks across 23 specialized agents, 5 platforms, and a Codex execution layer.
> Last updated: 2026-07-09

---

## Architecture

```
ARIA / Agent 01 (Cowork/Claude) ← Master Orchestrator (v2.2) — sole routing authority
├── Agent 02 (ChatGPT GPT-5.5) ← Creative Asset Pipeline → routes video work to Agent 17
├── Agent 03 (ChatGPT GPT-5.5) ← Research Engine — owns 21-23 sub-pipeline
│   ├── Agent 21 (Perplexity) ← Research Execution — dispatched by Agent 03 only
│   ├── Agent 22 (Perplexity) ← Verification & Citation — mandatory gate on Agent 21
│   └── Agent 23 (Perplexity) ← Evidence Pack Builder — packages 22-approved output only
├── Agent 04 (ChatGPT GPT-5.5) ← Praxis HQ Sales & Outreach
├── Agent 05 (ChatGPT GPT-5.5) ← Emperious Healthcare Outreach
├── Agent 06 (ChatGPT + Perplexity) ← Job Search & Apply — requests research via Agent 03
├── Agent 07 (ChatGPT GPT-5.5) ← Content & Thought Leadership → routes video ideas to Agent 17
├── Agent 08 (Gemini + Perplexity + GPT) ← Data Enrichment Pipeline (incl. high-throughput JSON mode)
├── Agent 09 (Gemini 2.5 Pro) ← Praxis Client Onboarding
├── Agent 10 (Grok) ← Social Distribution — video requires Agent 19 QA pass
├── Agent 11 (Cowork/Claude) ← ARIA Memory & Sync — SOLE canonical Notion/Obsidian writer
├── Agent 12 (Gemini 2.5 Pro) ← Praxis Reporting & Dashboards
├── Agent 13 (ChatGPT + Grok + Perplexity) ← Career & LinkedIn
├── Agent 14 (Claude) ← Healthcare Compliance & CCM — *not yet backfilled locally*
├── Agent 15 (Grok) ← Lead Generation & Qualification — requests research via Agent 03
├── Agent 16 (Gemini) ← Funding & Grant Researcher — requests research via Agent 03
├── Agent 17 (Grok) ← Content & Video Production Coordinator — hands off to Agent 19
├── Agent 18 (Gemini, 2M context) ← Bulk Context Ingestion — feeds Agent 11 only
├── Agent 19 (Gemini Vision/Video) ← Multimodal Asset QA — gates Agent 17 → Agent 10
├── Agent 20 (Gemini function calling) ← Cross-Platform Systems Executor — execution-only
├── Codex Execution Dispatcher ← execution sequencing for Codex-side wrappers, no routing authority
│   └── 23 thin agent wrappers (Codex) ← reference-only, point to canonical .md contracts
├── NotebookLM ← Knowledge base synthesis
├── Notion ← Operational database + output storage
└── Obsidian ← Master knowledge vault (source of truth) — written only via Agent 11
```

---

## Delegate-First Rule (Non-Negotiable)

Before using Cowork, check:
1. Can GPT / Agent 02–13 do this? → YES → route there
2. Can Codex handle file writing/scripting? → YES → route there
3. Can Grok Build handle assets? → YES → route there
4. Can Gemini/Perplexity handle research? → YES → route there
5. No viable alternative? → ONLY THEN use Cowork

**Cowork's only job:** Decompose, route, review, resolve conflicts, store memory.

---

## Platform Routing

| Task Type | Platform |
|---|---|
| Orchestration, routing, memory | CLAUDE (Cowork) |
| Content drafts, copy, templates | GPT / Agent 07 |
| Research (quick lookup, company/person) | Perplexity |
| Research (comprehensive report) | Gemini Deep Research |
| Images + videos | Grok Build (Aurora) |
| Long documents (20+ pages) | Gemini |
| Multi-source knowledge base | NotebookLM |
| File writing, scripts, data processing | Codex |
| Social/X pulse, trending, real-time job intel | Grok |
| Data enrichment, lead lists, VSS scoring | Agent 08 (Gemini) |
| Client onboarding, Google Doc workspace | Agent 09 (Gemini) |
| Social distribution — all 5 platforms | Agent 10 (Grok) |
| Session logs, agent sync, system memory | Agent 11 (Claude) |
| Weekly pipeline, KPI reports | Agent 12 (Gemini) |
| LinkedIn optimization, job search, outreach | Agent 13 (ChatGPT + Grok + Perplexity) |
| Store all outputs | Notion + Obsidian |

---

## 85% Rule
> Before routing to Claude, ask: *"Would GPT produce output that is 85%+ as good?"*
> If YES → GPT. If NO → Claude (note why).

---

## Token Conservation
- Claude gets compressed summaries (<300 words), not raw dumps
- Store intermediate outputs in Notion, reference by URL
- Run parallel sub-tasks across platforms simultaneously

---

## Agent Registry (v3.0 — 23 agents + Codex execution layer)

| Agent | File | Platform | Owns |
|---|---|---|---|
| Agent 01 — ARIA Orchestrator | Agent_01_Task_Orchestrator.md | Cowork/Claude | Routing, memory, decomposition — sole routing authority |
| Agent 02 — Creative Asset | Agent_02_Creative_Asset_Agent.md | ChatGPT GPT-5.5 | Brief → creative → assets; routes video to Agent 17 |
| Agent 03 — Research | Agent_03_Research_Agent.md | ChatGPT GPT-5.5 | Research synthesis; owns 21–23 sub-pipeline |
| Agent 04 — Praxis Sales | Agent_04_Praxis_Sales_Agent.md | ChatGPT GPT-5.5 | VSS outreach, cold email, proposals |
| Agent 05 — Emperious Outreach | Agent_05_Emperious_Outreach_Agent.md | ChatGPT GPT-5.5 | PA county referral relationships |
| Agent 06 — Job Search | Agent_06_Job_Search_Agent.md | ChatGPT + Perplexity | Job discovery, scoring, applications |
| Agent 07 — Content & Thought Leadership | Agent_07_Content_Thought_Leadership_Agent.md | ChatGPT GPT-5.5 | LinkedIn posts, newsletters, YouTube; routes video to Agent 17 |
| Agent 08 — Data Enrichment | Agent_08_Data_Enrichment_Pipeline_Agent.md | Gemini + Perplexity + GPT | VSS pipeline, lead enrichment, scoring, high-throughput JSON mode |
| Agent 09 — Client Onboarding | Agent_09_Praxis_Client_Onboarding_Agent.md | Gemini 2.5 Pro | Closed deal → onboarding → 30-day plan |
| Agent 10 — Social Distribution | Agent_10_Social_Distribution_Agent.md | Grok (primary) | Agent 07/17 content → 5 platforms; requires Agent 19 QA pass on video |
| Agent 11 — Memory & Sync | Agent_11_ARIA_Memory_Sync_Agent.md | Cowork/Claude | **Sole canonical Notion/Obsidian writer** |
| Agent 12 — Reporting | Agent_12_Praxis_Reporting_Agent.md | Gemini 2.5 Pro | Pipeline reports, KPIs, dashboards |
| Agent 13 — Career & LinkedIn | Agent_13_Career_LinkedIn_Agent.md | ChatGPT + Grok + Perplexity | LinkedIn optimization, job pipeline, outreach |
| Agent 14 — Healthcare Compliance & CCM | *not yet backfilled locally* | Claude | HIPAA compliance, CCM/TCM billing, Emperious grant eligibility |
| Agent 15 — Lead Generation & Qualification | *not yet backfilled locally* | Grok | Prospect research/qualification, call booking for Praxis HQ |
| Agent 16 — Funding & Grant Researcher | *not yet backfilled locally* | Gemini | PA/HRSA/NIH/foundation opportunity hunting |
| Agent 17 — Content & Video Production | Agent_17_Content_Video_Production_Coordinator.md | Grok | Chibi 3D video production; hands off to Agent 19 |
| Agent 18 — Bulk Context Ingestion | Agent_18_Bulk_Context_Ingestion_Engine.md | Gemini (2M context) | Compression engine feeding Agent 11 only |
| Agent 19 — Multimodal Asset QA | Agent_19_Multimodal_Asset_Rigging_QA.md | Gemini Vision/Video | Mandatory QA gate, Agent 17 → Agent 10 |
| Agent 20 — Systems Executor | Agent_20_Cross_Platform_Systems_Executor.md | Gemini (function calling) | Execution-only file/API ops, no routing authority |
| Agent 21 — Research Execution | Agent_21_Research_Execution_Agent.md | Perplexity | Live-search legwork, dispatched by Agent 03 only |
| Agent 22 — Verification & Citation | Agent_22_Verification_Citation_Agent.md | Perplexity | Mandatory sourcing gate on Agent 21 output |
| Agent 23 — Evidence Pack Builder | Agent_23_Evidence_Pack_Builder.md | Perplexity | Packages verified research only |
| Codex Execution Dispatcher + 23 wrappers | ARIA_Codex_Integration_Contract.md | Codex (portable, not live) | Execution sequencing only; propose-only memory; no routing authority |

**Location:** ~/Documents/Claude/Projects/AI Learning Hub/
**⚠️ Model rule:** Never use o3 on any agent. Always confirm GPT-5.5, effort = Medium.
**⚠️ Governance rule:** Only Agent 01 sets routing/priority. Only Agent 11 writes canonical memory. Every other new agent added to ARIA — regardless of platform — inherits these two limits by default and must be explicitly negotiated if broader authority is ever requested.

---

## Outreach Rules

- All Praxis HQ outbound emails send FROM: **systems@praxishq.co** (never kp1818@gmail.com)
- Applies to: Agent 04, Agent 05, Agent 09, Agent 13

---

## Active Projects (as of 2026-06-29)

### VSS Provider Enrichment (Agent 08)
- Total records: 7,799 healthcare providers
- Rows enriched: ~875 (rows 1–875 complete)
- Next batch: Row 876+
- Outreach-ready (Score 4–5): ~60 records
- Priority Rank column (col M) active — top-to-bottom outreach order
- 824 rows have text notes in col K needing numeric score cleanup

### Praxis HQ Outreach — Batch 1 (Agent 04)
- 3 emails drafted and approved, sender: systems@praxishq.co
- Send schedule: Tue / Wed / Thu (approved, pending KP send)

### LinkedIn Optimization (Agent 13) — COMPLETED 2026-06-29
- Headline rewritten: Builder of ARIA framing ✅
- About section rewritten: operator-to-AI-builder arc ✅
- Praxis HQ + Emperious experience bullets rewritten ✅
- 15 recruiter-optimized skills added ✅

### Job Pipeline (Agent 13) — ACTIVE
- Tennr (AI Operations Lead) — outreach to Tyler Johnson, CTO → 2026-06-29 8:00am
- Develop Health (Head of AI) — outreach to Mel van Londen, CEO → 2026-06-29 8:15am
- Follow-up trigger: 2026-07-04 for both
- Notion pipeline: https://app.notion.com/p/38e54a8c7b4681619b95f5a9f8c85c2d

---

## Completed Workflows

| Date | Workflow | Result |
|---|---|---|
| 2026-06-28 | Obsidian Second Brain visual — Agent 03 → Agent 02 → Grok Build | ✅ Notion: https://app.notion.com/p/38d54a8c7b46819297e9fec9f7e3819a |
| 2026-06-28 | Agents 09–12 built and tested | ✅ All 4 agents passing |
| 2026-06-28 | VSS scoring sweep rows 1–770 | ✅ 48 rows scored, 19 outreach-ready |
| 2026-06-28 | Priority ranking column (col M) added | ✅ 871 rows ranked |
| 2026-06-28 | Agent 13 — Career & LinkedIn Agent built | ✅ v1.0 live |
| 2026-06-29 | LinkedIn profile full optimization | ✅ Headline + About + Experience + Skills |
| 2026-06-29 | Job pipeline — Tennr + Develop Health | ✅ Outreach scheduled 8am |
| 2026-07-09 | Grok proposal reviewed — Agents 14–17 (Healthcare Compliance, Lead Gen, Funding, Video Production) integrated into roster | ✅ Numbering conflict (video agent mislabeled 14) caught and corrected to 17 |
| 2026-07-09 | Gemini proposal negotiated — Agents 18–20 (Context Ingestion, Multimodal QA, Systems Executor) | ✅ Scope trimmed from 4 proposed agents to 3; JSON extraction folded into Agent 08 instead of standalone Agent 22 |
| 2026-07-09 | Perplexity proposal negotiated — Agents 21–23 (Research Execution, Verification, Evidence Packaging) | ✅ Formalized as sub-pipeline under Agent 03, not peer branch; gate labels PASS/PASS_WITH_FLAGS/FAIL adopted |
| 2026-07-09 | ChatGPT/Codex `aria-agent-team` plugin scope negotiated | ✅ Routing renamed to execution-only "Codex Execution Dispatcher"; memory-write dropped for propose-only briefs; 23 wrappers scoped as thin references, not duplicate logic |
| 2026-07-09 | Agent 11 contract hardened | ✅ Explicit sole-canonical-writer clause added, naming every support agent (18, 21–23, all Codex components) as having zero write authority |

---

## Security Rules
- Never send PII, passwords, financials to external LLMs without confirmation
- Always surface which platform produced which output (no source laundering)
- Flag conflicting outputs explicitly — never pick one silently
- No task complete until Notion + Obsidian records exist

## Related
- [[MOC — AI Agents]]
- [[MOC — Business]]
- [[Praxis HQ]]
- [[Emperious Healthcare]]
- [[VSS Provider Enrichment]]
