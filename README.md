# Zain Ahmed Agent Skills

Public, first-party agent skills for the developer resources at [zainahmed.net](https://zainahmed.net/developers). This repository contains instructions and portable MCP connection metadata, not application source or credentials.

Last reviewed: 2026-09-29

## Install

Prerequisites: Node.js 20+ and an AI coding agent supported by the [skills CLI](https://www.skills.sh/docs/cli).

```bash
npx skills add thezaynahmed/zainahmed-agent-skills --list
npx skills add thezaynahmed/zainahmed-agent-skills --skill zainahmed-public-api
```

| Skill | Use it for |
| --- | --- |
| `zain-ahmed-platform-engineering` | Exploring published architecture, projects, and services. |
| `zainahmed-public-api` | Reading current public API data or testing contact validation without sending. |
| `zainahmed-docs-mcp` | Retrieving API documentation and schemas through the documentation MCP server. |

The root [`plugin.json`](./plugin.json) and [`mcp.json`](./mcp.json) package these skills with the site's two public MCP endpoints under the [Agent Plugins 1.0 specification](https://agent-plugins.org/specification). Public reads need no token. Production agent credential issuance is currently unavailable; see the live [access contract](https://zainahmed.net/auth.md) before building an integration.

The live [OpenAPI specification](https://zainahmed.net/openapi.json) and [developer portal](https://zainahmed.net/developers) are the source of truth for endpoints. This repository is MIT licensed.
