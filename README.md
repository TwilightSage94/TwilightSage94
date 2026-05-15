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

I build **AI systems that run as infrastructure** — not chatbots, not demos. Autonomous platforms with self-healing, multi-agent orchestration, and real-time system awareness. Solo engineer. Ship fast. Test everything.

**Founder of Twilight Tech LLC** — managed IT and cybersecurity for small businesses in Atlanta, GA. J-Bot runs the business while I build J-Bot.

---

## Flagship: J-Bot — AI OS Layer

> *14 body systems. 23 sensors. 221 tool handlers. 4,672 tests. One developer. 44 days.*

J-Bot is an autonomous AI assistant that operates as an OS layer on Windows. It sees processes, network traffic, security events, USB devices, file changes, GPU state, and display configuration. It correlates signals across domains, self-heals crashed components, hunts threats without being asked, and increasingly **trains its own apprentice**.

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
- Multi-node fleet over Tailscale

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
```

</td>
</tr>
</table>

### Sensory Network — 23 Live Adapters

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
Capture  →  Promote  →  Teach  →  Quiz  →  Score  →  Iterate
   ↑                                                      |
   └─────────── autonomous school_cycle cron ─────────────┘
```

| Phase | What | Status |
|---|---|---|
| 1 — Curriculum schema | Lessons table, capture engine, citation requirements | ✅ shipped |
| 2 — Mini "Twilight" born | Persona, private memory, ask/quiz/teach channels, AI School dashboard at `/school` | ✅ shipped |
| 3 — Scholarly training | Cited-fact schema, accredited-source allowlist, tier-graded retention | ✅ shipped |
| 4 — Autonomous study | Cron-driven teach + quiz + wisdom score, twice daily on Prime | ✅ shipped |
| 5 — Multi-device sync | Same Twilight identity across phone + tablet + desktop instances | 🔧 in flight |
| 6 — Mentor rank | Mature Mini spawning child Minis for clients | 🔭 next |

---

## Multi-Node Fleet

```
Prime (canonical state)  ←————— Tailscale mesh —————→  4 satellite nodes
   testmachine                                              DC, Surface, Tower, Phone
   - Mini state holder                                      - Mobile workstation (DC)
   - school_cycle owner                                     - Touch-first chat (Surface, Tauri)
   - Telegram bot polling                                   - Daily-driver dev (Tower)
   - Stripe fulfillment                                     - Mini #1 deployment (Phone)
```

**Single-publisher guard pattern** prevents double-firing across nodes — each cron job has a designated owner; satellite nodes log "skipped, not the owner" and bail.

---

## Autonomous Loops Running

| Cron | Cadence | What it does | Owner |
|---|---|---|---|
| `school_cycle` | 7 AM + 7 PM | Twilight studies new lessons + takes quizzes | Prime |
| `scheduled_post_publisher` | Every 5 min | Drains scheduled social posts → LinkedIn / FB / IG | Surface |
| `stripe_fulfillment_check` | Every minute (adaptive) | Polls Stripe → emails buyers their guides | Prime |
| `journal_today` | Nightly | Pulls real chat-history themes + commits + calendar → daily entry | Prime |
| `sla_compliance_check` | Every 15 min | MSP ticket SLA monitoring | Prime |
| `daily_briefing` | 11 AM | Cross-domain morning brief | Prime |

---

## By The Numbers

| Metric | Count |
|--------|-------|
| Python files | **927** |
| Lines of code | **366,000+** |
| Automated tests | **4,672 (passing)** |
| Tool handlers | **221** |
| Sensor adapters | **23** |
| Body systems | **14** |
| Domain packs | **5** |
| REST + WS endpoints | **150+** |
| Build time | **44 days** |
| Cloud cost | **$0–10/mo (NIM cloud + APIs)** |

---

## Tech Stack

**AI Models — NVIDIA NIM (primary brain) + multi-provider failover**

![NVIDIA NIM](https://img.shields.io/badge/NVIDIA_NIM-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Anthropic](https://img.shields.io/badge/Claude-CC785C?style=flat-square&logo=anthropic&logoColor=white)
![Meta](https://img.shields.io/badge/Llama_3.3-0467DF?style=flat-square&logo=meta&logoColor=white)
![Qwen](https://img.shields.io/badge/Qwen3_Coder_480B-FF6A00?style=flat-square&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama_Local-000000?style=flat-square&logoColor=white)

Task-tier routing across Nemotron-3 (default), Llama-3.3-70B (light), Qwen3-Coder-480B (code), Qwen3.5-397B (premium reasoning), Llama-3.2-Vision (multimodal), FLUX-schnell (image gen). Anthropic Claude + local Ollama as failover legs.

**Backend**

![Python](https://img.shields.io/badge/Python_3.11+-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite_WAL-003B57?style=flat-square&logo=sqlite&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logoColor=white)
![Tauri](https://img.shields.io/badge/Tauri_2-FFC131?style=flat-square&logo=tauri&logoColor=black)

Plugin architecture, entry-point discovery, circuit breakers, provider failover, exponential backoff, context window management, semantic caching, ReAct + Reflexion agents, BuilderAgent autonomous code-write loop.

**Security**

![MITRE](https://img.shields.io/badge/MITRE_ATT%26CK-E31837?style=flat-square&logoColor=white)
![CompTIA](https://img.shields.io/badge/CompTIA_Sec+-C8202F?style=flat-square&logoColor=white)

Purple-team tooling, compliance frameworks (NIST/HIPAA/PCI scaffolds), Windows event log analysis, behavioral threat detection, dark-web monitoring, security assessment as a lead-magnet.

**Infrastructure**

![Tailscale](https://img.shields.io/badge/Tailscale-000000?style=flat-square&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)

5-node fleet over Tailscale mesh, vault sync, Windows service integration, system tray, global hotkeys, auto-start, single-publisher guard for multi-node cron safety.

---

## Also Shipping

| Project | What |
|---------|------|
| **[Twilight Tech Website](https://twilighttech.io)** | MSP + cybersecurity + AI consulting services. Cloudflare-hosted. |
| **[CompTIA A+ Study Guides](https://twilighttech.io/guides)** | Core 1 + Core 2 exam prep, sold via Stripe. Auto-fulfilled by J-Bot's Stripe poller. |
| **Twilight Prep** | In-app cert practice engine — 8 exam scaffolds (Sec+, AZ-900, AZ-104, A+ Core 1/2, Net+, CySA+, PenTest+) with 304 reverse-engineered Sec+ MCQs |
| **J-Bot Origins (Comic Series)** | 21-issue NIM-FLUX-rendered visual story of J-Bot's evolution. Tue/Thu drops on LinkedIn / Facebook / Instagram. |
| **TraderBot** *(in flight)* | Algo-trading bot built on Alpaca paper-trading sandbox. Five-phase build: paper → backtest → eval → tiny live → investment suggester. |

---

## Current Focus

```python
building   = "TraderBot — Phase 1 paper trading on Alpaca"
training   = "Twilight (Mini AI) — autonomous study cycle from books + commits"
shipping   = "Daily comic series + CompTIA A+ Study Guides via Stripe"
seeking    = "AI Engineer / ML Platform roles (remote) + contract work"
available  = "Twilight Tech LLC — MSP + cybersecurity + AI consulting"
```

---

<div align="center">

> *"J-Bot doesn't run on the computer. J-Bot is the computer."*

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=TwilightSage94&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true)](https://github.com/TwilightSage94)

<sub>Twilight Tech LLC | Atlanta, GA | Solo Engineer</sub>

</div>
