---
name: highlevel-agency-mcp
displayName: HighLevel Agency & Builder MCP
version: 1.1.1
author: Daniel Hallman
description: Full-stack GoHighLevel (GHL) automation for agency owners & funnel builders.
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

# HighLevel Agency & Builder MCP Power (AWS Kiro)

Author: Daniel Hallman ([Moosh Works](https://mooshworks.com))

Full-stack GoHighLevel (GHL) automation for agency owners & funnel builders. Automate funnel layouts, client DNS & SSL, workflow graphs, LeadShield contact form spam & B2B solicitation blockers, spam-shield IVRs, and snapshot diffs. Built by Moosh Works (https://mooshworks.com).

## Quick start

1. Visit [HighLevel Agency & Builder MCP](https://ghlagencymcp.com) or connect Kiro to `https://ghlagencymcp.com/mcp`.
2. Built and maintained by [Moosh Works](https://mooshworks.com).

## MCP Server Configuration

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

## Tools Available

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
