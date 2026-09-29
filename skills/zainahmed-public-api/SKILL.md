---
name: zainahmed-public-api
description: Use Zain Ahmed's public REST API to retrieve profile, project, article, and service information, or validate a contact integration in the no-send sandbox.
---

# Zain Ahmed public API

Use this skill when a user asks for current information from zainahmed.net or wants to test an integration with its public API. The API base URL is `https://zainahmed.net/api/v1`; its schema is at `https://zainahmed.net/openapi.json`.

1. Read the OpenAPI operation for the requested resource. Use `GET /profile`, `/projects`, `/articles`, or `/services` for public information. These reads require no API key.
2. Use `POST /sandbox/contact` for a no-send contact integration test. Check that the response identifies `environment: "sandbox"`.
3. Only call `POST /contact` when the user explicitly asks to send an inquiry. Generate one 16–128-character `Idempotency-Key` for that inquiry, and reuse the same key and exact payload on retries. HTTP 200 means provider acceptance, not inbox delivery. If delivery is unconfirmed, do not create a new key to retry.
4. Treat 429 according to `Retry-After`. Do not send identity assertions or passwords to the agent registration endpoints: production credential issuance is unavailable. Check `https://zainahmed.net/auth.md` if access behavior changes.

Return the source URL with retrieved facts. Never describe a sandbox result as a delivered message.
