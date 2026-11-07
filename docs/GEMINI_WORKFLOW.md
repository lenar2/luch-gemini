# Gemini CLI workflow: turn a terminal check into an operational report

[← LUCH for Gemini CLI](../README.md) · [Русский](GEMINI_WORKFLOW.ru.md)

## The situation

A service has changed and you need to understand its current state before deciding what to do.

## The work

1. **Choose the exact server.** Confirm its identity in the resources available to your account.
2. **Observe first.** Ask LUCH for current status and health.
3. **Run a bounded check.** Use a read-only command with a clear target, fixed working directory and timeout.
4. **Interpret the output.** Separate observed facts, expected conditions and unknowns.
5. **Report the next action.** Recommend what to inspect next; do not restart or deploy automatically.

## A prompt to try

> Check the status of the server I selected. Run only bounded, read-only diagnostics needed to understand whether the service is responding. Show the actual output, distinguish PASS from UNKNOWN, and recommend the next check. Do not restart or change anything.

## Why Gemini CLI and LUCH fit together

Gemini CLI gives you a terminal-first working style. LUCH can bring in the selected server, authorized files and — where available — a browser session. This connects command-line reasoning to observed resources instead of assumptions.

This is a designed workflow based on the extension's skills, not a claim that the exact scenario has been independently run for every user.
