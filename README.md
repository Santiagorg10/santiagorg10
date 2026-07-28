<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,40:292e42,70:3b4261,100:1a1b27&height=210&section=header&text=Santiago%20Ramirez.&fontSize=68&fontColor=7aa2f7&animation=fadeIn&fontAlignY=38&desc=Systems%20Architect%20%C2%B7%20Full-Stack%20Engineer%20%C2%B7%20Medell%C3%ADn%2C%20Colombia&descSize=15&descAlignY=58&descColor=565f89" width="100%"/>
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

---

## About

I'm the sole engineer at **VIA TERRESTRE S.A.**, a passenger-transport operator in Envigado, Colombia. I design, build and run the systems the company works on day to day — the ERP it operates from, the fleet-telemetry platform, the CI/CD that ships them, and an on-premise AI tier that keeps regulated data inside the building.

Most of this lives under real regulatory constraints — Ministerio de Transporte, DIAN, SG-SST, Ley 1581 — so correctness, auditability and honest documentation matter a lot more than moving fast. I write the decisions down, and I measure a claim before I put a number on it.

I'm still learning most of this as I go, especially the AI side. If you work on something similar, I'd genuinely enjoy comparing notes.

> Most repositories below are private — they hold a client's operational data — so the figures are measured from the repos rather than linked.

---

## Plataforma VIA

A production, domain-driven **ERP** replacing a decade of Excel trackers, paper signatures and scattered shared drives for a Ministerio de Transporte–regulated operator. It's the main system I work on.

*Figures measured from the repository on 2026-07-27, not estimated.*

| | |
|---|---|
| **Backend** | 68 FastAPI routers · 52 SQLAlchemy model modules · **336 PostgreSQL tables** · **1,327 REST endpoints** (count locked by a test) · ~195K lines of Python |
| **Schema** | **Zero Alembic.** 372 idempotent self-heal hooks apply every column, table and index at boot, behind 275 automated verification checks |
| **Access control** | **38 canonical RBAC module keys**, eight of them opt-in only · JTI revocation checked on every authenticated request · a standing census test keeps the un-gated route count at exactly zero |
| **Web & mobile** | React 19 · Vite 7 · strict TypeScript (370 `.tsx` modules) · an Expo / React Native app in Google Play closed testing and TestFlight |
| **Tests** | 2,200+ backend pytest cases against a fresh PostgreSQL · 579 Vitest · 72 Jest · Playwright E2E |
| **Docs** | 518 Markdown files, 378 carrying machine-readable knowledge-graph blocks |
| **History** | 2,681 commits, each with a full conventional-commit body |

**Domains** — Human Capital · Fleet & Maintenance · Operations & Dispatch · SG-SST (Res. 0312) · Environmental / ISO 14001 · Compliance & SAGRILAFT · Documental · Procurement · Finance & Accounting · LMS · CRM · Alerts

**Integrations** — `SIIGO Nube API` · `DIAN e-invoices` · `ONLYOFFICE` · `Grandstream UCM6300A PBX` · `Cloudflare Zero Trust` · GSM OTP

A few pieces I'm happy with:

- **Digital signatures** — 25 signable document types through one dispatch engine, with OTP / PIN / biometric tiers and RFC 3161 timestamping, sized to the proportionality rule in Decreto 2364/2012.
- **FUEC & roadside verification** — trip documents generate a 21-digit consecutivo per the MinTransporte formula, race-safe under advisory locks, and print a QR a police check can validate without platform credentials.
- **Historical integrity** — records Colombian law requires to survive can't be deleted; list endpoints serialize nested snapshots, so archiving a parent never blanks the history that referenced it.
- **Data protection by architecture** — occupational-medical data sits behind an opt-in perimeter with per-access logging, and AI transcripts are encrypted at rest with audited Habeas-Data deletion.

---

## The rest of the ecosystem

| Project | What it is | Where it's at |
|---|---|---|
| **Gps-Via** | The fleet GPS platform — Teltonika FMC125 device edge, a detached Traccar engine, a forked operator console, a passenger PWA with background arrival push, and a thin FastAPI service for toll quoting, route rounds and road-following ETAs. A frozen, versioned telemetry contract is what the ERP consumes. | Hardware bench-validated; the app runs on a synthetic fleet while production ingress clears sign-off · 315 commits |
| **Via-Stack** | The self-hosted CI/CD and operations layer — Woodpecker CI with Docker-in-Docker isolation, Cloudflare Tunnel ingress so nothing needs a public port, Trivy scan-before-push, Syft SBOM and cosign signing. It's the sole publisher of the platform's images. | Operational, four repos onboarded · 193 commits |
| **AI-Stack** | The on-premise AI tier. Local inference and a GraphRAG pipeline over the company's regulated document vault, behind a gateway with scoped keys and a PII quarantine gate on every ingest. This data can't leave the building, so I built the local alternative instead of calling a cloud API. | Inference and retrieval running; wiring it into the platform's copilot · 78 commits |
| **Hermes** | My own developer command center — a React/Vite SPA over a local model fleet, a graph-RAG knowledge base, phase ledgers and usage observability. Mostly where I keep my own tooling honest. | Running daily · 1,031 commits |

**Also** — 🐾 **Lucio & Co**, a small pet-product venture. The first product is a portable telescoping travel bowl: three rigid PP rings on a 3-start self-locking helical cam, a removable 304 stainless insert, two twists between three heights. Fully parametric, verified interference-clean in every position, currently in field-test prep.

---

## Stack

| | |
|---|---|
| **Backend & data** | ![Python](https://img.shields.io/badge/Python-1a1b27?style=flat-square&logo=python&logoColor=7aa2f7) ![FastAPI](https://img.shields.io/badge/FastAPI-1a1b27?style=flat-square&logo=fastapi&logoColor=9ece6a) ![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy%202.0-1a1b27?style=flat-square&logo=sqlalchemy&logoColor=ff9e64) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1a1b27?style=flat-square&logo=postgresql&logoColor=7aa2f7) ![Pydantic](https://img.shields.io/badge/Pydantic-1a1b27?style=flat-square&logo=pydantic&logoColor=e06c75) ![Redis](https://img.shields.io/badge/Redis-1a1b27?style=flat-square&logo=redis&logoColor=f7768e) |
| **Frontend & mobile** | ![React](https://img.shields.io/badge/React%2019-1a1b27?style=flat-square&logo=react&logoColor=7aa2f7) ![TypeScript](https://img.shields.io/badge/TypeScript-1a1b27?style=flat-square&logo=typescript&logoColor=7aa2f7) ![Vite](https://img.shields.io/badge/Vite-1a1b27?style=flat-square&logo=vite&logoColor=bb9af7) ![React Native](https://img.shields.io/badge/React%20Native-1a1b27?style=flat-square&logo=react&logoColor=7dcfff) ![Expo](https://img.shields.io/badge/Expo-1a1b27?style=flat-square&logo=expo&logoColor=ffffff) |
| **Infrastructure & ops** | ![Docker](https://img.shields.io/badge/Docker-1a1b27?style=flat-square&logo=docker&logoColor=7aa2f7) ![Ubuntu](https://img.shields.io/badge/Ubuntu-1a1b27?style=flat-square&logo=ubuntu&logoColor=ff9e64) ![Nginx](https://img.shields.io/badge/Nginx-1a1b27?style=flat-square&logo=nginx&logoColor=9ece6a) ![Cloudflare](https://img.shields.io/badge/Cloudflare-1a1b27?style=flat-square&logo=cloudflare&logoColor=f7768e) ![Woodpecker CI](https://img.shields.io/badge/Woodpecker%20CI-1a1b27?style=flat-square&logo=woodpeckerci&logoColor=9ece6a) ![Prometheus](https://img.shields.io/badge/Prometheus%20%C2%B7%20Grafana-1a1b27?style=flat-square&logo=prometheus&logoColor=ff9e64) ![Tailscale](https://img.shields.io/badge/Tailscale-1a1b27?style=flat-square&logo=tailscale&logoColor=bb9af7) |
| **Local AI** | ![Ollama](https://img.shields.io/badge/Ollama-1a1b27?style=flat-square&logo=ollama&logoColor=ffffff) ![LightRAG](https://img.shields.io/badge/LightRAG-1a1b27?style=flat-square&logoColor=7aa2f7) ![GraphRAG](https://img.shields.io/badge/GraphRAG-1a1b27?style=flat-square&logoColor=bb9af7) ![bge-m3](https://img.shields.io/badge/bge--m3%20embeddings-1a1b27?style=flat-square&logoColor=7dcfff) |
| **CAD & hardware** | ![Fusion 360](https://img.shields.io/badge/Autodesk%20Fusion%20360-1a1b27?style=flat-square&logo=autodesk&logoColor=ff9e64) ![Parametric](https://img.shields.io/badge/Parametric%20Modeling-1a1b27?style=flat-square&logo=autodesk&logoColor=9ece6a) ![3D printing](https://img.shields.io/badge/3D%20Printing-1a1b27?style=flat-square&logoColor=bb9af7) ![Betaflight](https://img.shields.io/badge/Betaflight-1a1b27?style=flat-square&logo=drone&logoColor=f7768e) |

---

## GitHub

<div align="center">
  <img height="180em" src="https://streak-stats.demolab.com?user=santiagorg10&theme=tokyonight&hide_border=true&background=1a1b27&ring=7aa2f7&fire=ff9e64&currStreakLabel=7aa2f7&sideLabels=a9b1d6&currStreakNum=a9b1d6&sideNums=a9b1d6&dates=565f89" />
</div>

<!-- Commit/stars stats card and top-languages card intentionally omitted:
     the self-hosted instance at santiagorg10-readme-stats.vercel.app is gone
     (DEPLOYMENT_NOT_FOUND) and the public one is chronically 503. Both cards also
     need a self-hosted instance + PAT to honour count_private — without it they
     would report almost nothing, since every substantial repo here is private.
     Redeploy the fork, then restore the two <img> tags. -->

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=santiagorg10&theme=tokyo-night&hide_border=true&area=true&area_color=7aa2f7&color=7aa2f7&line=bb9af7&point=ff9e64&bg_color=1a1b27" width="100%" />
</div>

---

## Beyond the code

| 🚁 FPV drones | 🖥️ Self-hosted infra | 🐾 Product design |
|:---|:---|:---|
| Freestyle and long-range builds | OPNsense · Tailscale mesh | Parametric CAD in Fusion 360 |
| Betaflight PID tuning and flashing | Asustor NAS · Grandstream PBX | 3D-printed prototypes, designed for injection molding |
| Stack wiring and soldering | Nightly `pg_dump` · off-site restic | Designs that adapt to each pet |

---

## Contact

<div align="center">

[![Email](https://img.shields.io/badge/santiagorg10%40gmail.com-1a1b27?style=for-the-badge&logo=gmail&logoColor=7aa2f7)](mailto:santiagorg10@gmail.com)

</div>

<div align="center">
  <sub>Built under real regulatory constraints, and documented like it.</sub>
</div>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,40:292e42,70:3b4261,100:1a1b27&height=120&section=footer" width="100%"/>
</div>
