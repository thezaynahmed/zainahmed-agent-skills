---
name: zainahmed-docs-mcp
description: Find Zain Ahmed's developer documentation, OpenAPI schema, and architecture guidance through the public documentation MCP server.
---

# Zain Ahmed documentation MCP

Use this skill to answer questions about the site's API, integration guides, or published architecture material. The documentation MCP endpoint is `https://zainahmed.net/mcp/docs`; the browser documentation index is `https://zainahmed.net/docs`.

1. Connect with a Streamable HTTP MCP client and list the available tools. Use the server's actual schemas rather than assuming a fixed tool count or argument shape.
2. Search the documentation for the user's topic, then retrieve the relevant page or OpenAPI specification before giving endpoint-specific guidance. The direct OpenAPI fallback is `https://zainahmed.net/openapi.json`.
3. Cite the page or schema URL used. If MCP is unavailable, follow links from `https://zainahmed.net/developers` and `https://zainahmed.net/docs/llms.txt`.
4. The public documentation server does not require a token. Agent registration and OAuth token issuance are currently unavailable; do not recommend them as a setup step. The current access contract is `https://zainahmed.net/auth.md`.

Keep retrieval separate from actions: reading a guide does not authorize sending a contact request or making other mutations.
