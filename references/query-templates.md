# DeepWiki Query Templates for OpenClaw

Pre-built query templates organized by topic. Use these as starting points when querying DeepWiki with `mcp__deepwiki__ask_question`.

## Installation & Setup

```
"How to install OpenClaw on [macOS|Linux|VPS]? Include prerequisites and post-install steps."
"What does the openclaw onboard wizard do step by step? What flags are available?"
"How to install OpenClaw Gateway as a background daemon service?"
"How to set up OpenClaw for the first time with [model provider]?"
```

## Gateway Management

```
"How to start, stop, and restart the OpenClaw Gateway? What are all available flags?"
"How to configure Gateway binding mode (loopback, LAN, Tailscale)?"
"How to check Gateway health and status? What does each status field mean?"
"How to expose Gateway remotely via Tailscale serve/funnel?"
"How to configure Gateway authentication (token vs password mode)?"
```

## Agent Configuration

```
"Show complete agent configuration schema in openclaw.json with all available fields."
"How to set up multi-agent routing? How does session resolution work per agent?"
"How to configure agent workspace, model selection, and tool policies?"
"How does agent sandboxing work? Explain sandbox modes (off, non-main, all) and scopes."
"How to configure model failover and routing for agents?"
"How does context overflow and auto-compaction work in agents?"
```

## Channel Setup

```
"Step-by-step guide to set up [WhatsApp|Telegram|Discord|Signal|Slack|iMessage] channel."
"How to configure channel access control (allowFrom, groups, requireMention)?"
"How to troubleshoot channel connection issues for [channel name]?"
"How does channel routing work? How to route different channels to different agents?"
"How to view channel logs and debug channel issues?"
```

## Model Configuration

```
"How to configure custom model providers (OpenRouter, local LLM, LiteLLM proxy)?"
"Show example model configuration for [Anthropic|OpenAI|custom provider] in openclaw.json."
"How does model failover work? How to configure primary and fallback models?"
"How to check model provider authentication and availability with openclaw models?"
```

## Skills System

```
"How do OpenClaw skills work? What is the skill loading precedence?"
"How to create a custom OpenClaw skill? Show SKILL.md format and directory structure."
"How to configure skills in openclaw.json (allowBundled, extraDirs, entries)?"
"What are the built-in bundled skills and what does each do?"
"How does skill metadata gating work (bins, env, config requirements)?"
```

## Memory System

```
"How does OpenClaw memory work? Explain daily notes and MEMORY.md."
"How to configure memory indexing and search?"
"How does session-based memory relate to workspace memory files?"
```

## Session Management

```
"How does session scoping work (per-sender, per-channel, shared)?"
"How to configure session reset policies (daily, idle, manual triggers)?"
"Where are session transcripts stored and in what format?"
```

## Commands & Directives

```
"List all available slash commands in OpenClaw with descriptions."
"How do directives work? What platform-specific commands are available?"
"How to use TTS and voice commands in OpenClaw?"
```

## Deployment

```
"How to deploy OpenClaw on a VPS with proper security hardening?"
"How to set up OpenClaw with Tailscale for remote access?"
"How to deploy OpenClaw using the openclaw-ansible playbook?"
"How to configure network settings for production deployment?"
```

## Troubleshooting

```
"What does openclaw doctor check? How to interpret and fix each diagnostic?"
"How to troubleshoot [specific error message or symptom]?"
"Common OpenClaw issues and their solutions?"
"How to enable verbose logging for debugging?"
"How to perform migration and backup of OpenClaw data?"
```

## CLI Deep Dives

```
"Complete flag reference for openclaw [subcommand name]."
"How to use openclaw config to manage configuration?"
"How to use openclaw diagnostic commands for troubleshooting?"
"How to manage memory via openclaw CLI (openclaw memory commands)?"
```

## Tips for Effective Queries

1. **Be specific**: Include the exact feature, config key, or error message
2. **Ask for examples**: "Show example config" yields better results than "explain config"
3. **Combine topics**: "How to configure WhatsApp channel with access control and route to specific agent"
4. **Request comparisons**: "Compare sandbox modes off vs non-main vs all with use cases"
5. **Ask about edge cases**: "What happens when [specific scenario]?"
