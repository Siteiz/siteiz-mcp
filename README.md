# Siteiz MCP Server

Free, read-only remote MCP server for AI visibility. Ask Claude, Cursor or any MCP client whether a site blocks ChatGPT or Perplexity, what AI crawlers see without JavaScript, and what each AI bot does.

**Endpoint:** `https://siteiz.com/mcp` (Streamable HTTP, no API key)
**Docs:** https://siteiz.com/mcp-server
**Registry:** `com.siteiz/siteiz` in the official MCP Registry

## Tools

| Tool | What it does |
|---|---|
| `check_ai_crawlers` | Which of 11 AI crawlers (GPTBot, OAI-SearchBot, ClaudeBot, Claude-SearchBot, PerplexityBot, Google-Extended and more) a site's robots.txt allows, with AI search kept apart from training crawlers |
| `view_page_as_ai_crawler` | What a page delivers without JavaScript: title, meta, H1, structured data, word count, token reading cost |
| `explain_ai_crawler` | What an AI bot does and what blocking it changes |
| `get_ai_visibility_report` | Published, dated AI visibility reports on well-known sites |

## Install

**Claude Code**
```bash
claude mcp add --transport http siteiz https://siteiz.com/mcp
```

**Claude (claude.ai and desktop):** Settings, Connectors, Add custom connector, paste `https://siteiz.com/mcp`.

**Cursor** (`~/.cursor/mcp.json`)
```json
{ "mcpServers": { "siteiz": { "url": "https://siteiz.com/mcp" } } }
```

**VS Code** (`.vscode/mcp.json`)
```json
{ "servers": { "siteiz": { "type": "http", "url": "https://siteiz.com/mcp" } } }
```

## About

Built by [Siteiz](https://siteiz.com). Answers come from the same deterministic rules as the [Siteiz AI visibility scan](https://siteiz.com/scan). All tools are read-only.
