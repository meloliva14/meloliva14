# Mel · he/him

Independent engineer. I ship production systems solo — AI agent infrastructure, local-first AI, and field-service SaaS.

New Jersey.

---

## 🔎 x402 · machine-payable HTTP

Contributor to [**x402-foundation/x402**](https://github.com/x402-foundation/x402), the open standard for agent-to-server payments.

**Root-caused a silent, ecosystem-wide payment regression.** Coinbase's CDP facilitator had begun rejecting spec-compliant x402 v2 payloads with an opaque `400 invalid_request`. I isolated it to an **undocumented 500-character cap** on `resource.description` — probing with free unfunded keys, then delta-debugging to the exact boundary. Confirmed by a core maintainer; the CDP team updated their documentation as a result.

→ [**issue #2832**](https://github.com/x402-foundation/x402/issues/2832) — closed as completed, maintainer-confirmed · 20 comments
→ [PR #2837](https://github.com/x402-foundation/x402/pull/2837) — opt-in interop hardening for strict facilitators

I also work on client-side payment hardening (spend caps, chain pinning, asset pinning), file ecosystem bug reports where I find them, and measure the network **on-chain** rather than trusting dashboards.

---

## 🛡️ VerityLayer · verification for AI agents

An independent, fail-closed second opinion immediately before an agent does something irreversible. Fact-check a claim, screen untrusted text for prompt-injection, or gate an action — **allow / review / block**. Every verdict is Ed25519-signed and **independently re-verifiable offline** against a published key, so you never have to trust the issuer. Pay-per-call over x402 (USDC on Base) — no accounts, no subscriptions.

| | |
|---|---|
| 🌐 [**veritylayer.dev**](https://veritylayer.dev) | the product · [manifesto](https://veritylayer.dev/manifesto) |
| 📦 [**verity-guard**](https://github.com/meloliva14/verity-guard) | one-line guard — LangChain · LangGraph · CrewAI · OpenAI Agents · Vercel AI SDK<br>`pip install verity-guard` · `npm i @veritylayer/guard` |
| 🔌 [**verity-mcp**](https://github.com/meloliva14/verity-mcp) | MCP server — agents discover and call verification as a tool |
| ⛓️ **@veritylayer/openclaw-plugin** | OpenClaw `before_tool_call` hook — enforcement in the tool-call path, where it can't be skipped |

Published across PyPI, npm, and ClawHub. The rule the whole design holds to: **a missing verdict is never permission.** If the check didn't happen, the caller is told exactly that — it never renders as an allow.

---

## 🧠 Cerebra · your Obsidian vault as a living 3D brain

Renders a knowledge vault as a navigable 3D brain: semantic UMAP layout, HDBSCAN lobes, a grounded local LLM you can chat with (it cites the real pages), and cinematic in-app tours. Clone it and fly through your own notes — runs 100% local.

`Electron · React · three.js · Python` — [source](https://github.com/meloliva14/cerebra)

---

## 🔧 Also building

**PC Brain** — a local-first AI operating layer for Windows. Bring your own model; it runs on your hardware, and your data never leaves the box. In active private development.
→ [pcbrain.ai](https://pcbrain.ai) · [landing source](https://github.com/meloliva14/PCBrain-Landing)

**Field-service SaaS** — a full operations platform for a service trade: scheduling, routing, billing, and native iOS + Android apps for crews in the field. Private.

**Websites** — design and build, start to finish.

---

*Most of what I build is fail-closed by default: when a system can't verify something, it should say so rather than guess.*

meloliva14 at yahoo dot com — inquiries
