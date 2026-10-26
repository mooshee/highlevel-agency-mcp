# HighLevel Agency & Builder MCP

[![HighLevel Agency & Builder MCP](https://img.shields.io/badge/HighLevel%20Agency%20MCP-v1.0.0-blue.svg)](https://ghlagencymcp.com)
[![HighLevel Agency MCP server quality and maintenance on Glama](https://glama.ai/mcp/servers/mooshee/highlevel-agency-mcp/badges/score.svg)](https://glama.ai/mcp/servers/mooshee/highlevel-agency-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> **Author**: Daniel Hallman  
> **Website**: [ghlagencymcp.com](https://ghlagencymcp.com) (Aliases: [ghlmcp.dev](https://ghlmcp.dev), [ghlmcp.app](https://ghlmcp.app))  
> **Remote MCP Endpoint**: `https://ghlagencymcp.com/mcp` (`streamable-http`)  
> **Official MCP Registry ID**: `io.github.mooshee/highlevel-agency-mcp`  

HighLevel Agency & Builder MCP is the full-stack GoHighLevel (GHL) Model Context Protocol server and skill suite for agency owners, SaaS Mode operators, and funnel builders. Automate funnel and website page layouts, client domain DNS and SSL onboarding, workflow graphs, LeadShield contact form spam and B2B solicitation blockers, call-screening IVRs, Custom Values validation, LC Phone wallet-drain audits, and Master Snapshot diffs from Claude, Cursor, ChatGPT, VS Code, Gemini CLI, Grok Bot, Muse, Antigravity, and Perplexity.

## Quick start

1. Visit [HighLevel Agency & Builder MCP](https://ghlagencymcp.com) to browse workflow blueprints, architecture guides, and setup docs.
2. Connect any MCP client to `https://ghlagencymcp.com/mcp` (`streamable-http`), or install directly in your preferred host:
   - **VS Code (1-Click MCP)**: [Install HighLevel Agency MCP in VS Code](https://insiders.vscode.dev/redirect/mcp/install?name=highlevel-agency-mcp&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fghlagencymcp.com%2Fmcp%22%7D)
   - **Claude Code**: `/plugin marketplace add mooshee/highlevel-agency-mcp` then `/plugin install highlevel-agency-mcp@highlevel-agency-mcp`
   - **Gemini CLI**: `gemini extensions install https://github.com/mooshee/highlevel-agency-mcp`
   - **Devin CLI**: `devin plugins install mooshee/highlevel-agency-mcp`
   - **Vercel Skills (`skills.sh`)**: `npx skills add mooshee/highlevel-agency-mcp`
   - **ClawHub**: `clawhub install highlevel-agency-mcp`

---

## Core Capabilities

### 1. Funnel & Website Page Builder (`ghl_site_builder_sync`)
- Export, inspect, diff, and update live funnel steps and website pages.
- Modify headlines, copy, sections, and custom CSS while keeping native 2-step order forms, order bumps, and 1-click upsell blocks intact.
- Sync page templates and layout revisions with local Git version control and dry-run diff previews before publishing.

### 2. Client Domain, DNS & Branded Link Onboarding (`ghl_domain_ssl_onboard`)
- Plan and verify custom funnel/website domains and branded short-link domains (`CNAME`, `A`, and `TXT` records).
- Check DNS propagation, SPF/DKIM/DMARC, Apple Branded Mail BIMI logos, and SSL readiness before attaching domains.

### 3. Workflows, LeadShield Form Spam Guards & Call-Screening IVRs (`ghl_workflow_ivr_builder`)
- Generate and publish multi-branch workflow automations from structured specifications, including 2-stage **LeadShield** contact form spam and B2B solicitation screening (`deliver_to_client` vs `spam_quarantine` branches).
- Provision call-screening IVR trees ("Press 1 to connect") on tracking numbers to block robocalls before forwarding to client phones.
- Create and update multi-step forms and conditional surveys mapped directly to sub-account custom fields.

### 4. Snapshot Drift, Custom Values & Broken-Merge-Tag Auditing (`ghl_snapshot_diff_audit`, `ghl_custom_values_audit`)
- Compare any live client sub-account against a reference Master Snapshot without overwriting existing sub-account customizations.
- Batch-sync sub-account Custom Values and scan SMS/email templates for unresolved `{{ custom_values.* }}` merge tags or `TBD`/`INSERT_HERE` placeholders before launch.

### 5. Telephony Wallet-Drain Audit & Role Governance (`ghl_phone_wallet_audit`, `ghl_user_role_governance`)
- Audit LC Phone numbers and number pools for unassigned numbers draining monthly balance, self-forwarding loops, and missing SMS/MMS capabilities.
- Provision staff and contractors with least-privilege role presets (`va-support`, `sales-rep`, `client-admin`, `agency-admin`) and offboard sub-account access in one command.

---

## MCP Configuration (`mcp.json`)

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

## Links & Documentation

- **Website**: [https://ghlagencymcp.com](https://ghlagencymcp.com)
- **Pricing & Plans**: [https://ghlagencymcp.com/pricing](https://ghlagencymcp.com/pricing)
- **Support & Docs**: [https://ghlagencymcp.com/support](https://ghlagencymcp.com/support)
- **Privacy Policy**: [https://ghlagencymcp.com/privacy](https://ghlagencymcp.com/privacy)
- **Terms of Service**: [https://ghlagencymcp.com/terms](https://ghlagencymcp.com/terms)
- **Release Notes**: [GitHub Releases](https://github.com/mooshee/highlevel-agency-mcp/releases)
