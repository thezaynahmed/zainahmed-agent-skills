# Agent instructions for this public skills repository

This repository publishes instructions for using zainahmed.net. It does not contain the website source code or production credentials.

- Keep each skill in `skills/<name>/SKILL.md` with matching lowercase `name` frontmatter and a specific `description`.
- Verify API endpoints and authentication status against `https://zainahmed.net/openapi.json` and `https://zainahmed.net/auth.md` before changing a skill.
- Public profile, project, article, service, and documentation reads require no token. Do not invent OAuth registration or ask users to submit identity assertions while issuance is unavailable.
- `POST /api/v1/sandbox/contact` is a no-send integration test. Only use production `POST /api/v1/contact` after explicit user authorization; reuse the same idempotency key and payload on retries.
- Never commit credentials, private source, or copied user data. Validate `plugin.json` and `mcp.json` against their declared Agent Plugins schemas and run `npx skills add . --list` before publishing.
