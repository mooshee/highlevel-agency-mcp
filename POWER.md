---
name: highlevel-agency-mcp
displayName: HighLevel Agency & Builder MCP
version: 1.1.2
author: Daniel Hallman
description: Manage HighLevel funnels, websites, domains, workflows, and sub-accounts from your AI assistant.
keywords:
  - highlevel
  - gohighlevel
  - ghl
  - mcp
  - agency
  - funnels
  - workflows
  - dns
  - snapshots
  - custom-values
  - saas-mode
  - telephony
  - ivr
  - spam-blocker
  - leadshield
mcpServers:
  highlevel-agency-mcp:
    type: streamable-http
    url: https://ghlagencymcp.com/mcp
---

# HighLevel Agency & Builder MCP for Kiro

Author: Daniel Hallman ([Moosh Works](https://mooshworks.com))

Manage HighLevel funnels, websites, domains, workflows, and sub-accounts from your AI assistant. Check forms for spam, set up call screening, and compare account settings. Built by Moosh Works (https://mooshworks.com).

## Quick start

1. Open [HighLevel Agency & Builder MCP](https://ghlagencymcp.com) for setup instructions.
2. Add `https://ghlagencymcp.com/mcp` as an MCP server in Kiro using the configuration below. Complete any required sign-in.
3. Check that the connection lists the plugin's tools before starting a task.

## Server configuration

```json
{
  "mcpServers": {
    "highlevel-agency-mcp": {
      "type": "streamable-http",
      "url": "https://ghlagencymcp.com/mcp"
    }
  }
}
```

## Available tools

- `ghl_agency_connection_health`
- `ghl_agency_contexts`
- `ghl_agency_doctor`
- `ghl_agency_locations`
- `ghl_agency_tools_enable`
- `ghl_agency_tools_search`
- `ghl_custom_values_audit`
- `ghl_domain_ssl_onboard`
- `ghl_phone_wallet_audit`
- `ghl_site_builder_sync`
- `ghl_snapshot_diff_audit`
- `ghl_user_role_governance`
- `ghl_workflow_ivr_builder`
