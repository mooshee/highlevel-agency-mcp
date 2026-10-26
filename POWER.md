---
name: highlevel-agency-mcp
displayName: HighLevel Agency & Builder MCP
version: 1.0.0
author: Daniel Hallman
description: Full-stack GoHighLevel (GHL) MCP for agency owners and funnel builders to automate funnel layouts, client DNS & SSL, workflow graphs, LeadShield contact form spam blockers, spam-shield IVRs, and snapshot diffs.
keywords:
  - highlevel
  - gohighlevel
  - ghl
  - mcp
  - funnels
  - workflows
  - dns
  - snapshots
  - leadshield
mcpServers:
  highlevel-agency-mcp:
    type: streamable-http
    url: https://ghlagencymcp.com/mcp
---

# HighLevel Agency & Builder MCP Power (AWS Kiro)

Author: Daniel Hallman

HighLevel Agency & Builder MCP connects your AI assistant to GoHighLevel (GHL) to automate funnel and website layouts, client domain DNS & SSL onboarding, workflow graphs, LeadShield contact form spam guards, call-screening IVRs, and Master Snapshot diffs.

## MCP Server Configuration

Connect Kiro to the remote Streamable HTTP MCP endpoint:

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

- `ghl_agency_connection_health`: Check HighLevel Agency MCP connection health, active Safe-Writes Policy preset, and progressive discovery status.
- `ghl_agency_tools_search`: Search across all 55 native HighLevel Agency MCP tools and tool packs by keyword or domain pack.
- `ghl_agency_tools_enable`: Dynamically enable a HighLevel MCP tool pack or specific tool names for the current Progressive Discovery session.
- `ghl_snapshot_diff_audit`: Compare a live HighLevel client sub-account against a reference Master Snapshot without overwriting assets.
- `ghl_site_builder_sync`: Export, diff, and update HighLevel funnel steps and website layouts while preserving 2-step carts and 1-click upsells.
- `ghl_domain_ssl_onboard`: Plan, verify, and attach HighLevel custom funnel domains and branded short-link CNAME/A/TXT records with SSL checks.
- `ghl_workflow_ivr_builder`: Synthesize and publish HighLevel workflows, LeadShield contact form spam guards, and call-screening IVRs.
- `ghl_custom_values_audit`: Batch-sync sub-account Custom Values and scan SMS/email templates for broken merge tags or TBD placeholders.
- `ghl_phone_wallet_audit`: Read-only audit of sub-account LC Phone numbers, number pools, forwarding loops, and unassigned monthly wallet drain.
- `ghl_user_role_governance`: Provision staff with least-privilege role presets or offboard sub-account access.
