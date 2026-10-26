---
name: highlevel-agency-mcp
version: 1.0.0
description: Automate GoHighLevel (GHL) funnel and website page layouts, client domain DNS & SSL onboarding, multi-step forms, workflow graphs, LeadShield contact form spam & B2B solicitation blockers, spam-shield IVRs, and sub-account snapshot diffs using HighLevel Agency & Builder MCP.
---

# HighLevel Agency & Builder MCP

Author: Daniel Hallman

Use the **HighLevel Agency & Builder MCP** (`https://ghlagencymcp.com/mcp`) whenever the user wants to inspect, build, update, or verify GoHighLevel (GHL) funnels, websites, domains, forms, workflows, LeadShield contact form spam guards, call-screening IVRs, or sub-account snapshots.

## Quick start

1. Open [HighLevel Agency & Builder MCP](https://ghlagencymcp.com) for interactive blueprints, setup guides, or to connect your AI assistant to `https://ghlagencymcp.com/mcp`.
2. Connect any Streamable HTTP MCP client (`https://ghlagencymcp.com/mcp`) or install the public plugin repository from [github.com/mooshee/highlevel-agency-mcp](https://github.com/mooshee/highlevel-agency-mcp).

## Core Capabilities

1. **Funnel & Website Page Builder (`ghl_site_builder_sync`)**:
   - Export, inspect, and update live funnel steps and website pages.
   - Modify headlines, copy, sections, and custom CSS while preserving native 2-step order forms, order bumps, and 1-click upsell blocks.
   - Sync page templates and layout revisions with local Git version control and dry-run diff previews before publishing.

2. **Client Domain, DNS & Branded Link Onboarding (`ghl_domain_ssl_onboard`)**:
   - Plan and verify funnel/website custom domains and branded short-link domains (`CNAME`, `A`, and `TXT` records).
   - Check propagation, SPF/DKIM/DMARC, Apple Branded Mail logos, and SSL provisioning status before attaching domains.

3. **Workflows, LeadShield Form Spam Guards, Spam-Shield IVRs & Multi-Step Forms (`ghl_workflow_ivr_builder`)**:
   - Generate and publish multi-branch workflow automations from structured specifications, including 2-stage **LeadShield** contact form spam and B2B solicitation screening (`deliver_to_client` vs `spam_quarantine` branches with `$0.00` Stage 0 deterministic bot drops).
   - Provision call-screening IVR trees ("Press 1 to connect") on tracking numbers to block robocalls before forwarding to client phones.
   - Create and update multi-step forms and conditional surveys mapped directly to sub-account custom fields.

4. **Snapshot Drift, Custom Values & Broken-Merge-Tag Auditing (`ghl_snapshot_diff_audit`, `ghl_agency_custom_values`, `ghl_agency_fleet_audit`)**:
   - Compare any live client sub-account against a reference Master Snapshot (`diff-location`) or run agency-wide `fleet-audit`.
   - Batch-sync sub-account Custom Values (`sync`) and run the Broken-Merge-Tag & Placeholder Validator (`validate`) across SMS/email templates to catch unresolved `{{ custom_values.* }}` references and `TBD`/`INSERT_HERE` placeholders before launch.

5. **Sub-Account Onboarding, SaaS Mode & Role Governance (`ghl_agency_saas`, `ghl_agency_brand_boards`, `ghl_agency_chat_widget`, `ghl_agency_custom_menus`, `ghl_agency_users`)**:
   - Manage SaaS Mode plans, subscriptions, pause/resume, and rebilling markups with dry-run guards.
   - Configure sub-account Brand Boards, Brand Voices, Chat Widgets, and Agency Custom Menu links.
   - Provision staff and contractors using locked least-privilege presets (`va-support`, `sales-rep`, `client-admin`, `agency-admin`) that prevent accidental contact exports, and offboard users in one command (`offboard`).

6. **Telephony Wallet-Drain Audit & Daily Changelog Loop (`ghl_agency_phone`, `ghl_agency_announcements`)**:
   - Audit LC Phone numbers and number pools (`phone audit`) for unassigned numbers draining monthly balance, self-forwarding loops, and missing SMS/MMS capabilities.
   - Ingest HighLevel's daily changelog feed (`announcements loop`) and diff live Private Integration Token scopes to stay current on platform launches.

## Safe Operating Principles

- **Explicit Context Selection**: Always confirm the target sub-account (`locationId`) and whether the operation targets a sandbox or production sub-account before mutating live assets.
- **Dry-Run, Read-Back & Safe-Writes Policy Presets**: Every write defaults to a read-only `--dry-run` preview and verifies persistence with a live read-back check. Supports Safe-Writes Policy Presets (`full-access`, `no-sending`, `no-deletes`, `read-only`) and Progressive Discovery (`--progressive`).

