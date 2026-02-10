[English](README.md) | [繁體中文](README.zh.md)

# openclaw-mentor

一個 Claude Code 技能，作為 [OpenClaw](https://github.com/openclaw/openclaw) 的 AI 導師 — 自架多頻道 AI 代理閘道器。

## 說明

當使用者詢問「OpenClaw 怎麼用」、「查 OpenClaw 文件」、「OpenClaw 幫助」、「openclaw mentor」，或需要 OpenClaw 設定、CLI 指令、頻道、代理、技能、記憶、部署或疑難排解的指引時，使用此技能。

## 功能特色

此技能不依賴靜態的過時知識，而是透過 **smart-search** 技能即時查詢 `openclaw/openclaw` 倉庫的文件。涵蓋所有主要 OpenClaw 領域：

- **安裝與入門** — 設定精靈、背景服務管理
- **閘道器與設定** — `openclaw.json`（JSON5）、WebSocket 服務
- **代理與工作階段** — 工作區、模型、沙箱化執行環境
- **工具與技能** — 內建工具、自訂技能、排程任務
- **記憶** — 每日筆記、`MEMORY.md`、索引
- **頻道** — WhatsApp、Telegram、Discord、Signal、iMessage、Slack
- **CLI 指令** — 所有子命令和旗標
- **部署** — VPS、雲端、Tailscale、Ansible
- **疑難排解** — `openclaw doctor`、診斷工具

## 安裝

將技能安裝到 Claude Code：

```bash
claude skill add joneshong-skills/openclaw-mentor
```

### 前置條件

- 已安裝 **smart-search** 技能（`~/.claude/skills/smart-search/`）

## 使用方式

安裝後，直接詢問 Claude 任何 OpenClaw 相關問題：

- *「如何在 OpenClaw 中設定 WhatsApp 頻道？」*
- *「Show me an example openclaw.json for multi-agent setup」*
- *「如何在 VPS 上使用 Tailscale 部署 OpenClaw？」*
- *「openclaw doctor 會檢查什麼？」*

技能會自動查詢最新文件並合成即時回答。

## 授權

MIT
