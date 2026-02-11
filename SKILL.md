---
name: openclaw-mentor
description: This skill should be used when the user asks to "ask about OpenClaw", "query OpenClaw docs", "how does OpenClaw work", "OpenClaw help", "openclaw mentor", or needs guidance on OpenClaw configuration, CLI commands, channels, agents, skills, memory, deployment, or troubleshooting.
version: 0.1.0
tools: Read, WebSearch
argument-hint: <OpenClaw question in any language>
disable-model-invocation: true
---

# OpenClaw Mentor

An AI mentor for OpenClaw — the self-hosted multi-channel AI agent gateway. Instead of containing all knowledge internally, this skill uses the **smart-search** skill to query the `openclaw/openclaw` repository documentation on demand.

## Core Principle

When answering OpenClaw questions, **always query live documentation first** via the smart-search skill rather than relying on potentially outdated knowledge. OpenClaw evolves rapidly; live documentation is the source of truth.

## How to Answer Questions

### Step 1: Identify the Topic Area

Map the user's question to one of OpenClaw's main domains:

| Domain | Keywords | Wiki Sections |
|--------|----------|---------------|
| Installation | install, onboard, setup, daemon | 2.x |
| Gateway | gateway, port, WebSocket, service | 3.x |
| Configuration | config, openclaw.json, JSON5, settings | 4.x |
| Agents | agent, workspace, model, session, sandbox | 5.x |
| Tools & Skills | tool, skill, exec, read, browser, cron | 6.x |
| Memory | memory, MEMORY.md, daily notes, indexing | 7.x |
| Channels | WhatsApp, Telegram, Discord, Signal, iMessage, Slack | 8.x |
| Commands | slash command, /model, /new, /reset, directives | 9.x |
| Plugins | plugin, extension, custom plugin | 10.x |
| Nodes | node, pairing, macOS app, iOS, Android | 11.x |
| CLI | openclaw CLI, subcommand, flags | 12.x |
| Deployment | deploy, VPS, cloud, Tailscale, Ansible | 13.x |
| Troubleshooting | doctor, health, error, fix, debug | 14.x |
| Development | architecture, protocol, build, CI/CD | 15.x |

### Step 2: Query Documentation

Search for OpenClaw information using these tools directly:

1. **DeepWiki (preferred for OpenClaw)**: Call `mcp__deepwiki__ask_question` with `repoName: "openclaw/openclaw"` and your question. This gives architecture-level understanding of the OpenClaw codebase and docs.
2. **WebSearch (fallback)**: Use `WebSearch` for general queries, recent changes, or when DeepWiki lacks coverage. Include "OpenClaw" in the query for better results.

**Query writing tips:**
- Be specific: "How to configure WhatsApp channel with group message filtering in OpenClaw" instead of "WhatsApp setup"
- Ask for examples: "Show example openclaw.json configuration for multi-agent setup with model failover"
- Request step-by-step: "Step-by-step guide to deploy OpenClaw on a VPS with Tailscale"
- Include context: "How to troubleshoot OpenClaw Gateway connection timeout on port 18789"
- Always include "OpenClaw" in the query for better search results

### Step 3: Synthesize and Respond

After receiving search results:

1. Extract the relevant information
2. Adapt the answer to the user's specific context
3. Include code examples (config snippets, CLI commands) when applicable
4. Mention related topics the user might want to explore
5. Respond in the user's language

## Common Query Patterns

### Configuration Questions
```
"Show me the full openclaw.json schema for [agents|channels|models|skills|session|gateway]"
"How to configure [feature] in openclaw.json with examples"
```

### CLI Questions
```
"What are all the flags for openclaw [subcommand]?"
"How to use openclaw [command] for [specific task]?"
```

### Channel Setup
```
"Step-by-step setup for [WhatsApp|Telegram|Discord|Signal|Slack|iMessage] channel"
"How to configure message filtering for [channel] groups"
```

### Troubleshooting
```
"How to diagnose [specific error or symptom] in OpenClaw"
"What does openclaw doctor check and how to fix common issues"
```

## OpenClaw Quick Reference

A minimal reference to orient queries — not a substitute for querying live documentation via smart-search.

### Architecture
- **Gateway**: Always-on Node.js process, WebSocket on `ws://127.0.0.1:18789`
- **Agents**: Isolated AI runtimes with workspace, sessions, model config, tool policies
- **Channels**: Messaging platform integrations (WhatsApp, Telegram, Discord, etc.)
- **Sessions**: Conversation state stored as JSONL, keyed by `agent:ID:channel:peer`
- **Memory**: Daily notes (`memory/YYYY-MM-DD.md`) + curated `MEMORY.md`
- **Nodes**: Companion apps (macOS/iOS/Android) exposing device capabilities

### Config File
- Path: `~/.openclaw/openclaw.json` (JSON5 format)
- Precedence: Env vars > CLI flags > Config file > Defaults
- Top-level keys: `agents`, `channels`, `models`, `skills`, `session`, `gateway`

### Key CLI Commands
- `openclaw onboard` — Interactive setup wizard
- `openclaw gateway` — Manage Gateway (run/status/install/stop/restart)
- `openclaw channels` — Manage channels (list/add/remove/login/logs)
- `openclaw agent` — Interact with agents
- `openclaw models` — Check model provider auth and availability
- `openclaw doctor` — Diagnose and repair common issues
- `openclaw status` — Quick health snapshot

### Skills System
- Locations: workspace (`~/.openclaw/workspace/skills/`), managed (`~/.openclaw/skills/`), bundled
- Config: `skills` section in `openclaw.json`
- Each skill: directory with `SKILL.md` (YAML frontmatter + Markdown instructions)

## Additional Resources

### Reference Files

For detailed topic-specific query templates:
- **`references/query-templates.md`** - Pre-built query templates organized by topic for smart-search
