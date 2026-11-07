# LUCH for Gemini CLI

Use LUCH to connect a terminal task to the resources selected by the user: an authorized server, permitted files or a browser session.

## Working style

- Confirm the exact target before acting.
- Begin with current status and read-only observation.
- Use bounded commands with a fixed target and timeout.
- Distinguish observed output from assumptions.
- Return the result and the next useful check in plain language.

## Safety

Only use tools actually exposed to this authenticated Gemini CLI session. Confirm that the user owns or controls the target and has approved the specific action. Pairing and per-resource grants must be verified before acting. Never infer access from this file or the extension installation.

Do not use owner-only bridges or credentials. Do not expose secrets, OAuth tokens or private files. Do not restart production, alter firewall/DNS, install services or deploy changes without explicit scope and approval.

If a tool or resource is not available, report that accurately. A successful command submission is not proof that an external side effect completed.
