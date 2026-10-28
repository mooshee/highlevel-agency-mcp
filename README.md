# HighLevel Agency & Builder MCP

Author: Daniel Hallman ([Moosh Works](https://mooshworks.com))

Manage HighLevel funnels, websites, domains, workflows, and sub-accounts from your AI assistant. Check form spam, set up call screening, compare account settings, and review changes before applying them.

## Connect your assistant

1. Open the [setup guide](https://ghlagencymcp.com) and choose your AI assistant.
2. Connect a client that supports Streamable HTTP MCP to `https://ghlagencymcp.com/mcp`, or install the plugin from the [public repository](https://github.com/mooshee/highlevel-agency-mcp).
3. Check the connection with `ghl_agency_connection_health`.
4. Confirm the intended account appears before asking the assistant to make changes.

## Try a task

- Compare a client sub-account with your Master Snapshot.
- Check Custom Values for broken merge tags.
- Preview an update to a funnel headline while preserving its order form.
- Check unused phone numbers and forwarding loops.

See the [skill instructions](skills/highlevel-agency-mcp/SKILL.md) for the tools and required checks.

## Before applying changes

Confirm the target sub-account and whether it is a sandbox or production account. Preview changes, follow the active write restrictions, and read the saved result after an authorized update.

For help, use [support](https://ghlagencymcp.com/support). See the [privacy policy](https://ghlagencymcp.com/privacy) and [terms](https://ghlagencymcp.com/terms) before connecting an account.

## Package and review status

The included OpenAI review draft still needs a verified recording and provider checks before submission. Installing this package does not submit it to a directory.

## Release notes

[Version 1.1.2 — October 28, 2026](https://github.com/mooshee/highlevel-agency-mcp/releases/tag/v1.1.2) clarifies descriptions, example prompts, and setup checks. Existing connections and features are unchanged. Update your plugin or skill to load the revised instructions.
