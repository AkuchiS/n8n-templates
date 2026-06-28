# Free n8n templates — by AkuchiS

[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-8A2BE2)](https://github.com/sponsors/AkuchiS)
[![License](https://img.shields.io/github/license/AkuchiS/n8n-templates?color=8A2BE2)](LICENSE)
[![Last commit](https://img.shields.io/github/last-commit/AkuchiS/n8n-templates?color=8A2BE2)](https://github.com/AkuchiS/n8n-templates/commits)
[![Stars](https://img.shields.io/github/stars/AkuchiS/n8n-templates?color=8A2BE2)](https://github.com/AkuchiS/n8n-templates/stargazers)

Production-shaped n8n workflows you can import and use. **Core nodes only, no community packages, no embedded secrets** — and every one is validated import-clean with FlowProof (verdicts arbitrated against a live n8n import).

| Template | What it does | FlowProof |
|----------|--------------|-----------|
| **Daily RSS → Email Digest** (`daily-rss-email-digest.json`) | Every morning, read an RSS feed, take the top items, build an HTML digest, email it. | IMPORTABLE · 100/100 |
| **Webhook Input-Validation API** (`webhook-input-validation-api.json`) | Turn an incoming webhook into a tiny JSON API: validate the payload, respond `200` on success or `400` with an error. | IMPORTABLE · 100/100 |
| **Uptime Monitor → Email Alert** (`uptime-monitor-email-alert.json`) | Every 15 min, hit an endpoint; if it returns ≥ 400, email you an alert. | IMPORTABLE · 100/100 |
| **Webhook → Google Sheets Logger** (`webhook-to-google-sheets-logger.json`) | Append every webhook payload as a row in a Google Sheet, then respond. | IMPORTABLE · 100/100 |

## Use any of them
1. Download the `.json`.
2. In n8n: **Workflows → Import from File**.
3. Fill in the obvious bits (feed URL, SMTP / Google credential, the endpoint to watch, etc.) and activate.

## Why each one says "100/100"
Most shared n8n templates *don't* import cleanly — leaked credentials, missing community nodes, version drift, and broken connections are the norm. Before you ship a workflow to a client (or trust one you downloaded), check it:

- **FlowProof free CLI** (MIT, offline, no API keys): <https://github.com/AkuchiS/flowproof>
  ```bash
  flowproof check your-workflow.json
  ```
- **FlowProof for n8n** runs this check *inside* n8n so you can gate a deploy: [n8n-nodes-flowproof](https://github.com/AkuchiS/n8n-nodes-flowproof).
- **FlowProof Pro** repairs it and hands you an import-ready file + a content-hashed "FlowProof Checked" certificate + a client-ready handover: [fp.akuchis.com](https://fp.akuchis.com).

---
<sub>[AkuchiS](https://github.com/AkuchiS) tools · more at [github.akuchis.com](https://github.akuchis.com). Private-by-design — they run on your machine; we host nothing and see no data.</sub>
