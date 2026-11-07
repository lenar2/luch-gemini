<p><img src="https://raw.githubusercontent.com/lenar2/luch/main/website/assets/luch-ray.svg" width="36"></p>

# LUCH for Gemini CLI
### Keep the terminal. Reach the right tool.

Gemini CLI is the place you describe the work. With an enabled account, **LUCH can provide permission-scoped access to the browser, files, devices or approved servers** needed to make progress — without treating a prompt as unlimited authority.

[**See one real LUCH workflow**](https://github.com/lenar2/luch/blob/design/hea-evidence-first-20261107/docs/REAL_WORK.md) · [**Get started**](#connect-with-gemini-cli) · [Русский](README.ru.md) · [LUCH home](https://github.com/lenar2/luch)

> **Early access:** the extension source is public. An arbitrary new user's self-service enrollment, complete Gemini OAuth E2E and broad device access are **not verified**. Installation is not an account grant.

## What actual work can look like

The founder asked to change LUCH's over-technical website while leaving the Mac alone. The assistant inspected the website and GitHub source through authorized tools, prepared a redesign, fixed a mobile issue and released the change with permission. The [public commit](https://github.com/lenar2/luch/commit/06daa8d6b89a3dfd65e74628b895879e79a0c931) and [release evidence](https://github.com/lenar2/ai-factory-evidence/issues/4009#issuecomment-6692683064) are real.

**This was a founder-environment LUCH task, not a verified Gemini CLI execution.** [Full case and caveats](https://github.com/lenar2/luch/blob/design/hea-evidence-first-20261107/docs/REAL_WORK.md).

## Connect with Gemini CLI

**1 · See if your account is enabled.** [Service availability](https://luch.lenarsalimov.ru/en/status/). If not, public code cannot enroll you.

**2 · Install the extension** in a supported Gemini CLI setup:

```bash
gemini extensions install https://github.com/lenar2/luch-gemini
```

Restart Gemini CLI. Then:

```text
/extensions list
/mcp auth luch
/mcp list
```

OAuth may require a local browser loopback callback. Use an account explicitly permitted to access LUCH; never use owner credentials.

**3 · Start with a read-only result.** Ask: “Open this public documentation page, then tell me what it actually says with a source link.” Inspect the available tool list and the result before authorizing changes.

## What the extension contains

| Part | Purpose |
| --- | --- |
| [`gemini-extension.json`](gemini-extension.json) | Protected HTTPS remote MCP configuration |
| [`skills/`](skills/) | 12 portable, permission-aware skills |
| [`GEMINI.md`](GEMINI.md) | Baseline safety context; no hidden shell automation |

The public MCP endpoint is `https://api.lenarsalimov.ru/luch/core/mcp`. No secret keys, publisher device permissions or private server source ship with this extension.

<details><summary>Validation and release boundaries</summary>

Parsing the manifest or successfully installing a package is only a packaging check. Independent Gemini-host OAuth, authorized discovery and a real browser/server/file test, revocation and account isolation require separate evidence; no such broad PASS is asserted. The older text-only icon remains a draft pending brand sign-off.

[Security](SECURITY.md) · [Terms](https://luch.lenarsalimov.ru/terms/) · [Privacy](https://luch.lenarsalimov.ru/privacy/) · [Support](https://luch.lenarsalimov.ru/support/)

</details>
