# Free n8n templates — by AkuchiS

Production-shaped n8n workflows you can import and use. **Core nodes only, no community packages, no embedded secrets** — and every one is validated import-clean with FlowProof (verdicts arbitrated against a live n8n import).

| Template | What it does | FlowProof |
|----------|--------------|-----------|
| **Daily RSS → Email Digest** (`daily-rss-email-digest.json`) | Every morning, read an RSS feed, take the top items, build an HTML digest, email it. | IMPORTABLE · 100/100 · 0 blockers |
| **Webhook Input-Validation API** (`webhook-input-validation-api.json`) | Turn an incoming webhook into a tiny JSON API: validate the payload, respond `200` on success or `400` with an error. | IMPORTABLE · 100/100 · 0 blockers |

## Use any of them
1. Download the `.json`.
2. In n8n: **Workflows → Import from File**.
3. Fill in the obvious bits (feed URL, SMTP credential, etc.) and activate.

## Why each one says "100/100"
Most shared n8n templates *don't* import cleanly — leaked credentials, missing community nodes, version drift, and broken connections are the norm. Before you ship a workflow to a client (or trust one you downloaded), check it:

- **FlowProof free CLI** (MIT, offline, no API keys): <https://github.com/AkuchiS/flowproof>
  ```bash
  flowproof check your-workflow.json
  ```
- **FlowProof Pro** repairs it and hands you an import-ready file + a content-hashed "FlowProof Checked" certificate + a client-ready handover.

---
*[AkuchiS](https://github.com/AkuchiS) tools, operated by DIME. Private-by-design — they run on your machine; we host nothing and see no data.*
