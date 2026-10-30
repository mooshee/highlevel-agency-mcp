# HighLevel Agency & Builder MCP

Author: Daniel Hallman ([Moosh Works](https://mooshworks.com))

Preview page and workflow changes, save domain bindings, and inspect settings for a connected HighLevel sub-account. Review each proposed change before applying it, then verify the saved result.

## Connect your assistant

1. Connect a client that supports Streamable HTTP MCP to `https://ghlagencymcp.com/mcp`.
2. On the connection page, provide the intended sub-account's location ID and a dedicated Private Integration Token with only the required permissions. Leave the editing field empty for account checks. Page and workflow tools also need a builder session. Before supplying one, read the [credential permissions and revocation instructions](skills/highlevel-agency-mcp/SKILL.md#editing-credentials-and-revocation). Renewable session credentials carry the HighLevel user's permissions beyond the integration token's scopes. Keep credentials out of chat.
3. Check `ghl_agency_connection_health` with `includeDoctor: true` and confirm the returned location ID.
4. Reconnect if access expires or the service restarts. See the [setup guide](https://ghlagencymcp.com) for help.

## Try a task

- Compare a supplied snapshot export with the connected sub-account.
- Check Custom Values for broken merge tags.
- Preview an update to a funnel headline while preserving its order form.
- Inspect available phone routing and forwarding loops.

See the [skill instructions](skills/highlevel-agency-mcp/SKILL.md) for the tools and required checks.

## Before applying changes

Confirm the target sub-account and whether it is a sandbox or production account. Preview with `dryRun: true`. Apply an authorized change with `dryRun: false` and the returned `previewId`, then read the saved result. Workflow drafts, publication, and delivery are separate outcomes. Domain bindings do not establish DNS, HTTPS, hosting, or publication. Staff-permission and custom-value audits do not change those settings.

For help, use [support](https://ghlagencymcp.com/support). See the [privacy policy](https://ghlagencymcp.com/privacy) and [terms](https://ghlagencymcp.com/terms) before connecting an account.

## Package and review status

This is version 1.1.4 of the public integration package. The separate ChatGPT 1.1.3 listing is in review. Installing this package does not establish ChatGPT directory approval.

## Release notes

Version 1.1.4 — October 30, 2026 clarifies credential permissions and revocation. See [release notes](RELEASE-NOTES.md) and the [versioned release](https://github.com/mooshee/highlevel-agency-mcp/releases/tag/v1.1.4).
