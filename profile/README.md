<p align="center">
  <a href="https://sharpsir.group">
    <img src="https://raw.githubusercontent.com/sharpsir-group/.github/main/brand/logo-blue.png" alt="Sharp Sotheby's International Realty" width="400" />
  </a>
</p>

<h3 align="center">Sharp Matrix — Digital Platform for Luxury Real Estate</h3>

<p align="center">
  Multi-app platform powering brokerage operations across Cyprus, Hungary, and Kazakhstan.
  <br />
  Built with <a href="https://lovable.dev">Lovable</a> + <a href="https://supabase.com">Supabase</a> + <a href="https://www.databricks.com">Databricks</a>.
</p>

---

### Platform Architecture

```
Channels (WhatsApp, Email, Web, Ads)
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
| App Builder | [Lovable](https://lovable.dev) — AI-powered app builder |
| Frontend | React 18, Vite, TypeScript, shadcn/ui, Tailwind CSS, TanStack Query |
| Auth & IAM | OAuth 2.0 + PKCE, custom JWT, HMAC-SHA256, 5-level RBAC (self → team → global → org_admin → system_admin) |
| Backend | Supabase Edge Functions (Deno/TypeScript), PostgreSQL 15, Row-Level Security |
| Realtime | Supabase Realtime (WebSocket) — live updates across all apps |
| Data Standard | [RESO DD 2.0](https://www.reso.org/) — canonical data layer, OData 4.0 Web API |
| Data Pipeline | Databricks — Medallion ETL (Bronze → Silver → Gold), CDC every 15 min, Delta Lake |
| AI/ML | AI Brokerage Copilot, RAG (retrieval-augmented generation), semantic search, lead scoring, recommendation engine, personalization |
| NLP & LLM | OpenAI GPT-4, embeddings, AI agents for Next Best Action & document generation |
| Channels | WhatsApp Business API (Twilio), Microsoft Graph (Exchange, Calendar, AD), Telegram Bot API, SMTP/IMAP |
| Integrations | Qobrix REST API, Dash/Anywhere.com API, SIR syndication, Google/Meta Ads API |
| Infra | Self-hosted Linux (Apache, PM2, Node.js), automated deploy via GitHub webhooks |
| Observability | Structured logging, PM2 monitoring, Supabase Dashboard, Databricks job metrics |
| i18n | i18next — English and Russian |

### Design Philosophy

> **The broker works with the client. The system works with the process.**

- **RESO DD 2.0** as the canonical data layer — one field name everywhere, every app, every market
- **Multi-app, single data truth** — no translation layers between apps
- **Regional customization on a unified core** — Cyprus, Hungary, Kazakhstan share one platform
- **AI Copilot at the heart** — context-aware Next Best Action, automated matching, document generation

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
