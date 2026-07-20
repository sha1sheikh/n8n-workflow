# Pricing & Packaging — n8n Automation Services

A starting framework for selling n8n automations. These are illustrative ranges,
not fixed rules — adjust to your market, experience, and the client's size.
Anchor on the **value** you deliver (hours saved, revenue captured, errors
avoided), not the hours you spend building.

## The model that works: build fee + retainer

Charge a **one-time build fee** to create and deploy the automation, then a
**monthly retainer** to keep it running, monitored, and updated. The retainer is
where the sustainable income is — automations break when APIs change, and clients
happily pay to not worry about it.

## Packages

### 🥉 Starter Automation
**One workflow, ~1–3 nodes of real logic.** e.g. the Lead Capture template:
form → sheet + Slack notification.
- **Build fee:** entry-level one-time fee
- **Retainer:** small monthly (monitoring + minor tweaks)
- **Good for:** first clients, proving value fast

### 🥈 Business Automation
**A multi-step workflow with branching / an integration or two.** e.g. lead
capture + CRM sync + auto-reply email + lead scoring.
- **Build fee:** mid one-time fee
- **Retainer:** monthly (monitoring + monthly change window)
- **Good for:** SMBs replacing a real manual process

### 🥇 Automation System / Retainer
**Multiple connected workflows, ongoing build-out.** You become their
"automation person" — new workflows each month, maintenance, optimization.
- **Setup fee:** higher one-time onboarding
- **Retainer:** larger monthly (agreed number of workflows / hours per month)
- **Good for:** agencies, growing businesses, recurring revenue for you

### 📦 Template Product (passive)
Sell a polished workflow JSON as a downloadable product (your site, Gumroad,
n8n's template gallery). Low price per sale — the real money is upselling buyers
into a paid **customization + setup**.

## How to price a custom job (quick method)

1. Estimate build time honestly, then **double it** (testing, revisions, edge cases).
2. Multiply by your target hourly rate → that's your floor.
3. Now sanity-check against **value**: if it saves them 10 hrs/month forever,
   your fee should look small next to that. Price toward the value, not the floor.
4. Always attach a retainer. "I'll keep it running and fix it when something
   upstream changes" is an easy yes.

## What to put in every proposal

- **Scope:** exactly which trigger and actions are included (prevents scope creep).
- **What you need from them:** accounts/credentials, access, sample data.
- **Revisions:** e.g. "2 rounds of revisions included."
- **Ownership:** the workflow runs on *their* n8n; they own their data and credentials.
- **Retainer terms:** what's covered (monitoring, fixes) vs. what's a new paid job
  (new workflows, major changes).

## Sales motion (getting the first client)

1. Find a business doing a repetitive manual task (copying form entries, chasing
   leads, moving data between apps).
2. Offer a **paid pilot** at the Starter tier — low risk for them.
3. Deliver fast (Claude Code + n8n-mcp is your speed advantage), show the time saved.
4. Upsell into Business tier or a retainer once they trust the results.

## Licensing guardrails (stay on the safe side)

- ✅ Building automations for clients on **their own** n8n instance — fine.
- ✅ Selling **workflow templates** (the JSON) — fine.
- ✅ Consulting, setup, retainers, maintenance — fine.
- ⚠️ **Hosting n8n as a service** for clients (multi-tenant / white-label SaaS)
  needs a commercial **embed license** from n8n.io. Contact them before doing this.

When in doubt, keep the automation on an instance the **client owns** and you're
firmly in the clear.
