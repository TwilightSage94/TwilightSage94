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

> *14 body systems. 19 sensors. 103 tool handlers. 3,623 tests. One developer. 14 days.*

J-Bot is an autonomous AI assistant that operates as an OS layer on Windows. It sees processes, network traffic, security events, USB devices, file changes, GPU state, and display configuration. It correlates signals across domains, self-heals crashed components, and hunts threats without being asked.

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
- SQLite WAL mode, zero cloud dependencies

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
Mouth .... Voice TTS + toast notifications
```

</td>
</tr>
</table>

### Sensory Network — 19 Live Adapters

| Layer | Sensors |
|-------|---------|
| **System** | Process monitor, network activity, active window, service monitor, startup programs |
| **Security** | Event log (brute force detection), USB device (mass storage alerts), screen lock, Windows Defender, firewall |
| **Hardware** | GPU load/temp, hardware inventory, battery/power, display/DPI |
| **Environment** | File watcher, WiFi, audio, productivity tracker, screenshot capture |

### Two-Node Distributed System

```
Prime (Laptop) ←——— Tailscale Bridge ———→ Server (Always-On)
   dev + build          heartbeat            production
   19 sensors          command relay          24/7 uptime
   desktop presence    vault sync             API serving
```

<div align="center">

**[View Repository →](https://github.com/TwilightSage94/j-Bot)**

</div>

---

## Specialist: HackBot — Deployable Security Sentinel

> *Purple-team AI agent, forged into a deployable security platform. J-Bot's security-specialist domain pack, now shipping as its own product.*

While J-Bot runs as my AI OS layer, **HackBot** has crossed over into a deployable product. It's a Docker-packaged security sentinel that plugs into a client's network, learns what normal looks like, and responds to anomalies with tiered autonomy.

<table>
<tr>
<td width="50%" valign="top">

**What It Does**
- Per-client behavioral baselines — time-aware anomaly detection
- Tiered autonomous response (AUTO / CONFIRM / MANUAL) with kill switch
- Attack forecasting — breach risk, CVE exploitation timelines, MITRE kill-chain progression
- Multi-channel alerting — Email, Slack, Telegram, PagerDuty, custom webhooks
- Compliance mapping — NIST 800-53, PCI-DSS, HIPAA, SOC 2
- Self-healing watchdog over every security service

</td>
<td width="50%" valign="top">

**How It Ships**
```
     HackBot Server (central)
        ↓ HTTPS + API key
   ┌────┴────┬─────────┐
   │         │         │
Client A  Client B  Client C
Collector Collector Collector
  (Docker)
```

- Multi-tenant auth, per-client isolation
- FastAPI + WebSocket + live operator dashboard
- SQLite WAL persistence, zero cloud dependencies
- 511 fusion tests, boring-tech stack on purpose

</td>
</tr>
</table>

<div align="center">

**[View HackBot Repository →](https://github.com/TwilightSage94/HackBot)**

</div>

---

## By The Numbers

| Metric | Count |
|--------|-------|
| Python files | **739** |
| Lines of code | **296,000+** |
| Automated tests | **3,623 (100% pass)** |
| Tool handlers | **103** |
| Sensor adapters | **19** |
| Body systems | **14** |
| Domain packs | **5** |
| REST + WS endpoints | **138+** |
| Build time | **14 days** |
| Cloud cost | **$0** |

---

## Tech Stack

**AI & Agents**

![Anthropic](https://img.shields.io/badge/Claude-CC785C?style=flat-square&logo=anthropic&logoColor=white)
![OpenAI](https://img.shields.io/badge/GPT--4o-412991?style=flat-square&logo=openai&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama_Local-000000?style=flat-square&logoColor=white)

ReAct loop, reflexion engine, multi-agent orchestration (parallel, pipeline, debate, race), semantic routing, adaptive prompts, confidence scoring, hallucination detection

**Backend**

![Python](https://img.shields.io/badge/Python_3.11+-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite_WAL-003B57?style=flat-square&logo=sqlite&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logoColor=white)

Plugin architecture, entry-point discovery, circuit breakers, provider failover, exponential backoff, context window management, semantic caching

**Security**

![MITRE](https://img.shields.io/badge/MITRE_ATT%26CK-E31837?style=flat-square&logoColor=white)
![CompTIA](https://img.shields.io/badge/CompTIA_A+-C8202F?style=flat-square&logoColor=white)

Purple team tooling, compliance frameworks, Windows event log analysis, behavioral threat detection, dark web monitoring

**Infrastructure**

![Tailscale](https://img.shields.io/badge/Tailscale-000000?style=flat-square&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)

Two-node bridge, vault sync, Windows service integration, system tray, global hotkeys, auto-start

---

## Also Shipping

| Project | What |
|---------|------|
| **[Twilight Tech Website](https://twilighttech.io)** | MSP + cybersecurity services, Cloudflare-hosted |
| **[CompTIA A+ Study Guides](https://twilighttech.io/guides)** | Complete Core 1 + Core 2 exam prep, selling via Stripe |
| **J-Bot Origins** | 14-issue comic book series documenting the AI's evolution |

---

## Current Focus

```python
building   = "J-Bot AI OS Layer — system awareness, always-on presence"
shipping   = "CompTIA A+ Study Guides via Stripe"
seeking    = "AI Engineer / ML Platform roles (remote)"
available  = "Contract work via Twilight Tech LLC"
```

---

<div align="center">

> *"J-Bot doesn't run on the computer. J-Bot is the computer."*

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=TwilightSage94&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true)](https://github.com/TwilightSage94)

<sub>Twilight Tech LLC | Atlanta, GA | Solo Engineer</sub>

</div>
