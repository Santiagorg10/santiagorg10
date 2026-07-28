<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,40:292e42,70:3b4261,100:1a1b27&height=210&section=header&text=Santiago%20Ramirez.&fontSize=68&fontColor=7aa2f7&animation=fadeIn&fontAlignY=38&desc=Arquitecto%20de%20Sistemas%20%C2%B7%20Desarrollador%20Full-Stack%20%C2%B7%20Medell%C3%ADn%2C%20Colombia&descSize=15&descAlignY=58&descColor=565f89" width="100%"/>
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
  <img src="https://komarev.com/ghpvc/?username=santiagorg10&label=Visitas+al+Perfil&color=7aa2f7&style=for-the-badge&labelColor=1a1b27" />

</div>

---

## Sobre mí

Soy el único ingeniero de **VIA TERRESTRE S.A.**, una empresa de transporte de pasajeros en Envigado, Colombia. Diseño, construyo y opero los sistemas con los que la empresa trabaja todos los días: el ERP desde el que opera, la plataforma de telemetría de flota, el CI/CD que los despliega, y una capa de IA on-premise que mantiene los datos regulados dentro del edificio.

Casi todo esto vive bajo restricciones regulatorias reales — Ministerio de Transporte, DIAN, SG-SST, Ley 1581 — así que la corrección, la auditabilidad y una documentación honesta importan mucho más que ir rápido. Dejo las decisiones por escrito, y mido un dato antes de ponerle un número.

Sigo aprendiendo casi todo sobre la marcha, en especial la parte de IA. Si trabajas en algo parecido, me encantaría comparar notas.

> La mayoría de los repositorios de abajo son privados — contienen datos operativos de un cliente — así que las cifras están medidas sobre los repos, no enlazadas.

---

## Plataforma VIA

Un **ERP** en producción, orientado a dominios, que reemplaza una década de archivos de Excel, firmas en papel y carpetas dispersas en la nube para un operador regulado por el Ministerio de Transporte. Es el sistema principal en el que trabajo.

*Cifras medidas sobre el repositorio el 2026-07-27, no estimadas.*

| | |
|---|---|
| **Backend** | 68 routers FastAPI · 52 módulos de modelos SQLAlchemy · **336 tablas PostgreSQL** · **1.327 endpoints REST** (conteo fijado por un test) · ~195K líneas de Python |
| **Esquema** | **Cero Alembic.** 372 hooks idempotentes de auto-reparación aplican cada columna, tabla e índice al arranque, respaldados por 275 verificaciones automáticas |
| **Control de acceso** | **38 claves canónicas de módulo RBAC**, ocho de ellas solo por concesión explícita · revocación por JTI verificada en cada request autenticado · un test censo permanente mantiene en exactamente cero las rutas sin protección |
| **Web y móvil** | React 19 · Vite 7 · TypeScript estricto (370 módulos `.tsx`) · una app Expo / React Native en pruebas cerradas de Google Play y en TestFlight |
| **Pruebas** | 2.200+ casos pytest de backend contra una PostgreSQL limpia · 579 Vitest · 72 Jest · Playwright E2E |
| **Documentación** | 518 archivos Markdown, 378 con bloques de grafo de conocimiento legibles por máquina |
| **Historia** | 2.681 commits, cada uno con su cuerpo de conventional commit completo |

**Dominios** — Talento Humano · Flotas y Mantenimiento · Operaciones y Despacho · SG-SST (Res. 0312) · Gestión Ambiental / ISO 14001 · Cumplimiento y SAGRILAFT · Documental · Compras · Finanzas y Contabilidad · Capacitaciones · CRM · Alertas

**Integraciones** — `SIIGO Nube API` · `facturación electrónica DIAN` · `ONLYOFFICE` · `PBX Grandstream UCM6300A` · `Cloudflare Zero Trust` · OTP por GSM

Algunas piezas con las que quedé contento:

- **Firma electrónica** — 25 tipos de documento firmables a través de un solo motor de despacho, con niveles OTP / PIN / biométrico y sellado de tiempo RFC 3161, dimensionados según el criterio de proporcionalidad del Decreto 2364/2012.
- **FUEC y verificación en vía** — los documentos de viaje generan un consecutivo de 21 dígitos según la fórmula del MinTransporte, a prueba de carreras mediante advisory locks, e imprimen un QR que un control policial puede validar sin credenciales de la plataforma.
- **Integridad histórica** — los registros que la ley colombiana exige conservar no se pueden borrar; los endpoints de listado serializan snapshots anidados, así que archivar un padre nunca vacía el historial que lo referenciaba.
- **Protección de datos por arquitectura** — los datos médicos ocupacionales viven tras un perímetro de concesión explícita con registro por acceso, y las transcripciones de IA se cifran en reposo con borrado auditado por Habeas Data.

---

## El resto del ecosistema

| Proyecto | Qué es | En qué va |
|---|---|---|
| **Gps-Via** | La plataforma GPS de la flota — el borde de dispositivo Teltonika FMC125, un motor Traccar desacoplado, una consola de operador bifurcada, una PWA para pasajeros con push de llegada en segundo plano, y un servicio FastAPI delgado para cotización de peajes, rondas de ruta y ETAs que siguen la vía. Un contrato de telemetría congelado y versionado es lo que consume el ERP. | Hardware validado en banco; la app corre sobre una flota sintética mientras el ingreso a producción pasa su aprobación · 315 commits |
| **Via-Stack** | La capa de CI/CD y operación autoalojada — Woodpecker CI con aislamiento Docker-in-Docker, ingreso por Cloudflare Tunnel para que nada necesite un puerto público, escaneo Trivy antes de publicar, SBOM con Syft y firma con cosign. Es el único publicador de las imágenes de la plataforma. | Operativa, cuatro repos integrados · 193 commits |
| **AI-Stack** | La capa de IA on-premise. Inferencia local y un pipeline GraphRAG sobre la bóveda documental regulada de la empresa, detrás de un gateway con llaves acotadas y una compuerta de cuarentena de PII en cada ingesta. Estos datos no pueden salir del edificio, así que construí la alternativa local en vez de llamar a una API en la nube. | Inferencia y recuperación funcionando; conectándola al copiloto de la plataforma · 78 commits |
| **Hermes** | Mi propio centro de mando de desarrollo — una SPA React/Vite sobre una flota de modelos locales, una base de conocimiento graph-RAG, registros de fases y observabilidad de uso. Sobre todo, donde mantengo honesto mi propio herramental. | En uso diario · 1.031 commits |

**Además** — 🐾 **Lucio & Co**, un pequeño emprendimiento de productos para mascotas. El primer producto es un bebedero de viaje telescópico portátil: tres anillos rígidos de PP sobre una leva helicoidal autoblocante de 3 entradas, un inserto removible de acero 304, dos giros entre tres alturas. Totalmente paramétrico, verificado libre de interferencias en cada posición, actualmente en preparación de pruebas de campo.

---

## Stack

| | |
|---|---|
| **Backend y datos** | ![Python](https://img.shields.io/badge/Python-1a1b27?style=flat-square&logo=python&logoColor=7aa2f7) ![FastAPI](https://img.shields.io/badge/FastAPI-1a1b27?style=flat-square&logo=fastapi&logoColor=9ece6a) ![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy%202.0-1a1b27?style=flat-square&logo=sqlalchemy&logoColor=ff9e64) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1a1b27?style=flat-square&logo=postgresql&logoColor=7aa2f7) ![Pydantic](https://img.shields.io/badge/Pydantic-1a1b27?style=flat-square&logo=pydantic&logoColor=e06c75) ![Redis](https://img.shields.io/badge/Redis-1a1b27?style=flat-square&logo=redis&logoColor=f7768e) |
| **Frontend y móvil** | ![React](https://img.shields.io/badge/React%2019-1a1b27?style=flat-square&logo=react&logoColor=7aa2f7) ![TypeScript](https://img.shields.io/badge/TypeScript-1a1b27?style=flat-square&logo=typescript&logoColor=7aa2f7) ![Vite](https://img.shields.io/badge/Vite-1a1b27?style=flat-square&logo=vite&logoColor=bb9af7) ![React Native](https://img.shields.io/badge/React%20Native-1a1b27?style=flat-square&logo=react&logoColor=7dcfff) ![Expo](https://img.shields.io/badge/Expo-1a1b27?style=flat-square&logo=expo&logoColor=ffffff) |
| **Infraestructura y operación** | ![Docker](https://img.shields.io/badge/Docker-1a1b27?style=flat-square&logo=docker&logoColor=7aa2f7) ![Ubuntu](https://img.shields.io/badge/Ubuntu-1a1b27?style=flat-square&logo=ubuntu&logoColor=ff9e64) ![Nginx](https://img.shields.io/badge/Nginx-1a1b27?style=flat-square&logo=nginx&logoColor=9ece6a) ![Cloudflare](https://img.shields.io/badge/Cloudflare-1a1b27?style=flat-square&logo=cloudflare&logoColor=f7768e) ![Woodpecker CI](https://img.shields.io/badge/Woodpecker%20CI-1a1b27?style=flat-square&logo=woodpeckerci&logoColor=9ece6a) ![Prometheus](https://img.shields.io/badge/Prometheus%20%C2%B7%20Grafana-1a1b27?style=flat-square&logo=prometheus&logoColor=ff9e64) ![Tailscale](https://img.shields.io/badge/Tailscale-1a1b27?style=flat-square&logo=tailscale&logoColor=bb9af7) |
| **IA local** | ![Ollama](https://img.shields.io/badge/Ollama-1a1b27?style=flat-square&logo=ollama&logoColor=ffffff) ![LightRAG](https://img.shields.io/badge/LightRAG-1a1b27?style=flat-square&logoColor=7aa2f7) ![GraphRAG](https://img.shields.io/badge/GraphRAG-1a1b27?style=flat-square&logoColor=bb9af7) ![bge-m3](https://img.shields.io/badge/bge--m3%20embeddings-1a1b27?style=flat-square&logoColor=7dcfff) |
| **CAD y hardware** | ![Fusion 360](https://img.shields.io/badge/Autodesk%20Fusion%20360-1a1b27?style=flat-square&logo=autodesk&logoColor=ff9e64) ![Paramétrico](https://img.shields.io/badge/Modelado%20Param%C3%A9trico-1a1b27?style=flat-square&logo=autodesk&logoColor=9ece6a) ![Impresión 3D](https://img.shields.io/badge/Impresi%C3%B3n%203D-1a1b27?style=flat-square&logoColor=bb9af7) ![Betaflight](https://img.shields.io/badge/Betaflight-1a1b27?style=flat-square&logo=drone&logoColor=f7768e) |

---

## GitHub

<div align="center">
  <img height="180em" src="https://streak-stats.demolab.com?user=santiagorg10&locale=es&theme=tokyonight&hide_border=true&background=1a1b27&ring=7aa2f7&fire=ff9e64&currStreakLabel=7aa2f7&sideLabels=a9b1d6&currStreakNum=a9b1d6&sideNums=a9b1d6&dates=565f89" />
</div>

<!-- Tarjetas de estadísticas y de lenguajes omitidas a propósito:
     la instancia autoalojada en santiagorg10-readme-stats.vercel.app ya no existe
     (DEPLOYMENT_NOT_FOUND) y la pública responde 503 de forma crónica. Además ambas
     necesitan instancia propia + PAT para respetar count_private — sin eso reportarían
     casi nada, porque todos los repos importantes aquí son privados.
     Redesplegar el fork y restaurar las dos etiquetas <img>. -->

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=santiagorg10&theme=tokyo-night&hide_border=true&area=true&area_color=7aa2f7&color=7aa2f7&line=bb9af7&point=ff9e64&bg_color=1a1b27" width="100%" />
</div>

---

## Más allá del código

| 🚁 Drones FPV | 🖥️ Infraestructura propia | 🐾 Diseño de producto |
|:---|:---|:---|
| Builds de freestyle y largo alcance | OPNsense · malla Tailscale | CAD paramétrico en Fusion 360 |
| Ajuste de PID y flasheo en Betaflight | NAS Asustor · PBX Grandstream | Prototipos impresos en 3D, diseñados para inyección |
| Cableado y soldadura del stack | `pg_dump` nocturno · restic fuera de sitio | Diseños que se adaptan a cada mascota |

---

## Contacto

<div align="center">

[![Email](https://img.shields.io/badge/santiagorg10%40gmail.com-1a1b27?style=for-the-badge&logo=gmail&logoColor=7aa2f7)](mailto:santiagorg10@gmail.com)

</div>

<div align="center">
  <sub>Construido bajo restricciones regulatorias reales, y documentado como tal.</sub>
</div>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,40:292e42,70:3b4261,100:1a1b27&height=120&section=footer" width="100%"/>
</div>
