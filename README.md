# Argus — Architecture Document

The standalone architecture document for **Argus**, a Solana smart-transaction stack built for the
Superteam Nigeria *Advanced Infrastructure Challenge*.

- **Live document:** <https://argus-architecture.pages.dev/>
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

It is **interactive**, driven by the real graded-run data embedded inline:

- a **lifecycle explorer** of all 15 submissions — landed rows link the slot *and* the transaction
  on Solscan and show the commitment deltas to scale; faulted rows expand to the agent's diagnosis,
  triage, and full reasoning trace;
- a **failure explorer** that lets you step through each program error and watch the four-class
  baseline stay blind while the agent reasons out a distinct cause;
- a **to-scale lifecycle timeline** contrasting the ~123 ms processed→confirmed delta with the
  ~12.2 s confirmed→finalized wait.

## Deploy

The live document is hosted on Cloudflare, connected to this repository — a push to `main`
auto-deploys. To deploy a copy manually:

```bash
npx wrangler pages deploy ./ --project-name argus-architecture
```
