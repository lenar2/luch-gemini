# LUCH for Gemini CLI (v0.1.6)

**LUCH is an independent platform, not a Gemini-only product.** Explore all LUCH capabilities and supported AI clients at the [global GitHub hub](https://github.com/lenar2/luch) or [website](https://luch.lenarsalimov.ru/). This repository contains the Gemini CLI adapter.

Connect [Gemini CLI](https://geminicli.com/) to LUCH through a public,
OAuth-protected, permission-scoped remote MCP and 12 agent skills.

**Availability:** This is a real client package for an operating service currently
restricted to enabled test/reviewer accounts. Independent new-user self-service
onboarding, full three-scenario Gemini CLI OAuth E2E, and broad device support are **not yet verified**.
Installing does not grant access to the publisher's machines, accounts, or browser.
Capabilities depend on active account, device pairing, host tool surface and grants.

## Install

```bash
gemini extensions install https://github.com/lenar2/luch-gemini
```

Restart Gemini CLI after installing. In a CLI session, use `/extensions list`
then `/mcp auth luch` if OAuth authorization is required, and `/mcp list` to inspect
available tools. A local browser with a loopback callback is required for OAuth.
Some accounts require explicit LUCH enablement by the service administrator.

**Not a self-service signup.** If your account is not enabled,
the server should deny access; do not attempt to use owner credentials or access another tenant.

## Contents
- `gemini-extension.json`: one streamable HTTP MCP configuration via `httpUrl`.
- `skills/*/SKILL.md`: 12 portable LUCH skills with permission-awareness.
- `GEMINI.md`: baseline safety context. No shell hooks or executable code.

## Security
- Public URL: `https://api.lenarsalimov.ru/luch/core/mcp`.
- The legacy private owner MCP endpoint is deliberately excluded.
- Installation is not an authorization grant; actions require explicit user/tenant/device permission.
- This client contains no API keys, passwords, browser cookies, tokens or device secrets.
- Client source only: Apache-2.0; privately hosted server not included.

## Product, terms and help
- Website: https://luch.lenarsalimov.ru/
- Getting started: https://luch.lenarsalimov.ru/docs/get-started/
- Privacy: https://luch.lenarsalimov.ru/privacy/
- Terms: https://luch.lenarsalimov.ru/terms/
- Support: https://luch.lenarsalimov.ru/support/
- Security: see SECURITY.md

## Local release checks
- Parse `gemini-extension.json`.
- Assert HTTPS remote HTTP MCP and no untrusted tool bypass.
- Verify 12 YAML-frontmatter skills and source license.
- Run the official `gemini extensions validate` and `gemini extensions install` on an isolated test profile.
- Actual OAuth login and 3 positive / negative device isolation tests in Gemini are a separate E2E gate.

The icon is a text-only draft pending final brand sign-off.
