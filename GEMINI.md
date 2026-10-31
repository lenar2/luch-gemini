# LUCH for Gemini CLI
LUCH is an authorization-scoped remote MCP client, not a license to access devices.
Only use tools actually exposed to this authenticated Gemini CLI session. Confirm the user
owns/controls target resources and has approved the specific action. Pairing and per-device
grants must be verified before device operations.
Never infer authorization from skill descriptions, host installation or historical tool lists.
Public MCP: https://api.lenarsalimov.ru/luch/core/mcp. The legacy owner-only bridge is NOT
part of this extension and must never be used for public users.
Begin with bounded read-only work. Never expose secrets, OAuth tokens or private files.
If tools are absent or onboarding fails, report the verified limitation rather than claiming success.
