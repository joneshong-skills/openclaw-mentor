[English](README.md) | [繁體中文](README.zh.md)

# openclaw-mentor

A Claude Code skill that acts as an AI mentor for [OpenClaw](https://github.com/openclaw/openclaw) — the self-hosted multi-channel AI agent gateway.

## Description

This skill should be used when the user asks to "ask about OpenClaw", "query OpenClaw docs", "how does OpenClaw work", "OpenClaw help", "openclaw mentor", or needs guidance on OpenClaw configuration, CLI commands, channels, agents, skills, memory, deployment, or troubleshooting.

## What It Does

Instead of relying on static, potentially outdated knowledge, this skill uses the **smart-search** skill to query the `openclaw/openclaw` repository documentation on demand. It covers all major OpenClaw domains:

- **Installation & Onboarding** — setup wizard, daemon management
- **Gateway & Configuration** — `openclaw.json` (JSON5), WebSocket service
- **Agents & Sessions** — workspaces, models, sandboxed runtimes
- **Tools & Skills** — built-in tools, custom skills, cron jobs
- **Memory** — daily notes, `MEMORY.md`, indexing
- **Channels** — WhatsApp, Telegram, Discord, Signal, iMessage, Slack
- **CLI Commands** — all subcommands and flags
- **Deployment** — VPS, cloud, Tailscale, Ansible
- **Troubleshooting** — `openclaw doctor`, diagnostics

## Installation

Install the skill into Claude Code:

```bash
claude skill add joneshong-skills/openclaw-mentor
```

### Prerequisites

- The **smart-search** skill installed (`~/.claude/skills/smart-search/`)

## Usage

Once installed, simply ask Claude about anything OpenClaw-related:

- *"How do I set up a WhatsApp channel in OpenClaw?"*
- *"Show me an example openclaw.json for multi-agent setup"*
- *"How to deploy OpenClaw on a VPS with Tailscale?"*
- *"What does openclaw doctor check?"*

The skill will automatically query live documentation and synthesize an up-to-date answer.

## License

MIT
