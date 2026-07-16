# Mel · he/him

Building **PC Brain** — a local-first AI operating layer for Windows.

The idea: bring your own LLM, run it on your hardware, and let it be the surface where your agent acts, remembers, and refuses. No cloud round-trips. No data leaving the box. Your model gets categorically smarter as you use it; the software is the structure around it.

---

## 🚀 Shipping in public

### 🧠 [Cerebra](https://github.com/meloliva14/cerebra) — your Obsidian vault as a living 3D brain

Renders a knowledge vault as a navigable 3D brain: semantic UMAP layout, HDBSCAN lobes, a grounded local-LLM you can chat with (it cites the real pages), and cinematic in-app tours. Clone it and fly through your own notes — runs 100% local.
`Electron · React · three.js · Python`

### 🛡️ [VerityLayer](https://veritylayer.dev) — the trust layer for AI agents

Independent, fail-closed verification — a signed second opinion right before an agent does something irreversible. Fact-check a claim, screen untrusted text for prompt-injection, or gate an action: **allow / review / block**. Every verdict is Ed25519-signed and independently re-verifiable, forever. Live and pay-per-call over x402 (USDC on Base) — no accounts, no subscriptions.

| | |
|---|---|
| 🌐 [**veritylayer.dev**](https://veritylayer.dev) | the product · [manifesto](https://veritylayer.dev/manifesto) |
| 📦 [**verity-guard**](https://github.com/meloliva14/verity-guard) | one-line guard — LangGraph · CrewAI · OpenAI Agents SDK · Vercel AI SDK (`pip install verity-guard` · `npm i @veritylayer/guard`) |
| 🔌 [**verity-mcp**](https://github.com/meloliva14/verity-mcp) | MCP server — agents discover and call verification as a tool |

### 🌐 [pcbrain.ai](https://pcbrain.ai) — PC Brain's product surface  ·  [source](https://github.com/meloliva14/PCBrain-Landing)

---

## 🔒 PC Brain — the flagship (private, in active development)

A Windows-first agent that runs on your own hardware and brings no inference of its own — you bring the LLM (BYOK), it brings the structure: a standing team of specialists, a plan-before-act discipline, a five-level risk model, an append-only audit log, and memory that compounds. Companion apps for visualizing and authoring the agent are in private development alongside it.

Shipping quietly at v2.1 (EV-signed). Public when it's right — intentional, not accidental.

---

## 🔎 In the open

Root-caused a silent, ecosystem-wide x402 payment regression: an undocumented **500-character cap** on `resource.description` in Coinbase's CDP facilitator — isolated with free unfunded-key probing and delta-debugged to the exact boundary. Confirmed by a core x402 maintainer; the CDP team updated their docs as a result.

- [Root-cause investigation → #2832](https://github.com/x402-foundation/x402/issues/2832) — closed as completed, maintainer-confirmed
- [Signed lib-side PR → #2837](https://github.com/x402-foundation/x402/pull/2837) — opt-in interop fix, thanked by the maintainers

---

## Links

- **[pcbrain.ai](https://pcbrain.ai)** — PC Brain
- **[veritylayer.dev](https://veritylayer.dev)** — the trust layer for AI agents
- meloliva14 at yahoo dot com — inquiries

---

*Architected from New Jersey. Built quietly. Shipping when it's right.*
