# Mel · he/him

Independent engineer. I ship production systems solo — AI agent infrastructure, local-first AI, and field-service SaaS.

New Jersey.

---

## 🔎 x402 · machine-payable HTTP

Contributor to [**x402-foundation/x402**](https://github.com/x402-foundation/x402), the open standard for agent-to-server payments.

**I run a daily, signed, append-only census of the network.**

→ [**x402-measure**](https://github.com/meloliva14/x402-measure) — 1,521 hosts, one unauthenticated request each. No wallet, no key, nothing ever paid. Every day's observation is Ed25519-signed and verifies against a published key with a short, dependency-free verifier. **Eighteen consecutive days as of 2026-08-25, no gaps.**

What it has found, every figure dated and recomputable from the repo:

- **91.3%** of payment-gated hosts are fully conformant (1,211 of 1,326, 2026-08-25; it read 91.6% on 2026-08-16). The network is in better shape than the discourse suggests.
- **972 of 1,521** hosts publish a discovery manifest. **Zero** of them serve a cryptographically signed one.
- **811** gated hosts answered with a payout address, resolving to **379** distinct addresses. One address serves **144** hosts, so counting sellers per host overstates badly. Counting the other way is worse: a shared address does not establish a shared operator, so distinct addresses is neither a ceiling nor a floor on distinct parties.

**The instrument gets audited too, in public.** A failed fetch can only move a host toward `UNREACHABLE` and never toward `OK`, so transport failure invents state transitions and never hides them. That bias put two wrong numbers into my own published figures before I caught it. I corrected both on the thread with the hosts named, replaced the hand-count with [`flap_census.py`](https://github.com/meloliva14/x402-measure/blob/main/flap_census.py) (46 flap events across 38 hosts in 18 days, 92 recorded transitions that are not state changes), and shipped a retry rule so the sweep stops manufacturing them. Every observation carries a hash of the method, and that hash moves when the method moves, so a reader can separate a method change from a network change without asking me.

That habit is why the numbers get used. The rule it produced, that a signed observation is evidence the issuer observed something and never that the observation was correct, has been taken up by other implementers in the Foundation's [evidence-record working group](https://github.com/x402-foundation/tsc/issues/4). One of them applied it to a problem I never touched, comparing two canonicalization schemes rather than probing hosts, found the same one-directional error there, and rewrote a rule in their own specification to it.

Figures from the census are cited in the discovery specification work ([PR #2979](https://github.com/x402-foundation/x402/pull/2979)) by the author of the IETF Internet-Draft on x402 DNS discovery, who now runs a second independent observer against the same pinned host list so the two columns can be diffed daily.

Three open submissions in the x402 Foundation identity working group:
[#14](https://github.com/x402-foundation/wg-identity/issues/14) what is measurably checkable about a payee and why none of it is identity ·
[#15](https://github.com/x402-foundation/wg-identity/issues/15) how grouping by shared payout address launders an attribution claim ·
[#16](https://github.com/x402-foundation/wg-identity/issues/16) DNS TXT key authorization, verified against a live implementation as an unrelated third party

**Root-caused a silent, ecosystem-wide payment regression.** Coinbase's CDP facilitator had begun rejecting spec-compliant x402 v2 payloads with an opaque `400 invalid_request`. I isolated it to an **undocumented 500-character cap** on `resource.description` — probing with free unfunded keys, then delta-debugging to the exact boundary. Confirmed by a core maintainer; the CDP team updated their documentation as a result.

→ [**issue #2832**](https://github.com/x402-foundation/x402/issues/2832) — closed as completed, maintainer-confirmed · 20 comments
→ [PR #2837](https://github.com/x402-foundation/x402/pull/2837) — opt-in interop hardening for strict facilitators

I also work on client-side payment hardening (spend caps, chain pinning, asset pinning) and file ecosystem bug reports where I find them.

The census also answers the question a seller cannot answer from their own funnel: *did nobody want it, or could nobody pay?* Those look identical from the inside and have completely different fixes.

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
