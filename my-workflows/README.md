# My n8n Workflows — Client Automation Business

This directory is your **inventory and delivery system** for selling n8n
automations to clients. It is intentionally separate from the `n8n-mcp` source
code in the rest of this repo — nothing here touches that project.

## Folder structure

```
my-workflows/
├── README.md                  ← you are here
├── PRICING.md                 ← packaging & pricing outline for clients
├── templates/                 ← your reusable products (build once, resell many times)
│   └── lead-capture-notification/
│       ├── workflow.json      ← the importable n8n workflow
│       └── README.md          ← what it does + client setup guide
└── clients/                   ← one folder per paying client
    └── _TEMPLATE/             ← copy this to start a new client
        └── README.md
```

## The core idea

- **`templates/`** holds your *products* — generic, reusable workflows. You build
  a workflow once, keep the JSON here under version control, and adapt a copy for
  each client. This is your intellectual property and your competitive edge.
- **`clients/`** holds one folder per client — the *specific* customized version
  you delivered to them, plus notes (what they wanted, their quirks, what you charged).

## How you actually work

1. **Build or pick a template** in `templates/`.
2. **Copy it into a client folder** under `clients/<client-name>/` and customize
   (their Slack channel, their sheet, their API, etc.).
3. **Deploy** — either onto the client's own n8n instance, or hand them the
   `workflow.json` to import themselves (Import from File in n8n).
4. **Commit** the customized version so you have a record of exactly what you shipped.

## Deploying with Claude Code + n8n-mcp

Because you have n8n-mcp connected, you can deploy straight from a Claude Code
session pointed at a running n8n instance:

> "Take `my-workflows/templates/lead-capture-notification/workflow.json`,
>  adapt it for a client whose CRM is HubSpot, validate it, and deploy it to n8n."

Claude will use `validate_workflow` and `n8n_create_workflow` to push it live.

## Important: credentials are never stored here

n8n exports workflows **without** credential secrets — only references. Each
client supplies their own API keys/logins inside *their* n8n instance. Never
commit real API keys, tokens, or passwords into this repo.

## Licensing reminder

n8n is fair-code (Sustainable Use License). Building automations for clients and
selling workflow templates is fine. Hosting n8n **as a service** for others
(multi-tenant SaaS / white-label) needs a commercial embed license from n8n.io —
talk to them first if you go that route. See `PRICING.md` for the safe models.
