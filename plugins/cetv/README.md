# CETV Campaigns for Claude

Advertise on CETV's network of digital screens in break rooms and venues, from a conversation with Claude.

- **Pick a package** — each with its own price, number of plays across the network, and duration.
- **Add your ad** — upload your JPG or PNG (1920×1080 landscape looks best).
- **Pay** — by card from a Stripe payment link (also emailed as an invoice), or with a promo code.
- **Track it** — ask how your campaign is doing to see plays delivered, updated hourly.

## What's included

| Component | What it does |
|---|---|
| **CETV connector** (`.mcp.json`) | Connects Claude to `https://mcp.cetvnow.com/mcp`. You sign in with your email (a one-time code) the first time it's used. |
| **`new-campaign` skill** | Walks you through package, start date, business details, uploading your ad, confirmation, and payment. |
| **`campaign-report` skill** | Shows status, plays delivered vs. your package, daily plays, and payment status. |

Works in claude.ai (web, desktop, mobile), Cowork, and Claude Code.

## Install

**Claude Code**

```
claude plugin marketplace add CETV-Now/claude-plugins
claude plugin install cetv@cetv-now
```

Then start a session and say "I want to advertise on CETV" (or run `/cetv:new-campaign`). Run `/mcp` → **cetv** → **Authenticate** if Claude asks you to sign in.

**claude.ai / Claude desktop / Cowork**

Open **Customize → Plugins → Add marketplace**, enter `CETV-Now/claude-plugins`, then install **CETV Campaigns** and connect it from the plugin's **Connectors** tab.

## Data and privacy

The plugin runs nothing on your computer. It adds two skills (instructions for Claude) and one remote MCP server, `https://mcp.cetvnow.com/mcp`, operated by CETV Now. When you use it:

- You sign in to your CETV advertiser account with your email address (Clerk handles sign-in).
- Claude sends the CETV server only what each request needs, such as the package, start date, campaign name, and business name. It doesn't send your conversation, chat history, or files.
- Your ad image is uploaded through a private, single-use upload link (or, in Claude Code, straight from the file you choose) to CETV's storage, so it can be shown on CETV screens.
- Invoices are sent and paid through Stripe. Payment happens on Stripe's page; Claude never sees your card details.

Details: [documentation](https://mcp.cetvnow.com/docs) · [privacy notice](https://mcp.cetvnow.com/privacy)

## Support

info@cetvnow.com · https://cetvnow.com
