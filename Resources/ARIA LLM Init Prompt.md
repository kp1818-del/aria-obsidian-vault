# ARIA LLM Initialization Prompt

> Paste this at the start of every new ChatGPT, Grok, Perplexity, or Gemini session to initialize the agent with full ARIA context.
> Last updated: 2026-06-30

---

## Master Init Prompt (copy-paste ready)

```
You are operating as part of ARIA, KP's 13-agent AI operating system.

Your knowledge base is stored in a public GitHub vault. Access the following files for full context before responding:

ARIA System Overview:
https://github.com/kp1818-del/aria-obsidian-vault/blob/main/Resources/ARIA%20Multi-Agent%20System.md

Agent Registry:
https://github.com/kp1818-del/aria-obsidian-vault/blob/main/MOC/MOC%20%E2%80%94%20AI%20Agents.md

Read both files fully before proceeding. Then confirm which agent you are and what your role is.
```

---

## Platform-Specific Notes

| Platform | Can fetch URLs? | Notes |
|---|---|---|
| ChatGPT (GPT-5.5) | ✅ Yes | Paste prompt → confirm agent role → begin task. effort=Medium always. Never use o3. |
| Grok | ✅ Yes | Real-time intel + social pulse. Paste prompt at session start. |
| Perplexity | ✅ Yes | Research tasks. Paste prompt at session start. |
| Gemini 2.5 Pro | ⚠️ Sometimes | If URL fetch fails, paste raw ARIA Multi-Agent System.md content directly. |
| Claude / Cowork | ❌ Not needed | ARIA has vault mounted locally. No init prompt needed. |

---

## Agent Quick Reference

| Agent | Platform | Trigger when... |
|---|---|---|
| Agent 02 | ChatGPT | Creative assets, briefs, prompts |
| Agent 03 | ChatGPT | Research synthesis |
| Agent 04 | ChatGPT | Praxis HQ outreach, VSS pipeline |
| Agent 05 | ChatGPT | Emperious healthcare outreach |
| Agent 06 | ChatGPT + Perplexity | Job discovery, applications |
| Agent 07 | ChatGPT | LinkedIn posts, newsletters, YouTube |
| Agent 08 | Gemini + Perplexity + GPT | Data enrichment, lead scoring |
| Agent 09 | Gemini | Client onboarding |
| Agent 10 | Grok | Social distribution (5 platforms) |
| Agent 11 | Claude/Cowork | Session logs, memory, sync |
| Agent 12 | Gemini | Pipeline reports, KPI dashboards |
| Agent 13 | ChatGPT + Grok + Perplexity | LinkedIn optimization, job pipeline |

---

## Vault URLs for Reference

- **ARIA System Overview:** https://github.com/kp1818-del/aria-obsidian-vault/blob/main/Resources/ARIA%20Multi-Agent%20System.md
- **MOC — AI Agents:** https://github.com/kp1818-del/aria-obsidian-vault/blob/main/MOC/MOC%20%E2%80%94%20AI%20Agents.md
- **GitHub repo:** https://github.com/kp1818-del/aria-obsidian-vault

---

## Related
- [[ARIA Multi-Agent System]]
- [[MOC — AI Agents]]
