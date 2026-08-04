<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,40:292e42,70:3b4261,100:1a1b27&height=230&section=header&text=Santiago%20Ramirez.&fontSize=72&fontColor=7aa2f7&animation=fadeIn&fontAlignY=36&desc=Systems%20Architect%20%E2%80%A2%20Full-Stack%20Platform%20%E2%80%A2%20FPV%20Pilot&descSize=16&descAlignY=56&descColor=565f89" width="100%"/>
</div>

<div align="center">

  <a href="README.md">
    <img src="https://img.shields.io/badge/🇺🇸 English-7aa2f7?style=for-the-badge&labelColor=1a1b27" />
  </a>
  &nbsp;
  <a href="README.es.md">
    <img src="https://img.shields.io/badge/🇨🇴 Español-9ece6a?style=for-the-badge&labelColor=1a1b27" />
  </a>
  &nbsp;&nbsp;
  <img src="https://komarev.com/ghpvc/?username=santiagorg10&label=Profile+Views&color=7aa2f7&style=for-the-badge&labelColor=1a1b27" />

</div>

<br/>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=19&duration=2800&pause=1000&color=7aa2f7&center=true&vCenter=true&width=680&lines=Building+a+full+ERP+from+scratch+%F0%9F%8F%97%EF%B8%8F;336+tables+%C2%B7+1%2C327+endpoints+%C2%B7+zero+Alembic+migrations;Python+%7C+FastAPI+%7C+React+%7C+React+Native+%7C+Docker;Fleet+telemetry+%C2%B7+self-hosted+CI%2FCD+%C2%B7+on-prem+AI;Parametric+CAD+in+Fusion+360+%F0%9F%90%BE;FPV+freestyle+pilot+%F0%9F%9A%81+%C2%B7+Betaflight+%C2%B7+PID+tuning;Medell%C3%ADn%2C+Colombia+%F0%9F%87%A8%F0%9F%87%B4" />
</div>

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🧑‍💻 &nbsp;About Me

```python
class SantiagoR:
    location    = "Medellín, Colombia 🇨🇴"
    company     = "VIA TERRESTRE S.A. — Envigado, Antioquia"
    role        = "Sole Engineer · Systems Architect"
    current     = "Plataforma VIA — production ERP, built solo from scratch"
    ecosystem   = ["Plataforma VIA", "Gps-Via", "Via-Stack", "AI-Stack", "Hermes"]
    infra       = ["Ubuntu 24.04", "OPNsense", "Docker", "Tailscale", "Cloudflare"]
    side_quest  = "Lucio & Co — pet products in Fusion 360 🐾"
    hobbies     = ["FPV Drones 🚁", "Betaflight PID tuning", "Self-hosted everything"]

    def say_hi(self):
        print("I build real systems under real regulatory constraints.")
        print("No managed databases. No Alembic. No shortcuts.")
```

I design, build and run the systems a passenger-transport operator works on every day — the ERP it
operates from, the fleet-telemetry platform, the CI/CD that ships them, and an on-premise AI tier that
keeps regulated data inside the building. Ministerio de Transporte, DIAN, SG-SST and Ley 1581 are design
inputs, not afterthoughts, so correctness and auditability matter more than moving fast.

> Most repositories below are private — they hold a client's operational data — so the figures are
> measured from the repos rather than linked. I'm still learning a lot of this as I go, especially the
> AI side. If you work on something similar, I'd genuinely enjoy comparing notes.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🚀 &nbsp;Flagship — Plataforma VIA

> A production, **domain-driven ERP** replacing a decade of Excel, paper signatures, and fragmented Google Drive for a *Ministerio de Transporte*-regulated passenger-transport operator.

<div align="center">

<table>
  <tr>
    <td align="center"><img src="https://img.shields.io/badge/336-PostgreSQL%20Tables-7aa2f7?style=for-the-badge&labelColor=1a1b27" /></td>
    <td align="center"><img src="https://img.shields.io/badge/1%2C327-REST%20Endpoints-bb9af7?style=for-the-badge&labelColor=1a1b27" /></td>
    <td align="center"><img src="https://img.shields.io/badge/68-FastAPI%20Routers-9ece6a?style=for-the-badge&labelColor=1a1b27" /></td>
  </tr>
  <tr>
    <td align="center"><img src="https://img.shields.io/badge/370-React%20%2B%20TS%20Modules-ff9e64?style=for-the-badge&labelColor=1a1b27" /></td>
    <td align="center"><img src="https://img.shields.io/badge/195K-LOC%20Python-7dcfff?style=for-the-badge&labelColor=1a1b27" /></td>
    <td align="center"><img src="https://img.shields.io/badge/372-Self--Heal%20Hooks-f7768e?style=for-the-badge&labelColor=1a1b27" /></td>
  </tr>
  <tr>
    <td align="center"><img src="https://img.shields.io/badge/38-RBAC%20Scopes-e0af68?style=for-the-badge&labelColor=1a1b27" /></td>
    <td align="center"><img src="https://img.shields.io/badge/2%2C200%2B-Backend%20Tests-7aa2f7?style=for-the-badge&labelColor=1a1b27" /></td>
    <td align="center"><img src="https://img.shields.io/badge/Zero-Alembic%20Migrations-9ece6a?style=for-the-badge&labelColor=1a1b27" /></td>
  </tr>
</table>

<sub>Measured from the repository on 2026-07-27 — not estimated.</sub>

</div>

**Domains:** Human Capital · Fleet & Maintenance · Operations & Dispatch · SG-SST (Res. 0312) · Environmental / ISO 14001 · Compliance & SAGRILAFT · Documental · Procurement · Finance & Accounting · LMS · CRM · Alerts

**Integrations:** `SIIGO Nube API` · `DIAN e-invoices` · `ONLYOFFICE` · `Grandstream UCM6300A PBX` · `Cloudflare Zero Trust` · `GSM OTP`

A few pieces I'm happy with:

- **Digital signatures** — 25 signable document types through one dispatch engine, with OTP / PIN / biometric tiers and RFC 3161 timestamping, sized to the proportionality rule in Decreto 2364/2012.
- **FUEC & roadside verification** — trip documents generate a 21-digit consecutivo per the MinTransporte formula, race-safe under advisory locks, and print a QR a police check can validate without platform credentials.
- **Historical integrity** — records Colombian law requires to survive can't be deleted; list endpoints serialize nested snapshots, so archiving a parent never blanks the history that referenced it.
- **Zero-trust RBAC** — a standing census test classifies every one of the 1,327 endpoints and keeps the un-gated count at exactly zero.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🛰️ &nbsp;The Vía Ecosystem

<div align="center">

### 📍 Gps-Via — Fleet Telemetry

</div>

> Teltonika FMC125 device edge, a detached Traccar engine, a forked operator console, a passenger PWA with background arrival push, and a thin FastAPI service for toll quoting, route rounds and road-following ETAs. A frozen, versioned telemetry contract is what the ERP consumes.

<div align="center">

![Teltonika](https://img.shields.io/badge/Teltonika%20FMC125-1a1b27?style=flat-square&logoColor=7aa2f7)
![Traccar](https://img.shields.io/badge/Traccar-1a1b27?style=flat-square&logoColor=9ece6a)
![FastAPI](https://img.shields.io/badge/FastAPI-1a1b27?style=flat-square&logo=fastapi&logoColor=9ece6a)
![React](https://img.shields.io/badge/React-1a1b27?style=flat-square&logo=react&logoColor=7aa2f7)
![PWA](https://img.shields.io/badge/PWA%20%C2%B7%20Push-1a1b27?style=flat-square&logo=pwa&logoColor=bb9af7)
![Valhalla](https://img.shields.io/badge/Valhalla%20Routing-1a1b27?style=flat-square&logoColor=ff9e64)

<sub>Hardware bench-validated · the app runs on a synthetic fleet while production ingress clears sign-off · 315 commits</sub>

</div>

<div align="center">

### ⚙️ Via-Stack — Self-Hosted CI/CD

</div>

> The operational layer that ships every other project. Woodpecker CI with Docker-in-Docker isolation, Cloudflare Tunnel ingress so nothing needs a public port, Trivy scan-before-push, Syft SBOM and cosign signing. It's the sole publisher of the platform's images.

<div align="center">

![Woodpecker CI](https://img.shields.io/badge/Woodpecker%20CI-1a1b27?style=flat-square&logo=woodpeckerci&logoColor=9ece6a)
![Docker](https://img.shields.io/badge/Docker--in--Docker-1a1b27?style=flat-square&logo=docker&logoColor=7aa2f7)
![Cloudflare](https://img.shields.io/badge/Cloudflare%20Tunnel-1a1b27?style=flat-square&logo=cloudflare&logoColor=f7768e)
![Trivy](https://img.shields.io/badge/Trivy-1a1b27?style=flat-square&logoColor=bb9af7)
![cosign](https://img.shields.io/badge/Syft%20SBOM%20%C2%B7%20cosign-1a1b27?style=flat-square&logoColor=7dcfff)
![Grafana](https://img.shields.io/badge/Prometheus%20%C2%B7%20Grafana-1a1b27?style=flat-square&logo=grafana&logoColor=ff9e64)

<sub>Operational · four repos onboarded · 193 commits</sub>

</div>

<div align="center">

### 🧠 AI-Stack — On-Premise AI

</div>

> The AI tier of Plataforma VIA, and the project I'm learning the most from right now. Local inference and a Graph-RAG pipeline over the company's regulated document vault, behind a gateway with scoped keys and a PII quarantine gate on every ingest. This data can't leave the building, so I built the local alternative instead of calling a cloud API — and documented every step like infrastructure, not experiments.

<div align="center">

<img src="https://raw.githubusercontent.com/Santiagorg10/santiagorg10/main/assets/ollama.svg" height="42" alt="Ollama" />

![Ollama](https://img.shields.io/badge/Ollama-1a1b27?style=flat-square&logo=ollama&logoColor=ffffff)
![qwen3](https://img.shields.io/badge/qwen3%3A32b%20%C2%B7%2070%20tok%2Fs-1a1b27?style=flat-square&logoColor=9ece6a)
![LightRAG](https://img.shields.io/badge/LightRAG-1a1b27?style=flat-square&logoColor=7aa2f7)
![GraphRAG](https://img.shields.io/badge/GraphRAG-1a1b27?style=flat-square&logoColor=bb9af7)
![bge-m3](https://img.shields.io/badge/bge--m3%20embeddings-1a1b27?style=flat-square&logoColor=7dcfff)
![LiteLLM](https://img.shields.io/badge/LiteLLM%20Gateway-1a1b27?style=flat-square&logoColor=ff9e64)

<sub>Inference and retrieval running · wiring it into the platform's copilot · 78 commits</sub>

</div>

<div align="center">

### 🪐 Hermes — Developer Command Center

</div>

> My own tooling hub: a React/Vite SPA over a local model fleet, a graph-RAG knowledge base, phase ledgers and usage observability. Mostly where I keep my own workflow honest.

<div align="center">

![React](https://img.shields.io/badge/React%20%C2%B7%20Vite-1a1b27?style=flat-square&logo=react&logoColor=7aa2f7)
![FastAPI](https://img.shields.io/badge/FastAPI-1a1b27?style=flat-square&logo=fastapi&logoColor=9ece6a)
![LightRAG](https://img.shields.io/badge/Graph--RAG%20%2B%20BM25-1a1b27?style=flat-square&logoColor=bb9af7)
![Ollama](https://img.shields.io/badge/Local%20Model%20Fleet-1a1b27?style=flat-square&logo=ollama&logoColor=ffffff)

<sub>Running daily · 1,031 commits</sub>

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🖧 &nbsp;Infrastructure & Operations

> **Two tiers, on purpose.** An on-prem server does the compute — ERP, CI and the AI stack — behind a Cloudflare Tunnel with **no public ports at all**. A small edge VPS abroad does the things a tunneled box fundamentally can't: hold a real public IP, *not* share fate with the office's power and fiber, and host the estate's single sanctioned public listener — the fleet's raw-TCP GPS ingress, rate-limited and connection-capped.

| | |
|---|---|
| **On-prem** | Ubuntu 24.04 · OPNsense micro-segmentation · Docker Compose · Tailscale mesh · Cloudflare Tunnel + Access, GitHub SSO, webhook HMAC verification |
| **Edge VPS** | Public-edge + off-site tier · key-only SSH · UFW · ops reachable only over the tailnet · **off-box uptime monitoring**, so the monitor doesn't die in the outage it's supposed to report |
| **Disaster recovery** | Nightly **client-encrypted restic** to the off-site box over Tailscale · **RPO ≤ 24 h · RTO ~1–2 min** — measured in a real restore drill, not assumed. A backup you've never restored isn't a backup |
| **Observability** | Prometheus · Grafana · Alertmanager · node-exporter · cAdvisor · Uptime-Kuma · push alerting · a fate-independent dead-man's heartbeat |
| **Capacity** | A k6 harness that *measures* the real concurrent-user ceiling — connection-pool saturation, p95 latency, the point where 5xx starts |
| **Telephony** | Self-hosted **Asterisk 20 LTS** with `chan_dongle` over Huawei USB GSM modems — AGI scripts report DTMF and inbound events back to FastAPI; Spanish prompts are synthesized at image build, so nothing calls a TTS API at runtime |

<div align="center">

![Linux](https://img.shields.io/badge/Linux%20VPS-1a1b27?style=flat-square&logo=linux&logoColor=e0af68)
![OPNsense](https://img.shields.io/badge/OPNsense-1a1b27?style=flat-square&logo=opnsense&logoColor=ff9e64)
![Tailscale](https://img.shields.io/badge/Tailscale-1a1b27?style=flat-square&logo=tailscale&logoColor=bb9af7)
![restic](https://img.shields.io/badge/restic%20%C2%B7%20off--site%20DR-1a1b27?style=flat-square&logoColor=9ece6a)
![Prometheus](https://img.shields.io/badge/Prometheus%20%C2%B7%20Grafana-1a1b27?style=flat-square&logo=prometheus&logoColor=ff9e64)
![k6](https://img.shields.io/badge/k6%20Load%20Testing-1a1b27?style=flat-square&logo=k6&logoColor=f7768e)
![Asterisk](https://img.shields.io/badge/Asterisk%20%C2%B7%20GSM-1a1b27?style=flat-square&logo=asterisk&logoColor=7aa2f7)

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

<div align="center">

**🐾 Side quest — Lucio & Co** · customizable pet products, designed around each pet.
The first one is a portable telescoping travel bowl — three rigid PP rings on a 3-start self-locking
helical cam, a removable 304 stainless insert, two twists between three heights. Fully parametric,
verified interference-clean in every position, now in field-test prep.

<img src="https://raw.githubusercontent.com/Santiagorg10/santiagorg10/main/assets/fusion360.svg" height="42" alt="Autodesk Fusion 360" />

![Fusion 360](https://img.shields.io/badge/Autodesk%20Fusion%20360-1a1b27?style=flat-square&logo=autodesk&logoColor=ff9e64)
![Parametric](https://img.shields.io/badge/100%25%20Parametric-1a1b27?style=flat-square&logo=autodesk&logoColor=9ece6a)
![Injection Molding](https://img.shields.io/badge/Design%20for%20Injection%20Molding-1a1b27?style=flat-square&logoColor=bb9af7)

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🛠️ &nbsp;Tech Stack

<div align="center">

**⚙️ Backend**

<img src="https://skillicons.dev/icons?i=py,fastapi,postgres,redis&theme=dark" height="48" />

![Python](https://img.shields.io/badge/Python-1a1b27?style=flat-square&logo=python&logoColor=7aa2f7)
![FastAPI](https://img.shields.io/badge/FastAPI-1a1b27?style=flat-square&logo=fastapi&logoColor=9ece6a)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy%202.0-1a1b27?style=flat-square&logo=sqlalchemy&logoColor=ff9e64)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1a1b27?style=flat-square&logo=postgresql&logoColor=7aa2f7)
![Pydantic](https://img.shields.io/badge/Pydantic-1a1b27?style=flat-square&logo=pydantic&logoColor=e06c75)
![Redis](https://img.shields.io/badge/Redis-1a1b27?style=flat-square&logo=redis&logoColor=f7768e)
![pandas](https://img.shields.io/badge/pandas-1a1b27?style=flat-square&logo=pandas&logoColor=bb9af7)

<br/>

**🖥️ Frontend**

<img src="https://skillicons.dev/icons?i=react,ts,vite&theme=dark" height="48" />

![React](https://img.shields.io/badge/React%2019-1a1b27?style=flat-square&logo=react&logoColor=7aa2f7)
![Vite](https://img.shields.io/badge/Vite%207-1a1b27?style=flat-square&logo=vite&logoColor=bb9af7)
![TypeScript](https://img.shields.io/badge/TypeScript%20Strict-1a1b27?style=flat-square&logo=typescript&logoColor=7aa2f7)
![Recharts](https://img.shields.io/badge/Recharts-1a1b27?style=flat-square&logo=react&logoColor=9ece6a)

<br/>

**📱 Mobile**

<img src="https://skillicons.dev/icons?i=react,ts&theme=dark" height="48" />

![React Native](https://img.shields.io/badge/React%20Native%200.85-1a1b27?style=flat-square&logo=react&logoColor=7dcfff)
![Expo](https://img.shields.io/badge/Expo%20SDK%2056-1a1b27?style=flat-square&logo=expo&logoColor=ffffff)
![EAS](https://img.shields.io/badge/EAS%20Build-1a1b27?style=flat-square&logo=expo&logoColor=bb9af7)
![Play Store](https://img.shields.io/badge/Play%20Console%20%C2%B7%20TestFlight-1a1b27?style=flat-square&logo=googleplay&logoColor=9ece6a)

<br/>

**🚢 DevOps & Infrastructure**

<img src="https://skillicons.dev/icons?i=docker,linux,nginx,git,github,cloudflare&theme=dark" height="48" />

![Docker](https://img.shields.io/badge/Docker%20Compose-1a1b27?style=flat-square&logo=docker&logoColor=7aa2f7)
![Ubuntu](https://img.shields.io/badge/Ubuntu%2024.04-1a1b27?style=flat-square&logo=ubuntu&logoColor=ff9e64)
![Nginx](https://img.shields.io/badge/Nginx-1a1b27?style=flat-square&logo=nginx&logoColor=9ece6a)
![Cloudflare](https://img.shields.io/badge/Cloudflare%20ZT-1a1b27?style=flat-square&logo=cloudflare&logoColor=f7768e)
![Woodpecker](https://img.shields.io/badge/Woodpecker%20CI-1a1b27?style=flat-square&logo=woodpeckerci&logoColor=9ece6a)
![OPNsense](https://img.shields.io/badge/OPNsense-1a1b27?style=flat-square&logo=opnsense&logoColor=ff9e64)
![Tailscale](https://img.shields.io/badge/Tailscale-1a1b27?style=flat-square&logo=tailscale&logoColor=bb9af7)
![Linux VPS](https://img.shields.io/badge/Linux%20VPS%20%C2%B7%20UFW-1a1b27?style=flat-square&logo=linux&logoColor=e0af68)

<br/>

**📡 Observability, Reliability & Telephony**

<img src="https://skillicons.dev/icons?i=prometheus,grafana&theme=dark" height="48" />

![Prometheus](https://img.shields.io/badge/Prometheus-1a1b27?style=flat-square&logo=prometheus&logoColor=ff9e64)
![Grafana](https://img.shields.io/badge/Grafana-1a1b27?style=flat-square&logo=grafana&logoColor=e0af68)
![Alertmanager](https://img.shields.io/badge/Alertmanager%20%C2%B7%20Uptime--Kuma-1a1b27?style=flat-square&logoColor=9ece6a)
![restic](https://img.shields.io/badge/restic%20%C2%B7%20Off--site%20DR-1a1b27?style=flat-square&logoColor=7dcfff)
![k6](https://img.shields.io/badge/k6-1a1b27?style=flat-square&logo=k6&logoColor=f7768e)
![Asterisk](https://img.shields.io/badge/Asterisk%2020%20%C2%B7%20AMI%2FARI%2FAGI-1a1b27?style=flat-square&logo=asterisk&logoColor=7aa2f7)

<br/>

**🧠 AI & LLM Ops**

<img src="https://raw.githubusercontent.com/Santiagorg10/santiagorg10/main/assets/ollama.svg" height="48" alt="Ollama" />

![Ollama](https://img.shields.io/badge/Ollama-1a1b27?style=flat-square&logo=ollama&logoColor=ffffff)
![LightRAG](https://img.shields.io/badge/LightRAG-1a1b27?style=flat-square&logoColor=7aa2f7)
![GraphRAG](https://img.shields.io/badge/GraphRAG-1a1b27?style=flat-square&logoColor=bb9af7)
![bge-m3](https://img.shields.io/badge/bge--m3%20embeddings-1a1b27?style=flat-square&logoColor=7dcfff)
![LiteLLM](https://img.shields.io/badge/LiteLLM-1a1b27?style=flat-square&logoColor=ff9e64)

<br/>

**📐 CAD & Product Design**

<img src="https://raw.githubusercontent.com/Santiagorg10/santiagorg10/main/assets/fusion360.svg" height="48" alt="Autodesk Fusion 360" />

![Fusion 360](https://img.shields.io/badge/Autodesk%20Fusion%20360-1a1b27?style=flat-square&logo=autodesk&logoColor=ff9e64)
![Parametric Modeling](https://img.shields.io/badge/Parametric%20Modeling-1a1b27?style=flat-square&logo=autodesk&logoColor=9ece6a)
![3D Printing](https://img.shields.io/badge/3D%20Print%20Prototyping-1a1b27?style=flat-square&logoColor=bb9af7)

<br/>

**🔧 Tools & Environment**

<img src="https://skillicons.dev/icons?i=vscode,bash&theme=dark" height="48" />&nbsp;<img src="https://raw.githubusercontent.com/Santiagorg10/santiagorg10/main/assets/betaflight.png" height="44" alt="Betaflight" />

![VS Code](https://img.shields.io/badge/VS%20Code-1a1b27?style=flat-square&logo=visualstudiocode&logoColor=7aa2f7)
![Betaflight](https://img.shields.io/badge/Betaflight-1a1b27?style=flat-square&logo=drone&logoColor=f7768e)

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

<!-- All three third-party stat cards (commits/stars, top languages, streak) are
     intentionally omitted — they do not survive GitHub's image proxy:
       · santiagorg10-readme-stats.vercel.app → DEPLOYMENT_NOT_FOUND (instance deleted)
       · github-readme-stats.vercel.app       → chronically 503
       · streak-stats.demolab.com             → 6-7s warm, 16s+ cold, frequent 503;
                                                camo times out, so it renders broken
     Fix: self-host both projects on Vercel with a read-only PAT. That also enables
     count_private, which matters here because every substantial repo is private —
     without it the cards would report almost nothing. Then restore the <img> tags. -->

## 📈 &nbsp;Contribution Activity

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=santiagorg10&theme=tokyo-night&hide_border=true&area=true&area_color=7aa2f7&color=7aa2f7&line=bb9af7&point=ff9e64&bg_color=1a1b27" width="100%" />
</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 👾 &nbsp;Pac-Man Contribution Graph

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/santiagorg10/santiagorg10/output/pacman-contribution-graph-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/santiagorg10/santiagorg10/output/pacman-contribution-graph.svg" />
    <img alt="pacman contribution graph" src="https://raw.githubusercontent.com/santiagorg10/santiagorg10/output/pacman-contribution-graph-dark.svg" width="100%" />
  </picture>
</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🚁 &nbsp;Beyond the Code

<div align="center">

| 🚁 FPV Drones | 🖥️ Self-Hosted Infra | 🧠 Local AI | 🐾 Product Design |
|:---:|:---:|:---:|:---:|
| Freestyle & long-range builds | OPNsense · Tailscale mesh | On-prem Ollama · LightRAG | Lucio & Co — pet products |
| Betaflight PID tuning & flash | Asustor NAS · Grandstream PBX | Graph-RAG over messy real docs | Fusion 360 parametric CAD |
| FPV stack wiring & soldering | Nightly `pg_dump` · off-site restic | Always re-learning this one | Designs that fit each pet |

</div>

## 📫 &nbsp;Connect

<div align="center">

[![Email](https://img.shields.io/badge/santiagorg10%40gmail.com-1a1b27?style=for-the-badge&logo=gmail&logoColor=7aa2f7)](mailto:santiagorg10@gmail.com)

</div>

---

<div align="center">
  <sub>Built with discipline, domain boundaries, and the Colombian transport sector's appetite for compliance.</sub>
</div>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,40:292e42,70:3b4261,100:1a1b27&height=130&section=footer" width="100%"/>
</div>
