# MindMate Chatbot

**An AI-powered chatbot for daily mental wellness check-ins and personalized mindfulness exercises — built with Next.js.**

MindMate helps users build healthier daily habits through short conversational check-ins, adaptive mindfulness exercises, mood journaling, and data-backed insights. This repository contains the web frontend, backend API, and AI integration skeleton for a hackathon-ready MVP (≈90% of planned features).

---

## 👥 Team Members

**Hemil Hansora**  
**Vrund Patel**  
**Meet Soni**

---

## 💚 Problem Statement

Many people live with daily stress, anxiety, and burnout but lack a low-friction, affordable, and stigma-free way to check in with their mental health. Existing tools are often generic, hard to maintain, or expensive. MindMate provides gentle, science-backed daily check-ins and personalized mindfulness exercises so users can cultivate consistent self-care and spot patterns before issues escalate.

---

## 🏆 Project Overview

MindMate is a compassionate, AI-driven companion that:
- Checks in with users conversationally each day,
- Provides short, adaptive mindfulness exercises (breathing, grounding, micro-meditations),
- Tracks mood and journal entries over time,
- Generates simple insights and nudges based on user history,
- Prioritizes privacy, safety, and clear escalation flows for crisis situations.

This project was built for hackathon delivery with a pragmatic, demo-focused architecture using Next.js for rapid iteration and an extensible AI orchestration layer.

---

## ✨ Key Features

### 📌 Core (MVP)
- **Signup / Login** (email + OAuth)
- **Conversational Daily Check-ins** — 3–5 adaptive questions + free text
- **Mindfulness Exercise Library** — short guided breathing, grounding, micro-meditations
- **Mood Journal & Timeline** — view, edit, and search past entries
- **AI Chat** — LLM-driven empathetic responses and exercise suggestions
- **Crisis Detection & Escalation** — safety-first pipeline showing helplines & resources
- **Settings & Notifications** — schedule reminders and privacy controls

### 🌱 Stretch / Future
- Insights dashboard & trend analysis
- Voice interaction (ASR/TTS)
- Wearables integration (HR/sleep)
- WhatsApp/Telegram check-ins
- Mood forecasting & proactive nudges
- Gamification (streaks & badges)

---

## 🛠️ Tech Stack

**Frontend**
- Next.js (React) — PWA-capable  
- Tailwind CSS — utility styling  
- React Query / SWR — data fetching

**Backend**
- Next.js API Routes or Node + Express  
- PostgreSQL (or MongoDB) — primary persistence  
- Redis — sessions, caching, queues

**AI**
- OpenAI / chosen LLM for dialogue  
- Lightweight sentiment/emotion classifier (local or via API)  
- Prompt templates + safety filter layer

**Dev / Infra**
- Docker & docker-compose (local)  
- GitHub Actions (CI)  
- Vercel / Cloud Run / DigitalOcean for deployment  
- Sentry for error tracking (optional)

---

## 📁 Project Structure (recommended)

mindmate-chatbot/
├─ README.md
├─ .env.example
├─ frontend/ # Next.js app (UI + API routes)
│ ├─ package.json
│ └─ src/
│ ├─ components/
│ ├─ app/ or pages/
│ ├─ services/
│ └─ styles/
├─ backend/ # Optional standalone backend (if used)
│ ├─ package.json
│ └─ src/
├─ ai/ # prompts, adapters, safety filters
├─ infra/ # deployment scripts / IaC
├─ docs/ # design docs, API spec
└─ scripts/ # seeds, migrations, helpers

yaml
Copy code

---

## 🚀 Quick Start (Local Development)

### Prerequisites
- Node.js 18+  
- Docker & docker-compose (recommended)  
- Git

### Run locally (without Docker)
```bash
# Clone
git clone https://github.com/<your-org>/mindmate-chatbot.git
cd mindmate-chatbot

# Frontend (Next.js)
cd frontend
npm install
cp .env.example .env.local   # update keys (OPENAI_API_KEY, DATABASE_URL, etc.)
npm run dev
# Open http://localhost:3000
Run with Docker (recommended)
bash
Copy code
# from repo root
docker-compose up --build
# frontend -> http://localhost:3000
🔐 .env Example
Place a .env.local in frontend/ (or repo root if unified):

env
Copy code
NEXT_PUBLIC_APP_URL=http://localhost:3000

# Database & Redis
DATABASE_URL=postgres://postgres:password@localhost:5432/mindmate
REDIS_URL=redis://localhost:6379

# Auth
JWT_SECRET=your_jwt_secret
NEXTAUTH_URL=http://localhost:3000
GOOGLE_CLIENT_ID=...
GOOGLE_CLIENT_SECRET=...

# AI
OPENAI_API_KEY=sk-...
AI_MODEL=gpt-4o-mini

NODE_ENV=development
SENTRY_DSN=
Never commit real secrets. Use .env.example with placeholders.

🔌 API Endpoints (Overview)
Example if using Next.js API routes or a small express backend:

bash
Copy code
POST   /api/auth/register
POST   /api/auth/login
GET    /api/auth/me

POST   /api/checkins
GET    /api/checkins?from=&to=
GET    /api/exercises
POST   /api/exercises/start
POST   /api/journal
GET    /api/insights/summary
POST   /api/ai/respond
POST   /api/webhooks/whatsapp
🗂️ Data Model (Simplified)
users

id, email, name, password_hash, timezone, prefs, created_at

checkins

id, user_id, mood_score, mood_label, text, sentiment, tags, created_at

exercises

id, title, type, duration_sec, content_url, metadata

journals

id, user_id, title, body, created_at

sessions

id, user_id, exercise_id, started_at, completed_at, rating

🧪 Testing
Unit tests (Jest / React Testing Library) for frontend components and backend services

E2E tests (Cypress) for critical flows (signup, check-in, play exercise)

Seed/demo data to make dashboards look populated for the hackathon demo

📈 Performance & Privacy
Performance

Caching (Redis) for frequent reads

DB indexes for checkins & users

Lazy loading and image optimization (next/image or native)

Privacy & Safety

TLS in transit, DB encryption at rest recommended

Rule-based + ML safety filters for crisis detection

Explicit disclaimer: not a replacement for professional therapy

Easy “Delete my data” option and privacy-first defaults

🧭 Hackathon Demo Script
Landing & Signup

Show landing page, sign up (or use demo account)

Daily Check-in

Start a conversational check-in → complete 3 Qs → show saved entry in timeline

Mindfulness Exercise

Play a 2-minute breathing exercise → mark complete → show streak increment

AI Chat

Ask: “I’m stressed about deadlines” → show empathetic response + exercise recommendation

Crisis Flow (Demo Mode)

Use the demo-only “simulate crisis” toggle to show helpline modal & escalation flow

Insights

Open Insights to display seeded mood trends and AI summary

🛠️ Roadmap
Short term

Fully-featured Insights dashboard, Admin panel, Scheduled notifications

Medium term

Voice (ASR/TTS), WhatsApp integration, wearable data

Long term

Advanced personalization, mood forecasting, mobile apps

🤝 Contributing
We welcome contributions! Preferred workflow:

Fork → create branch feat/your-feature

Add tests & documentation

Open PR with clear description

Follow ESLint, Prettier, and add tests for new features.

⚖️ License
This project is released under the MIT License. See LICENSE for details.

🙏 Acknowledgements
Built with care by the MindMate team — Hemil, Vrund, and Meet — for our hackathon. Thanks to the open-source libraries, model providers, and the broader developer community that made this possible.

📞 Contact / Support
Hemil Hansora — GitHub: @hemil-hansora

Vrund Patel — GitHub: @VrundPatel153

Meet Soni — GitHub: @meetsioni

For questions or demo access, open an issue or reach out to the team on the project repo.

Built with ❤️ — MindMate: gentle check-ins, kinder days.