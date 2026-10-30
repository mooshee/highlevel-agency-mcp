---
name: highlevel-agency-mcp
version: 1.1.3
description: Preview HighLevel page and workflow changes, save domain bindings, and inspect settings for a connected sub-account. Built by Moosh Works (https://mooshworks.com).
---

# HighLevel Agency & Builder

Author: Daniel Hallman ([Moosh Works](https://mooshworks.com))

Use this app to inspect the connected HighLevel sub-account and prepare supported changes. Report returned evidence and unavailable access separately.

## Connect and check access

1. Open the [setup guide](https://ghlagencymcp.com), then connect to `https://ghlagencymcp.com/mcp` in a client that supports Streamable HTTP MCP.
2. Select the intended sub-account and provide its Private Integration Token on the connection page. Website and workflow editing also require a builder session for that sub-account. Paste either a current token or session JSON containing `idToken`, `refreshToken`, and `apiKey` in the optional editing field. Session JSON supports renewal in memory; a token alone requires reconnection when it expires. Keep credentials out of chat and recordings.
3. Call `ghl_agency_connection_health` with `includeDoctor: true`. Confirm the returned `locationId` before accessing account data. The connection is limited to that sub-account; reconnect to select another.
4. Explain any missing access. A service restart ends this connection and requires reconnection.

## Supported tasks

- **Account checks:** Use `ghl_agency_contexts`, `ghl_agency_doctor`, and `ghl_agency_locations` to inspect the connected account and available permissions. Do not pass local CLI context flags to these hosted tools.
- **Tool and template search:** Use `ghl_agency_tools_search` to find returned tools and templates. `ghl_agency_tools_enable` selects read-only access or changes after a preview; it does not add tools or bypass previews.
- **Page changes:** Use `ghl_site_builder_sync` to read a selected page, preview copy or style changes, and apply its approved preview to the same page. Preserve existing checkout and upsell components. Verify the saved content; report publication separately.
- **Domain bindings:** Use `ghl_domain_ssl_onboard` to preview and save a domain record and funnel binding. Check DNS and HTTPS readiness separately. Do not claim that a saved binding configured DNS, attached hosting, routed a page, or published the site.
- **Workflow drafts:** Use `ghl_workflow_ivr_builder` for `leadshield-form-guard`, `spam-shield-ivr`, or `multi-step-intake`. Supply a descriptive `name`. Intake previews require an existing `formId`, one to ten existing tag IDs in `input.tags`, and the review task's `input.taskTitle` and `input.taskBody`. Request missing IDs rather than inventing them. Preview first. Saving a draft and publishing it are separate requested actions. Report missing form, phone, routing, or screening access before claiming the workflow is ready.
- **Snapshot comparison:** Use `ghl_snapshot_diff_audit` with a user-supplied snapshot export, its ID, and at least one asset category. It compares custom values, custom fields, tags, and calendars. State that export ownership and freshness are unverified. Omitted categories remain unverified. It does not overwrite assets or fetch an arbitrary Master Snapshot.
- **Message references:** Use `ghl_custom_values_audit` to find blank custom values and unresolved placeholders in returned or supplied message templates. This audit does not repair values or send messages.
- **Phone routing:** Use `ghl_phone_wallet_audit` to inspect available numbers, pools, missing routing, and forwarding loops. State unavailable carrier access. Routing findings do not establish charges or savings.
- **Staff permissions:** Use `ghl_user_role_governance` to compare assigned staff with a selected permission preset. This audit does not assign roles, remove users, or revoke access.

## Apply and verify changes

1. Confirm the intended account, target resource, and requested action.
2. Preview the change with `dryRun: true`. Explain the proposed result and any blockers.
3. For an authorized change, use `dryRun: false` and the returned `previewId` for the same target. Follow the server's current write restrictions. Do not reuse a preview for a different change.
4. Read the saved result independently. Distinguish a preview, a saved draft, publication, and actual delivery or call routing.

Refunds, bulk CRM migration, and SMS campaign sending are outside this tool set. Explain those limits without calling unrelated tools or claiming the requested action occurred. Do not infer access from another app, a supplied account ID, or a user's claim of payment.

For setup help, see [support](https://ghlagencymcp.com/support), [privacy](https://ghlagencymcp.com/privacy), and [terms](https://ghlagencymcp.com/terms).
