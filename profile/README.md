<p align="center">
  <a href="https://sharpsir.group">
    <img src="https://raw.githubusercontent.com/sharpsir-group/.github/main/brand/logo-blue.png" alt="Sharp Sotheby's International Realty" width="400" />
  </a>
</p>

<h3 align="center">Sharp Matrix — Digital Platform for Luxury Real Estate</h3>

<p align="center">
  Multi-app platform powering brokerage operations across Cyprus, Hungary, and Kazakhstan.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React_18-61DAFB?style=flat&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white" alt="Tailwind" />
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat&logo=supabase&logoColor=white" alt="Supabase" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Deno-000000?style=flat&logo=deno&logoColor=white" alt="Deno" />
  <img src="https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white" alt="Databricks" />
  <img src="https://img.shields.io/badge/Delta_Lake-003366?style=flat&logo=delta&logoColor=white" alt="Delta Lake" />
  <img src="https://img.shields.io/badge/OpenAI_GPT--4-412991?style=flat&logo=openai&logoColor=white" alt="OpenAI" />
  <img src="https://img.shields.io/badge/Claude_Opus-CC785C?style=flat&logo=anthropic&logoColor=white" alt="Claude" />
  <img src="https://img.shields.io/badge/Gemini-8E75B2?style=flat&logo=googlegemini&logoColor=white" alt="Gemini" />
  <img src="https://img.shields.io/badge/HumaticAI-00C896?style=flat&logoColor=white" alt="HumaticAI" />
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white" alt="LangChain" />
  <img src="https://img.shields.io/badge/Qwen3_Embeddings-6F42C1?style=flat&logoColor=white" alt="Qwen3" />
  <img src="https://img.shields.io/badge/Cursor_IDE-000000?style=flat&logo=cursor&logoColor=white" alt="Cursor" />
  <img src="https://img.shields.io/badge/Lovable-FF6B6B?style=flat&logo=heart&logoColor=white" alt="Lovable" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Apache-D22128?style=flat&logo=apache&logoColor=white" alt="Apache" />
  <img src="https://img.shields.io/badge/PM2-2B037A?style=flat&logo=pm2&logoColor=white" alt="PM2" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white" alt="GitHub" />
  <img src="https://img.shields.io/badge/Twilio-F22F46?style=flat&logo=twilio&logoColor=white" alt="Twilio" />
  <img src="https://img.shields.io/badge/Microsoft_Graph-0078D4?style=flat&logo=microsoft&logoColor=white" alt="Microsoft" />
  <img src="https://img.shields.io/badge/WhatsApp_API-25D366?style=flat&logo=whatsapp&logoColor=white" alt="WhatsApp" />

  <img src="https://img.shields.io/badge/OData_4.0-0078D4?style=flat&logo=odata&logoColor=white" alt="OData" />
  <img src="https://img.shields.io/badge/RESO_DD_2.0-1A1A2E?style=flat&logoColor=white" alt="RESO" />
  <img src="https://img.shields.io/badge/OAuth_2.0_+_PKCE-EB5424?style=flat&logo=auth0&logoColor=white" alt="OAuth" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black" alt="Linux" />
</p>

---

### Platform Architecture

```
Channels (WhatsApp, Email, Web, Microsoft 365, Ads)
  │
  ▼
Matrix Apps ── built from a shared App Template (React + Vite + shadcn/ui)
  │
  ├── CDL-Connected Apps ─── Pipeline, Contact Mgmt, Broker Dashboard
  │      read/write shared RESO DD 2.0 data layer
  │
  ├── Domain-Specific Apps ── HRMS, Financial Mgmt, ITSM
  │      own Supabase databases, shared SSO auth
  │
  └── AI Services ── Zoe Assistant, AI Web Chat, Blog Generator
         context-aware copilots for brokers, managers, and visitors
  │
  ▼
Supabase (CDL + Auth)  ◄──►  Databricks (DWH + ETL)  ◄──►  MLS / Portals
```

**24 apps** in the ecosystem — 11 live, 7 in progress, 6 planned.

### Tech Stack

| Layer | Technology |
|---|---|
| AI Development | [Cursor](https://cursor.com) (Claude Opus) — AI-native IDE for platform engineering |
| App Builder | [Lovable](https://lovable.dev) — AI-powered app builder, generates full-stack apps |
| Frontend | React 18, Vite, TypeScript, shadcn/ui, Tailwind CSS, TanStack Query, Radix UI |
| Auth & IAM | OAuth 2.0 + PKCE, custom JWT, HMAC-SHA256, 5-level RBAC (self → team → global → org_admin → system_admin) |
| Backend | Supabase Edge Functions (Deno/TypeScript), PostgreSQL 15, Row-Level Security |
| Realtime | Supabase Realtime (WebSocket) — live updates across all apps |
| Data Standard | [RESO DD 2.0](https://www.reso.org/) — canonical data layer, OData 4.0 Web API |
| Data Pipeline | Databricks — Medallion ETL (Bronze → Silver → Gold), CDC every 15 min, Delta Lake |
| AI/ML | AI Brokerage Copilot, LangChain, RAG (retrieval-augmented generation), semantic search, lead scoring, recommendation engine, personalization |
| NLP & LLM | OpenAI GPT-4, Claude (Anthropic), Google Gemini, Qwen3 embeddings, AI agents for Next Best Action & document generation |
| Conversational AI | [HumaticAI](https://humantic.ai) — autonomous WhatsApp replies, personality profiling, lead qualification |
| Channels | WhatsApp Business API (Twilio), Microsoft Graph (Exchange, Calendar, AD), SMTP/IMAP |
| Integrations | Qobrix REST API, Dash/Anywhere.com API, SIR syndication, Google/Meta Ads API |
| Infra | Self-hosted Linux (Debian), Apache, PM2, Node.js, Python 3.13, automated deploy via GitHub webhooks |
| Observability | Structured logging, PM2 monitoring, Supabase Dashboard, Databricks job metrics |
| i18n | i18next — English and Russian |

### Sharp Matrix DNA

> **We don't take ourselves too seriously. It's extremely difficult to compete with someone building for pleasure and fun.**

Sharp Matrix is not a product — it's an **AI-native digital ecosystem** that elevates luxury real estate brokerage to a completely new level. While others debated chatbot UX, we shipped 24 interconnected apps, autonomous assistants, and a unified data platform that runs a brokerage across three countries. Everything here — every line of code, every AI model, every pipeline — exists to make Sharp Matrix better.

- **Platform, not a feature** — Sharp Matrix is Zoe (internal copilot), AI Web Assistant (visitor-facing), Blog Generator, HumaticAI (autonomous WhatsApp), lead scoring, property matching, semantic search, recommendation engine, 24 apps, and a RESO-standard data layer — all wired together, sharing context, learning from every interaction.
- **From language to agency** — the ingredients for autonomous systems existed for years. Sharp Matrix combined them into a living platform integrated into WhatsApp, email, Microsoft 365, and daily broker workflows — where AI is not a tool you open, but a colleague that works alongside you.
- **One data truth, three markets** — RESO DD 2.0 as the canonical layer. One field name everywhere, every app, every market. Cyprus, Hungary, Kazakhstan share one platform with regional configuration, not code forks.
- **The broker works with the client. The system works with the process.** — AI Copilot handles data, timing, matching, and forecasting. Brokers focus on what only humans do well: build trust, negotiate, and close deals.
- **Creative problem-solving over programming** — Sharp Matrix agents demonstrate world knowledge that was never explicitly coded. They figure things out, improvise, and solve problems we didn't anticipate.
- **Vibe coding > structured development** — while big labs focused on language models, we built Sharp Matrix through iterative "vibe coding" — shipping fast, learning faster, and allowing more experimentation than any corporate environment would permit.

### Open Source

| Project | Description |
|---|---|
| **[GitHub Watcher](https://github.com/sharpsir-group/github-watcher)** | Zero-dependency webhook server that auto-deploys repos on `git push`. No CI needed. |
| **[Matrix Platform KB](https://github.com/sharpsir-group/matrix-platform-kb)** | Full knowledge base for the Sharp Matrix platform — architecture, data models, business processes, RESO DD mapping. |
| **[MLS 2.0 Pipeline](https://github.com/sharpsir-group/mls_2_0)** | Databricks ETL pipeline + RESO Web API for MLS data ingestion (Bronze/Silver/Gold). |

### Strategy Highlights (2026–2028)

- **90%+ process automation** (from 20-30% today)
- **Lead processing in 30 min** (down from 4 hours)
- **Sales cycle cut to 50-60 days** (from 90-150)
- **3x website traffic**, **3x marketing CTR**, **+160% deal close rate**
- 7-phase rollout: Foundation → CRM Migration → AI Copilot → Client Portal → Marketing Automation → Analytics → Optimization

---

<p align="center">
  <a href="https://sharpsir.group">sharpsir.group</a>
</p>
