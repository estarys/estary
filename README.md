<div align="center">

<img src="https://i.imgur.com/placeholder.png" alt="Estary Logo" width="80" height="80" />

# Estary

**Property OS for Filipino Landlords**

Stop chasing rent. Collect it automatically.

[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-beta-gold.svg)]()
[![Made in PH](https://img.shields.io/badge/Made%20in-Philippines%20🇵🇭-blue.svg)]()
[![Powered by](https://img.shields.io/badge/payments-PayMongo-purple.svg)](https://paymongo.com)

[🌐 Live Demo](https://estary.ph) · [📖 Docs](https://docs.estary.ph) · [🐛 Report Bug](https://github.com/estarys/estary/issues) · [✨ Request Feature](https://github.com/estarys/estary/issues)

</div>

---

## 📌 Overview

**Estary** is a Property Management OS built specifically for Filipino landlords. It automates rent reminders, GCash/Maya collection, tenant tracking, BIR-ready reports — so you get paid on time, every month, without lifting a finger.

Hindi lang ito basta-basta na foreign property app na na-translate. Ginawa ito **from scratch** para sa local na context — GCash, BIR compliance, NPC compliance, at lahat ng kailangan ng Pinoy landlord.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🤖 **AI Rent Reminders** | Personalized reminders sa bawat tenant — in Tagalog or English — with one-tap GCash payment link |
| 💙 **GCash & Maya Built-in** | Tenants pay using apps already on their phone. No new app to download. |
| 📊 **BIR-Ready Reports** | Auto-generated income & expense reports aligned with Philippine tax requirements |
| 📋 **Digital Lease Tracking** | Store, sign, and track leases. Get alerts before renewals expire. |
| 🔔 **Smart Overdue Escalation** | Auto-escalates reminders when rent is late. Know exactly who owes what. |
| 🏠 **Multi-Property Dashboard** | Manage apartments, condos, bedspace, and transient units in one place |
| 🔒 **NPC Compliant** | Registered with the National Privacy Commission. Data Privacy Act compliant. |

---

## 🏗️ Tech Stack

```
Frontend      →  Next.js + TailwindCSS
Backend       →  Supabase (PostgreSQL + Auth + Storage)
Payments      →  PayMongo (GCash, Maya, Cards, Bank Transfer)
AI            →  Anthropic Claude API
Hosting       →  Vercel
SMS/Comms     →  Semaphore (Philippine SMS gateway)
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js `v18+`
- npm or yarn
- Supabase account
- PayMongo account (for payments)
- Anthropic API key (for AI reminders)

### Installation

```bash
# 1. Clone the repo
git clone https://github.com/estarys/estary.git
cd estary

# 2. Install dependencies
npm install

# 3. Set up environment variables
cp .env.example .env.local
```

### Environment Variables

Fill in your `.env.local`:

```env
# Supabase
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_service_role_key

# PayMongo
PAYMONGO_SECRET_KEY=your_paymongo_secret
PAYMONGO_PUBLIC_KEY=your_paymongo_public

# Anthropic (AI Reminders)
ANTHROPIC_API_KEY=your_anthropic_key

# SMS (Semaphore)
SEMAPHORE_API_KEY=your_semaphore_key

# App
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

### Running Locally

```bash
npm run dev
# Open http://localhost:3000
```

### Database Setup

```bash
# Run Supabase migrations
npx supabase db push
```

---

## 📁 Project Structure

```
estary/
├── app/                    # Next.js App Router
│   ├── (auth)/             # Login, signup pages
│   ├── (dashboard)/        # Landlord dashboard
│   │   ├── units/          # Unit management
│   │   ├── tenants/        # Tenant management
│   │   ├── payments/       # Payment history
│   │   └── reports/        # BIR reports
│   └── api/                # API routes
│       ├── reminders/      # AI reminder engine
│       ├── webhooks/       # PayMongo webhooks
│       └── reports/        # Report generation
├── components/             # Reusable UI components
├── lib/                    # Utilities & configs
│   ├── supabase/           # DB client & queries
│   ├── paymongo/           # Payment helpers
│   └── ai/                 # Anthropic AI helpers
├── supabase/
│   └── migrations/         # Database migrations
└── public/                 # Static assets
```

---

## 💳 Supported Payment Methods

Powered by **PayMongo**:

- 💙 **GCash** — Most popular among Filipino tenants
- 💚 **Maya** (formerly PayMaya)
- 💳 **Credit / Debit Card** — Visa, Mastercard, JCB
- 🏦 **Bank Transfer** — InstaPay, PESONet

---

## 📦 Pricing Plans

| Plan | Price | Units |
|---|---|---|
| Free | ₱0/mo | Up to 2 units |
| Starter | ₱499/mo | Up to 5 units |
| Growth | ₱999/mo | Up to 20 units |
| Portfolio | ₱2,499/mo | Unlimited |

> Annual billing available — save up to 20%.

---

## 🔒 Compliance & Security

- ✅ **NPC Registered** — Compliant with the Data Privacy Act of 2012
- ✅ **Data Encryption** — All data encrypted at rest and in transit
- ✅ **BIR Aligned** — Reports formatted for Philippine rental income tax requirements
- ✅ **PCI-DSS** — Payment processing handled by PayMongo (PCI-DSS Level 1)

---

## 🤝 Contributing

Contributions are welcome! Here's how:

```bash
# 1. Fork the repo
# 2. Create your feature branch
git checkout -b feature/amazing-feature

# 3. Commit your changes
git commit -m 'feat: add amazing feature'

# 4. Push to the branch
git push origin feature/amazing-feature

# 5. Open a Pull Request
```

Please follow [Conventional Commits](https://www.conventionalcommits.org/) for commit messages.

---

## 🐛 Bug Reports & Feature Requests

Found a bug or have an idea? [Open an issue](https://github.com/estarys/estary/issues) — please include:
- What happened vs. what you expected
- Steps to reproduce
- Screenshots if applicable

---

## 📄 License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for more information.

---

## 📬 Contact

**Estary Technologies, Inc.**

- 🌐 Website: [estary.ph](https://estary.ph)
- 📧 Email: hello@estary.ph
- 💬 Support: [Book a Demo](https://estary.ph#demo)

---

<div align="center">

Built with ❤️ in the Philippines 🇵🇭

*Para sa bawat landlord na sawa nang mag-chasing ng renta.*

</div>
