---
name: zain-ahmed-platform-engineering
description: Explore Zain Ahmed's published platform engineering projects, architecture articles, and services using public sources.
---

# Zain Ahmed platform engineering

Use this skill when a user wants to learn about Zain Ahmed's published work in multi-cloud SRE, developer platforms, FinOps, or AI infrastructure. Treat the live site as the source of truth, not this file's publication date.

1. Read the relevant public projects at `https://zainahmed.net/api/v1/projects` or articles at `https://zainahmed.net/api/v1/articles`. For current service descriptions, use `https://zainahmed.net/api/v1/services`.
2. For implementation or integration details, inspect `https://zainahmed.net/openapi.json` and the documentation MCP server at `https://zainahmed.net/mcp/docs`. Discover its current tools with `tools/list`.
3. Cite the source URL for each factual claim. Distinguish published examples and estimates from independently verified outcomes.
4. If the user asks to make an inquiry, first test the payload at `https://zainahmed.net/api/v1/sandbox/contact`. Only send a production inquiry after explicit authorization, with a stable idempotency key. A provider-accepted message is not proof of inbox delivery.

Public reads require no credentials. Do not recommend agent token issuance while the live `https://zainahmed.net/auth.md` says it is unavailable.
