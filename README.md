# Mel · he/him

Building **PC Brain** — a local-first AI operating layer for Windows.

The idea: bring your own LLM, run it on your hardware, and have it be the surface where your agent acts, remembers, and refuses. No cloud round-trips. No data leaving the box. Your model gets categorically smarter as you train it; PC Brain is the structure around it.

---

## The trio

```
PC Brain     — the agent that runs
    │
    ├──► Cerebra   the observatory · what your agent knows
    │
    └──► Atelier   the workshop · where you shape its voice
```

Three apps. One nervous system.

**PC Brain** is the runtime. **Cerebra** visualizes the vault your agent reasons against — in 3D, navigable, lobed. **Atelier** is the operator's seat where you design personas, run scenarios, dispatch training, and watch the closed loop close.

---

## The product family

| Repository | What it is | Stack | Status |
|---|---|---|---|
| 🔒 [**PC-Brain**](https://github.com/meloliva14/PC-Brain) | The agent runtime · BYOK · local-first · single-action discipline | Python | Private · v2.1 · EV-signed |
| 🔒 [**PC-Brain-Cerebra**](https://github.com/meloliva14/PC-Brain-Cerebra) | The 3D vault observatory + LLM cockpit | Electron · TypeScript · three.js | Private · v1.5.0 |
| 🔒 [**PC-Brain-Atelier**](https://github.com/meloliva14/PC-Brain-Atelier) | The operator's workshop · 6 rooms · closed-loop ship wizard | Electron · TypeScript · React | Private · v0.3.0 |
| 🔒 [**PC-Brain-Trio**](https://github.com/meloliva14/PC-Brain-Trio) | Shared JSON schemas, integration proposals, brain-renderer | TypeScript · JSON Schema | Private · v1.0.0 |
| 🔒 [**PC-Brain-Mobile**](https://github.com/meloliva14/PC-Brain-Mobile) | Mobile companion (queued) | TypeScript | Private |
| 🌐 [**PCBrain-Landing**](https://github.com/meloliva14/PCBrain-Landing) | Product landing page | HTML | Public |

Code stays private until launch. Public is intentional, not accidental.

---

## Currently

Building the trio's connective tissue. Decision logs flowing. Voice grading live. Closed-loop ship wizard in Atelier v0.3. RunPod control warm. PC Brain side: v2.1 EV-signed, queued for the trio integration handoff.

---

## VerityLayer

Independent, fail-closed verification for AI agents — a signed second opinion right before an agent does something irreversible. Fact-check a claim, screen untrusted text for prompt-injection, or gate an action: **allow / review / block**. Every verdict is Ed25519-signed and independently re-verifiable, forever.

Live and pay-per-call over x402 (USDC on Base) — no accounts, no subscriptions.

| Where | What |
|---|---|
| 🌐 [**veritylayer.dev**](https://veritylayer.dev) | the product · [manifesto](https://veritylayer.dev/manifesto) |
| 📦 [**verity-guard**](https://github.com/meloliva14/verity-guard) | one-line guard — LangGraph · CrewAI · OpenAI Agents SDK · Vercel AI SDK (`pip install verity-guard` · `npm i @veritylayer/guard`) |
| 🔌 [**verity-mcp**](https://github.com/meloliva14/verity-mcp) | MCP server — agents discover and call it as a tool |

**In the open —** root-caused a silent, ecosystem-wide x402 payment regression: an undocumented **500-character cap** on `resource.description` in Coinbase's CDP facilitator, isolated with free unfunded-key probing and delta-debugged to the exact boundary. Confirmed by a core x402 maintainer; the CDP team updated their docs as a result.

- [Root-cause investigation → #2832](https://github.com/x402-foundation/x402/issues/2832) — closed as completed, maintainer-confirmed
- [Signed lib-side PR → #2837](https://github.com/x402-foundation/x402/pull/2837) — opt-in interop fix, thanked by the maintainers

---

## Links

- **[pcbrain.ai](https://pcbrain.ai)** — product surface
- **[veritylayer.dev](https://veritylayer.dev)** — the trust layer for AI agents
- meloliva14 at yahoo dot com — inquiries

---

*Architected from New Jersey. Built quietly. Shipping when it's right.*
