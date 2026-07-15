<!-- Profile README for TwilightSage94 -->

<div align="center">

```
 ___________       _ __ _       __    __     ______          __
/_  __/ ___/____  (_) /(_)___ _/ /_  / /_   /_  __/__  _____/ /_
 / /  \__ \/ __ \/ / / / / __ `/ __ \/ __/    / / / _ \/ ___/ __ \
/ /  ___/ / /_/ / / / / / /_/ / / / / /_     / / /  __/ /__/ / / /
/_/  /____/ .___/_/_/_/_/\__, /_/ /_/\__/    /_/  \___/\___/_/ /_/
         /_/            /____/
```

### James Destrades Jr.
**AI Engineer | Systems Builder | Founder**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-james--destrades--jr-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/james-destrades-jr)
[![Website](https://img.shields.io/badge/Twilight_Tech-twilighttech.io-00f0ff?style=for-the-badge&logoColor=white)](https://twilighttech.io)
[![Email](https://img.shields.io/badge/Email-james@twilighttech.io-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:james@twilighttech.io)

</div>

---

## The Short Version

I build **private AI that runs on your own hardware** — not chatbots, not demos, not another wrapper around someone else's API. Autonomous systems with self-healing, multi-agent orchestration, and real-time awareness of the machine they live on. Solo engineer. Ship fast. Measure everything.

**Founder of Twilight Tech LLC** (Atlanta, GA) — on-prem AI for firms that can't send client data to a vendor. The box stays in your building. J-Bot runs the business while I build J-Bot.

---

## Flagship: J-Bot — AI OS Layer

> *15 body systems. 25 sensors. 348 tool handlers. 7,767 tests. One developer. 105 days.*

J-Bot is an autonomous AI assistant that operates as an OS layer on Windows. It sees processes, network traffic, security events, USB devices, file changes, GPU state, and display configuration. It correlates signals across domains, self-heals crashed components, hunts threats without being asked, and trains its own apprentice.

<table>
<tr>
<td width="50%" valign="top">

**Architecture**
```
         Twilight Shell (Framework)
                   |
           JBotMetaPack (coordinator)
          /    |      |     \      \
     HackBot  MSP  Finance  Camera  Project
```

- 5 domain packs, hot-swappable via entry points
- Plugin architecture with ABC interfaces
- FastAPI + WebSocket + REST API
- SQLite WAL mode, USB-portable
- One brain, one GPU node, N PWA clients

</td>
<td width="50%" valign="top">

**The Body**
```
Blood .... Unified SignalBus + event sourcing
Heart .... Self-healing watchdog + redundancy
Brain .... Priority intelligence + optimization
Muscles .. DAG pipelines + tool forge
Legs ..... Autonomous goal planning
Hands .... App control + infrastructure-as-code
Immune ... Behavioral detection + threat hunting
DNA ...... Personality evolution + memory
Eyes ..... Screen reading + visual diffing
Ears ..... Audio intelligence + sentiment
Nose ..... Anomaly detection + causal graphs
Gut ...... Prediction + ensemble models
Skeleton . Hot-reload + pack generator
Mouth .... Voice TTS + multi-channel comms
Voice .... Local STT/TTS — zero egress
```

</td>
</tr>
</table>

---

## The Privacy Gate — the reason any of this is sellable

Cloud models are smart. Client data can't go to them. So J-Bot **de-identifies before egress and rehydrates on the way back** — the provider reasons over `[PERSON_1]` and `[ORG_1]` and never learns who they are.

```
"Draft a follow-up to Marcus Delgado at Brightwave Analytics
 (marcus@brightwave.io, 404-555-0182) about the $12,400 retainer."
                       |
                       |  scrub — regex + GLiNER, session-keyed EntityMap
                       v
"Draft a follow-up to [PERSON_1] at [ORG_1]
 ([EMAIL_1], [PHONE_1]) about the [MONEY_1] retainer."
                       |
                       |  the cloud reasons over placeholders
                       |  rehydrate — locally, exactly
                       v
        real names, real numbers, back in your hands
```

**Measured, not asserted:** a live scrub-quality eval scored **9/10** — anonymized queries produced answers equivalent to the raw baseline, with zero leaks and exact rehydration. The one failure was abstractive summarization paraphrasing the placeholders away; fixed with a directive that forces the tokens through.

It **fails toward privacy**: an endpoint it can't positively identify as local gets treated as cloud and scrubbed. Loopback, RFC1918, Tailscale CGNAT and `*.ts.net` are the only things it trusts as "inside."

**Honest about what it is:** this hides **who**, not **what**. The cloud still sees the *shape* of the work — just never the identities. Probabilistic, not provable. That's the real claim, and it's one you can actually make.

---

## Voice — 100% local, zero bytes out

Your voice is the most personal data you have, so none of it leaves the building:

| stage | engine | where | cost |
|---|---|---|---|
| **Hear** | faster-whisper `base` | your metal | $0.00 |
| **Speak** | Piper neural TTS | your metal | $0.00 |

Measured: **100% word recall** including brand names (`J-Bot`, `Twilight Tech`), **~1s** per utterance warm, and both phone codecs decode clean — iPhone AAC/MP4 and Android WebM/Opus. Not scrubbed. **Never sent.**

---

## The Arc: From Fleet to PWA Era

The most instructive thing I built this quarter, I deleted.

**Act I — The Fleet.** Every node ran a full J-Bot instance. Five brains on a Tailscale mesh, kept from double-firing by a single-publisher guard on every cron job. It worked. It was also five things that had to agree with each other.

**Act II — The Collapse.** The installable PWA became the universal client. Once the phone, the tablet and the desktop all opened the same command chair, an instance per node stopped earning its keep. The insight that made it safe: this was a **data move, not a config flip** — the node guards fail *soft*, so a mis-set owner doesn't throw an error, it silently skips. The per-node SQLite had to move first. **Copy → Flip → Verify → Retire.**

**Act III — The PWA Era.** One brain.

```
BEFORE — the Fleet                  AFTER — the PWA era
------------------                  -------------------
5 brains, mesh-synced               1 brain    ->  Prime (all crons, doors, state)
guards to stop double-fires         1 GPU      ->  Tower (Ollama only, no instance)
an instance per node                N clients  ->  phone / tablet / desktop, all equal
```

**What it bought:** the deletion of four brains. The guards stayed — belt-and-suspenders, and free — but the topology stopped being a negotiation. Local inference dispatches to the Tower's GPU over the tailnet; Prime's own CPU never runs transformer inference, because that would block the shared event loop everything else lives on.

**What it taught:** the best architecture change is usually the one that removes nodes. Complexity you delete can't drift, can't desync, and can't lie to you at 3am.

---

## Provider Routing — Local / Hybrid / Cloud

One switch, read per call, live-flippable without a restart:

| mode | behavior |
|---|---|
| **Local** | every tier on your own GPU. **Fails closed** — if the box is unreachable it refuses; it does not quietly call a vendor. |
| **Hybrid** | light + tool work local; heavy reasoning to the cloud, scrubbed by the gate. |
| **Cloud** | all cloud, scrubbed. Fastest. The default. |

**Fail-closed is the whole point.** A silent fallback is the worst possible failure for a product whose promise is *"it stays in the building"* — so local mode would rather answer **"I can't"** than answer **"sure"** from someone else's datacenter.

---

## Sensory Network — 25 Live Adapters

| Layer | Sensors |
|-------|---------|
| **System** | Process monitor, network activity, active window, service monitor, startup programs |
| **Security** | Event log (brute force detection), USB device, screen lock, Windows Defender, firewall |
| **Hardware** | GPU load/temp, hardware inventory, battery/power, display/DPI |
| **Environment** | File watcher, WiFi, audio, productivity tracker, screenshot capture |
| **Business** | Stripe sales feed, calendar, market data, sensory news |

---

## The Mini Arc — J-Bot Trains Its Apprentice

J-Bot doesn't just *use* AI — it **raises** one. The Mini Arc is a multi-phase build where J-Bot teaches a smaller AI ("Twilight") through articulated-rationale lessons captured from every shipped commit, chat session, and decision.

```
Capture  ->  Promote  ->  Teach  ->  Quiz  ->  Score  ->  Iterate
   ^                                                         |
   +------------- autonomous school_cycle cron --------------+
```

A **performance-gated drip** feeds it: score well and the curriculum opens the next batch; score poorly and it re-drills what it has. The teacher only hands over new material when the student has earned it.

---

## A Place To Show Up — the one that isn't infrastructure

Everything above is a system. This one is for people.

**[A Place To Show Up](https://app.aplacetoshowup.com)** is a mobile app for the adults orbiting a kid's life — the aunt, the coach, the neighbor, the family friend — who genuinely mean *"tell me if you need anything"* and never get told. It turns that goodwill into something a caregiver can actually spend: specific, claimable, low-friction ways to show up.

**Currently in public beta.** Passwordless magic-link auth, mobile-first, backend behind a Cloudflare tunnel. Next: the app stores, push, and an attorney review — because software that sits this close to families and kids gets the paperwork done *before* the launch post, not after.

**The part that ties it back:** J-Bot runs its product office. An on-demand desk that tracks the mission, the ledger, and the day's work for a product that isn't J-Bot. The assistant doesn't just maintain the business that builds it — it staffs a second one.

---

## By The Numbers

| Metric | Count |
|--------|-------|
| Python files | **1,279** |
| Python LOC | **491,000+** |
| Automated tests | **7,767** across 384 files |
| Tool handlers | **348** |
| Sensor adapters | **25** |
| Body systems | **15** |
| Domain packs | **5** |
| REST + WS endpoints | **150+** |
| Build time | **105 days** |
| Cloud cost | **$0–10/mo** — and $0.00 for voice |

---

## Tech Stack

**AI Models — tier-routed, multi-provider, vendor-churn-resistant**

![NVIDIA NIM](https://img.shields.io/badge/NVIDIA_NIM-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Anthropic](https://img.shields.io/badge/Claude-CC785C?style=flat-square&logo=anthropic&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama_Local-000000?style=flat-square&logoColor=white)
![Qwen](https://img.shields.io/badge/Qwen3-FF6A00?style=flat-square&logoColor=white)

Five tiers (`light_chat` · `tool_use` · `heavy_reasoning` · `code` · `premium`) resolve to a provider + model per call. Cloud tiers ride NIM; local tiers ride Ollama on the GPU node. Anthropic and local Ollama stand as failover legs.

**Vendors retire models without telling you.** Three of my pinned tiers went `410 Gone` — one had been dead for two months before anyone noticed. So the pins live in env, the fallbacks are per-tier rather than one hardcoded model, and an unrecognized routing mode now says so out loud instead of silently resolving to something nobody chose.

**Backend**

![Python](https://img.shields.io/badge/Python_3.11+-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite_WAL-003B57?style=flat-square&logo=sqlite&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat-square&logo=pwa&logoColor=white)

Plugin architecture, entry-point discovery, circuit breakers, provider failover, exponential backoff, context-window management, semantic caching, ReAct + Reflexion agents, and a BuilderAgent that writes and verifies its own code inside an isolated git worktree.

**Security & Privacy**

![WebAuthn](https://img.shields.io/badge/WebAuthn_Passkeys-3423A6?style=flat-square&logoColor=white)
![Tailscale](https://img.shields.io/badge/Tailscale-000000?style=flat-square&logoColor=white)
![MITRE](https://img.shields.io/badge/MITRE_ATT%26CK-E31837?style=flat-square&logoColor=white)

PII scrub/rehydrate gate on every cloud egress, PIN → revocable session tokens, per-device passkey enrollment, scoped API keys, prompt-injection filtering, per-tool rate limits, immutable audit trail. Purple-team tooling and NIST/HIPAA/PCI scaffolds from the security side of the house.

---

## Also Shipping

| Project | What |
|---------|------|
| **[Twilight Tech](https://twilighttech.io/ai)** | Private AI — the box stays in your building. Cloudflare-hosted. |
| **[A Place To Show Up](https://app.aplacetoshowup.com)** | *(above)* — mobile app turning "let me know if you need anything" into something a caregiver can actually spend. Public beta. |
| **Pulse** | Delta-neutral funding-carry harvester. Directional and market-making were both proven dead first — the pivot *is* the finding. |
| **[CompTIA A+ Study Guides](https://twilighttech.io/guides)** | Core 1 + Core 2 exam prep, sold via Stripe, auto-fulfilled by J-Bot's payment poller. |
| **Twilight Prep** | In-app cert practice engine — 8 exam scaffolds (Sec+, AZ-900, AZ-104, A+ Core 1/2, Net+, CySA+, PenTest+). |
| **J-Bot Origins** | NIM-FLUX-rendered visual story of J-Bot's evolution. |

---

## What I Actually Believe

```python
truth      = "a green check that measures the wrong thing is worse than a red one"
tarmac     = "root-cause fixes over quick patches — lay the best road, not the fastest"
privacy    = "de-identify before egress, or keep it on your own metal. no third option"
receipts   = "measure it, or don't claim it"
complexity = "the best architecture change is the one that removes a node"
```

The hardest bugs I shipped this quarter weren't broken code — they were **things that claimed to work**. A privacy gate wired at three chokepoints that a fourth caller walked around. A daily spend cap that had never once fired. A deploy script that reported success while restarting nothing for two days. A docstring describing an architecture that had been replaced months earlier.

None of them threw an error. All of them lied. **That's the class of bug worth hunting.**

---

## Current Focus

```python
building   = "Private AI — on-prem boxes for firms that can't use the cloud"
proving    = "local-first inference: scrub what leaves, keep the rest on your own GPU"
shipping   = "A Place To Show Up (public beta) + CompTIA guides via Stripe"
training   = "Twilight (Mini AI) — autonomous study from books, commits, decisions"
available  = "Twilight Tech LLC — private AI builds, AI advisory, security assessments"
```

<div align="center">

*Atlanta, GA · Building in public · [twilighttech.io](https://twilighttech.io)*

</div>
