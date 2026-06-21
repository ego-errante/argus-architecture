# Argus — Architecture Document

The standalone architecture document for **Argus**, a Solana smart-transaction stack built for the
Superteam Nigeria *Advanced Infrastructure Challenge*.

- **Live document:** _(Cloudflare Pages URL — added after first deploy)_
- **Code repository:** <https://github.com/ego-errante/argus>

It is a single self-contained `index.html` (diagrams via the Mermaid CDN, no build step). Open it
directly in a browser, or serve the folder:

```bash
python3 -m http.server 8099
# then visit http://127.0.0.1:8099/
```

## Contents

Covers the six required sections — system architecture, key components, data flow between services,
infrastructure decisions, failure-handling strategy, and AI-agent responsibilities — plus a thesis
introduction, an operational-evidence section (answering the three README questions from a real
mainnet run), and an ADR index.

## Deploy (Cloudflare Pages)

```bash
npx wrangler pages deploy ./ --project-name argus-architecture
```
