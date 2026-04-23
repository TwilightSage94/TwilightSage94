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
**AI Engineer | Systems Builder | Founder — Twilight Tech LLC**

[![Website](https://img.shields.io/badge/twilighttech.io-00f0ff?style=for-the-badge&logoColor=white)](https://twilighttech.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-james--destrades--jr-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/james-destrades-jr)
[![Email](https://img.shields.io/badge/james@twilighttech.io-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:james@twilighttech.io)

</div>

---

## The Short Version

I build **AI systems that run as infrastructure** — not chatbots, not demos. Autonomous platforms with self-healing, multi-agent orchestration, and real-time system awareness. Solo engineer. Ship fast. Test everything.

**Founder of Twilight Tech LLC** — managed IT and cybersecurity for small businesses in Atlanta, GA. My AI runs the business while I build the AI.

---

## What I'm Building

### 🧠 J-Bot — AI OS Layer

An autonomous AI assistant that operates as an **operating-system-level** layer on Windows. Not a chat window. Not a browser extension. A persistent agent that watches the machine, understands context, and acts.

<table>
<tr>
<td width="50%" valign="top">

**What J-Bot Does**
- Sees what's happening on the machine in real time — processes, network, security events, file changes, GPU, display, USB
- Correlates signals across domains (security + system + user activity)
- Self-heals when components crash
- Hunts threats without being asked
- Predicts what's coming (not just what happened)
- Speaks through multi-channel delivery — voice, toast, Telegram, dashboard
- Runs as a Windows service, always on

</td>
<td width="50%" valign="top">

**How It Fits In**
- Two-node distributed system: laptop (Prime) + server (always-on)
- Plugin architecture — new capabilities drop in as domain packs
- Deep integrations with Google Workspace, Telegram, Windows APIs
- FastAPI backend with WebSocket live dashboards
- Zero cloud dependencies, zero vendor lock-in
- Powers my MSP + cybersecurity operations end-to-end

</td>
</tr>
</table>

### 🛡️ HackBot — Deployable Security Sentinel

Purple-team AI agent, forged into a **deployable security product** for MSPs.

<table>
<tr>
<td width="50%" valign="top">

**What HackBot Does**
- Per-client behavioral baselines — time-aware anomaly detection
- Tiered autonomous response (AUTO / CONFIRM / MANUAL) with kill switch
- Attack forecasting — breach risk, CVE exploitation timelines, MITRE kill-chain progression
- Multi-channel alerting — Email, Slack, Telegram, PagerDuty, custom webhooks
- Compliance mapping — NIST 800-53, PCI-DSS, HIPAA, SOC 2
- Self-monitoring — watches its own security services and self-heals

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

Docker-packaged, multi-tenant, one operator monitoring many client networks from a single dashboard.

</td>
</tr>
</table>

<div align="center">

**See it in action: [twilighttech.io/#hackbot](https://twilighttech.io/#hackbot)** — request a pilot or demo

</div>

---

## Tech Stack

**AI & Agents**

![Anthropic](https://img.shields.io/badge/Claude-CC785C?style=flat-square&logo=anthropic&logoColor=white)
![OpenAI](https://img.shields.io/badge/GPT--4o-412991?style=flat-square&logo=openai&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama_Local-000000?style=flat-square&logoColor=white)

Tool-use agents with reflective loops, multi-agent orchestration, semantic routing, adaptive prompting, confidence scoring, and hallucination detection. Provider failover across Anthropic / OpenAI / local Ollama.

**Backend**

![Python](https://img.shields.io/badge/Python_3.11+-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite_WAL-003B57?style=flat-square&logo=sqlite&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

Plugin architecture with entry-point discovery, async pipelines with retry + circuit breakers, SQLite WAL persistence, multi-tenant auth, and containerized deployment.

**Security**

![MITRE](https://img.shields.io/badge/MITRE_ATT%26CK-E31837?style=flat-square&logoColor=white)
![CompTIA](https://img.shields.io/badge/CompTIA_A+-C8202F?style=flat-square&logoColor=white)

Purple-team tooling, compliance frameworks (NIST / PCI-DSS / HIPAA / SOC 2), Windows event log analysis, behavioral threat detection, dark-web monitoring, APT attribution.

**Infrastructure**

![Tailscale](https://img.shields.io/badge/Tailscale-000000?style=flat-square&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)

Tailscale mesh networking, Cloudflare Pages + DNS, Stripe payments for product revenue, Windows service integration with system tray + global hotkeys.

---

## Also Shipping

| Project | Status |
|---|---|
| **[Twilight Tech Website](https://twilighttech.io)** | Live — MSP + cybersecurity services, Cloudflare-hosted |
| **[CompTIA A+ Study Guides](https://twilighttech.io/guides)** | Shipping — Core 1 + Core 2 exam prep via Stripe |
| **J-Bot Origins** | In progress — comic book series documenting the AI's evolution |
| **MSP-Bot / Finance Bot / Project Bot / Camera Bot** | Domain packs running in production |

---

## Current Focus

```python
building    = "J-Bot AI OS Layer — continuous awareness, proactive operations"
shipping    = "HackBot pilots for MSPs + CompTIA A+ Study Guides"
seeking     = "AI Engineer / ML Platform roles (remote)"
available   = "Contract work, consulting, and pilot partners via Twilight Tech LLC"
```

---

## Work With Me

<div align="center">

| | |
|---|---|
| **Hire me full-time** | AI Engineer, ML Platform, or Senior Systems roles — [LinkedIn](https://linkedin.com/in/james-destrades-jr) |
| **Pilot HackBot** | Deploy the security sentinel in your network — [twilighttech.io](https://twilighttech.io/#hackbot) |
| **Contract / Consulting** | AI engineering, MSP services, custom platforms — [james@twilighttech.io](mailto:james@twilighttech.io) |
| **Everything else** | [twilighttech.io](https://twilighttech.io) |

</div>

---

<div align="center">

> *"I build AI that runs as infrastructure — not chatbots, not demos."*

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=TwilightSage94&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true)](https://github.com/TwilightSage94)

<sub>Twilight Tech LLC | Atlanta, GA | Solo Engineer</sub>

</div>
