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
| Frontend | React 18, Vite, TypeScript, shadcn/ui, Tailwind CSS |
| Auth | OAuth 2.0 + PKCE, custom JWT, 5-level RBAC scopes |
| Backend | Supabase Edge Functions (Deno), PostgreSQL, RLS |
| Data | RESO DD 2.0 canonical schema, Databricks Bronze/Silver/Gold ETL |
| AI/ML | AI Copilot (Next Best Action), RAG-powered assistants, lead scoring |
| Infra | Self-hosted (Apache + PM2), GitHub webhook auto-deploy |

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
