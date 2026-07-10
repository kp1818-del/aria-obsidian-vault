# 🏠 Home — Second Brain Dashboard

> *Last updated: 2026-07-10*

---

## 🧠 Identity
- [[Identity/USER|Who I Am]] — how KP works
- [[Identity/SOUL|Why I Do This]] — core drive and mission
- [[Identity/IDENTITY|Knowledge Persona]] — how I think and learn

---

## 🗺️ Maps of Content
- [[MOC/MOC — AI Agents|AI Agents MOC]] — full multi-agent system
- [[MOC/MOC — Obsidian Second Brain|Obsidian MOC]] — vault tips and setup
- [[MOC/MOC — Business|Business MOC]] — Praxis HQ + Emperious
- [[MOC/MOC — Learning|Learning MOC]] — videos, tips, prompts

---

## 📥 Inbox
*Drop new notes here — process weekly*

---

## 📅 Daily Notes
- [[Daily/2026-07-09|Today]]
- [[Daily/2026-06-29|2026-06-29]]
- [[Daily/2026-06-28|2026-06-28]]

---

## 📁 Projects
- [[Projects/Praxis HQ|Praxis HQ]] — Local business marketing agency
- [[Projects/Emperious Healthcare|Emperious Healthcare]] — PA home health + adult day care
- [[Projects/VSS Provider Enrichment|VSS Provider Enrichment]] — 7,799 healthcare provider records (~10% done)

## 📚 Resources
- [[Resources/ARIA Multi-Agent System|ARIA System]] — Full agent architecture + routing rules
- [[Resources/AI Business Summit — Key Prompts|AI Business Summit Prompts]] — Reusable AI prompts

## 📐 Areas
- [[Areas/Brand Positioning|Brand Positioning]] — Praxis.ai vs Axiom.ai decision

## 🔥 Active Projects
- ARIA 23-Agent Multi-Platform System (Claude, ChatGPT, Gemini, Grok, Perplexity, + Codex execution layer)
- Praxis HQ Marketing Automation
- Emperious Healthcare PA Market Entry
- VSS Provider Enrichment (resume from row 876)

## ✅ Resolved 2026-07-10
- **Duplicate agent files** — the stale `Obsidian-Queue/claude-projects/` folder (frozen at Agent 12, plus a confusing nested copy of the whole vault tree) was archived to `_Archive/claude-projects_ARCHIVED_2026-07-10/` — not deleted, just moved out of the way. Root cause fixed too: `aria_obsidian_sync.py`'s `sync_claude_projects()` was sweeping vault files into the queue as a side effect; it now explicitly skips `Obsidian_Vault_Files/` and `_Archive/`, so this won't recur on the next sync run.
- **Sync script Downloads gap** — `aria_obsidian_sync.py` only checked `~/Downloads/LLM-Exports/`, which resolves to a sandbox home directory (not KP's Mac) when run from Cowork. It now checks a new `LLM-Exports-Inbox/` folder inside AI Learning Hub first (reachable from both Cowork and locally), then falls back to the original Downloads path for local runs. Drop LLM exports in either place going forward.
- **Agents 14, 15, 16 backfilled** — `Agent_14_Healthcare_Compliance_CCM_Agent.md`, `Agent_15_Lead_Generation_Qualification_Agent.md`, and `Agent_16_Funding_Grant_Researcher.md` now exist as full local contracts matching the standard ARIA agent format, including the Agent 03 research-dispatch pattern and a new eligibility-gate relationship between Agent 16 and Agent 14 for Emperious-related funding opportunities.

## ⚠️ Still Needs KP Action
- **Notion connector not authorized in Cowork session.** This requires your own login — Cowork can't complete OAuth on its own. Go to claude.ai → Settings → Connectors, find Notion, and reauthorize. Once done, Agent 11 can resume writing canonical Notion records alongside Obsidian.
- These vault files were pushed to GitHub via direct upload (not the local obsidian-git plugin) — pull/sync in your Obsidian app to bring today's changes down locally.

---

## ⚡ Quick Capture
*For fleeting ideas — move to proper note within 48h*
