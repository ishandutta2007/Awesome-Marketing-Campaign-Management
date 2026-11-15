# Awesome-Marketing-Campaign-Management

# Awesome Marketing Campaign Management

> A curated list of top Marketing Campaign Management platforms — both SaaS/Hosted commercial solutions and open-source alternatives for planning, executing, and analyzing multi-channel marketing campaigns.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [Sector Overview & Market Dynamics](#-sector-overview--market-dynamics)
- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
- [Open-Source Software](#-open-source-software)
  - [Mautic](#mautic)
  - [Laudspeaker](#laudspeaker)
  - [Notifuse](#notifuse)
  - [Helio](#helio)
  - [erxes](#erxes)
  - [Listmonk](#listmonk)
  - [Plunk](#plunk)

---

## 📊 Sector Overview & Market Dynamics

The global marketing campaign management and marketing automation market is estimated at approximately **$13B–$15B** (campaign management software) to over **$40B+** (broad marketing automation ecosystem) and is growing at an 11–15% CAGR. The sector exhibits a **bifurcated market structure**: it is **heavily concentrated** at the top tier among enterprise giants (Adobe, Salesforce, HubSpot) that benefit from deep platform lock-in and high switching costs, while remaining **highly fragmented** across the mid-market and SMB tiers where hundreds of specialized tools compete on agility, developer workflows, and pricing transparency.

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Marketing Campaign Management platforms. These are not open-source but are included as reference points for feature comparison.

| Platform | Type / Core Focus | Company Size (Valuation / Revenue) | Starting Tier Pricing | Free Tier / Free Trial Limits | Key Capabilities |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Marketo Engage** (Adobe) | Enterprise B2B marketing automation & lead nurturing | **$94.6B+** Market Cap (Adobe Inc.) / ~$25.9B Revenue ($4.75B acquisition) | **$895/month** (Growth tier, billed annually; ~20k contacts) | **No free tier or trial** (Guided sales demo only) | Lead scoring, multi-touch attribution, ABM, enterprise campaign orchestration, deep CRM sync |
| **HubSpot Marketing Hub** | Inbound marketing & CRM suite | **~$10.6B** Market Cap / ~$2.6B+ Revenue | **$15/month** (billed annually, $20/mo billed monthly; Starter tier, 1,000 marketing contacts, 1 seat) | **Free Forever** (Up to 1,000 non-marketing contacts, basic forms, email marketing with HubSpot branding) | Drag-and-drop builder, landing pages, forms, email automation, CRM integration, analytics |
| **Klaviyo** | E-commerce marketing automation & lifecycle messaging | **~$6.1B** Market Cap / ~$1.47B Revenue | **$20/month** (Base Email plan; up to 500 active profiles, 5,000 email sends/month) | **Free Forever** (Up to 250 active profiles, 500 email sends/month, 150 SMS credits, Klaviyo branding, 60 days email support) | E-commerce behavioral triggers, deep Shopify/WooCommerce sync, revenue attribution, multi-channel messaging |
| **Braze** | Enterprise cross-channel customer engagement platform | **~$5.3B** Market Cap / ~$834M Revenue | **~$2,500/month** (~$30,000/year base entry annual contract) | **14-day free trial** (Sales-assisted demo trial access to product tours and test campaigns; no permanent free tier) | Real-time journey orchestration, mobile push, in-app messaging, SMS, email, event streaming |
| **ActiveCampaign** | Marketing automation with integrated SMB CRM | **$3.0B** Valuation (Series C) / ~$200M–$290M ARR | **$15/month** (billed annually, $19/mo billed monthly; Starter plan, up to 1,000 contacts) | **14-day free trial** (1 user seat, capped at 100 email sends total, access to Professional features; no permanent free tier) | Visual automation builder, contact tracking, email marketing, CRM pipeline, site messaging |
| **Customer.io** | Behavioral event-triggered messaging platform | **$400M+** Est. Valuation / ~$100M+ ARR | **$100/month** (billed monthly; Essentials plan, up to 5,000 profiles, 1M emails/month) | **14-day free trial** (Up to 5,000 test messages across channels, 50 daily test email sends cap; no permanent free tier) | Event-driven journeys, multi-channel workflows (email, SMS, push, in-app), webhooks, data pipelines |

---

## 🟩 Open-Source Software

Self-hosted, community-driven Marketing Campaign Management tools. The open-source ecosystem spans **mature marketing automation platforms**, **modern developer-friendly engagement suites**, **self-hosted email platforms with automation**, and **AI-native growth platforms**.

### Mautic
**Stack:** PHP / MySQL | **License:** GPL-3.0
Mautic is the world's largest open-source marketing automation project, explicitly positioned for data sovereignty and privacy [citation:1][citation:12]. Key capabilities include:
- **Multi-channel marketing**: email, SMS, app or browser notifications out of the box, with more channels via plugins
- **Visual campaign builder**: drag-and-drop journey orchestration with conditional logic
- **Lead management**: scoring, stages, and behavioral tracking
- **GDPR compliance**: consent management, data erasure, and audit logs
- **Unlimited users**: no per-seat pricing
- **REST API** for CRM integration
- **Self-hosted** with full data control

**Critical deployment detail:** A dedicated cron worker is required for campaigns and scheduled emails to actually fire—the most common failure in self-hosted Mautic deployments [citation:2][citation:9]. Mautic is a direct alternative to HubSpot, ActiveCampaign, and Mailchimp, with no per-contact pricing [citation:2].
**Best for:** Organizations wanting a proven, privacy-focused marketing automation platform with full data ownership and no per-user fees, accepting the PHP/MySQL deployment and cron configuration.

### Laudspeaker
**Stack:** TypeScript / Node.js | **License:** Open Source (Y Combinator-backed)
Laudspeaker is an open-source customer engagement platform positioned as an alternative to Braze, Iterable, and Customer.io, backed by Y Combinator [citation:4][citation:6]. Key features include:
- **Event-triggered cross-channel messages**: email, SMS, push, and Slack
- **No-code journey builder**: visual tool for designing campaigns
- **Time delays and time windows**: for drip campaigns
- **User segments**: create and target specific audiences
- **Database imports**: PostgreSQL and CSV imports
- **PostHog plugin**: integrates with product analytics
- **Self-hosted or hosted**: flexible deployment options

With 2,216 GitHub stars and active development, it is a strong choice for teams wanting a modern, YC-backed alternative to commercial engagement platforms [citation:4].
**Best for:** Teams wanting an open-source Braze/Customer.io alternative with a no-code journey builder and event-triggered messaging, accepting a younger ecosystem than Mautic.

### Notifuse
**Stack:** Go / React / PostgreSQL | **License:** Open Source
Notifuse is a modern, self-hosted email marketing and transactional email platform positioned as an alternative to Mailchimp, Brevo, Klaviyo, and Listmonk [citation:3][citation:11]. Key capabilities include:
- **Visual MJML drag-and-drop email builder** with real-time preview
- **Campaign management** with A/B testing and open/click analytics
- **Visual automation flow builder** with delay, email, branch, filter, webhook, and A/B test nodes
- **Multi-provider support**: Amazon SES, Mailgun, Postmark, SendGrid, SparkPost, Mailjet, SMTP
- **Transactional email API** with automatic provider failover
- **Subscriber segmentation** and contact lists
- **SMTP relay** for routing Supabase/Firebase emails
- **Web analytics (Staminads)**: cookieless, GDPR-friendly

With a Setup Wizard for quick deployment and no per-email fees, it is a strong choice for teams wanting a modern email marketing platform [citation:3][citation:11].
**Best for:** Developers and marketers wanting a self-hosted email platform with visual automation, multi-provider support, and no per-email fees, accepting a newer project than Mautic.

### Helio
**Stack:** TypeScript / Temporal / PostgreSQL / ClickHouse | **License:** AGPL-3.0
Helio is an open-source, AI-native growth platform combining a CDP, visual journey orchestration, and multi-channel delivery . Key capabilities include:
- **Multi-channel**: email, SMS (Twilio), WhatsApp (Cloud API), web push, and in-app messages
- **Visual journey builder**: React Flow canvas compiled to a validated DAG, with durable execution via Temporal
- **AI copilot**: describe a segment, journey, or email in a sentence and get a working draft
- **Bring your own AI**: OpenAI, Anthropic, Groq, NVIDIA NIM, or local Ollama
- **MCP server**: exposes capabilities as tools for external AI agents
- **Migration importers**: HubSpot, Mailchimp, Klaviyo exports
- **Free forever**: no plans, no contact caps, no metering

It is explicitly positioned as a Mautic alternative with AI-native capabilities .
**Best for:** Teams wanting a genuinely free, AI-native marketing automation platform with durable execution and multi-channel delivery, accepting a newer project than Mautic.

### erxes
**Stack:** Node.js / MongoDB / React | **License:** AGPL-3.0 (Community Edition)
erxes is an open-source Experience Operating System (XOS) combining marketing, sales, operations, and support in one self-hostable platform, positioned as a HubSpot alternative [citation:8][citation:13]. Key features include:
- **Team Inbox**: real-time client and team communication with in-app messaging, live chat, email, and form
- **Leads**: capture visitors with customizable landing pages, forms, pop-ups, or embed placements
- **Engage**: convert prospects through email, SMS, messenger, and more
- **CRM**: all-in-one customer relationship management
- **Knowledge base**: help center for brands, products, and services
- **Sales Management**: sales funnels and pipeline control

It provides a **web-based CRM with mobile-responsive interfaces** rather than dedicated native mobile apps.
**Best for:** Organizations wanting a self-hostable HubSpot alternative with sales, marketing, and support in one platform, accepting a web-based rather than native mobile experience.

### Listmonk
**Stack:** Go / PostgreSQL | **License:** AGPL-3.0
Listmonk is a standalone, self-hosted **newsletter and mailing list manager** with a fast, clean interface. It supports multi-list management, custom subscriber attributes, segmentation, templates (HTML or Markdown), analytics, and transactional messaging via a REST API. It is designed for high-volume sending (millions of subscribers) with a single binary deployment and no external dependencies beyond PostgreSQL. It is explicitly **email-only**—no SMS, push, or journey builder.
**Best for:** Organizations wanting a lightweight, high-performance newsletter platform with segmentation and templates, accepting that it is email-only.

### Plunk
**Stack:** Node.js / PostgreSQL | **License:** Open Source
Plunk is an open-source email platform that unifies marketing, transactional, and broadcast emails in a single solution. It offers a generous free tier of 3,000 emails per month, a responsive email editor, and actions for building automations. It is positioned as a cost-effective alternative to Mailchimp, SendGrid, and Mailgun, with pricing at $0.001 per email for paid usage [citation:14].
**Best for:** Teams wanting an all-in-one open-source email platform for marketing and transactional emails with a generous free tier, accepting a newer project than established alternatives.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Visual Builder | Multi-Channel | Self-Hosted | Best For |
|----------|---------|-------|----------------|---------------|-------------|----------|
| **HubSpot** | Proprietary | Cloud | ✅ | ✅ | ❌ | HubSpot CRM integration |
| **Marketo** | Proprietary | Cloud | ✅ | ✅ | ❌ | Enterprise B2B automation |
| **Braze** | Proprietary | Cloud | ✅ | ✅ | ❌ | Enterprise cross-channel |
| **Mautic** | GPL-3.0 | PHP/MySQL | ✅ Campaign builder | ✅ Email/SMS/Notifications | ✅ | Proven OSS + data sovereignty |
| **Laudspeaker** | Open Source | TypeScript | ✅ No-code journey | ✅ Email/SMS/Push/Slack | ✅ | YC-backed Braze alternative |
| **Notifuse** | Open Source | Go/React/Postgres | ✅ MJML + Automation | (Email-focused) | ✅ | Modern email + automation |
| **Helio** | AGPL-3.0 | TypeScript/Temporal | ✅ React Flow | ✅ Email/SMS/WhatsApp/Push | ✅ | AI-native + free forever |
| **erxes** | AGPL-3.0 | Node.js/React | ✅ Sales funnels | ✅ Email/SMS/Messenger | ✅ | HubSpot alternative |
| **Listmonk** | AGPL-3.0 | Go/Postgres | ❌ (Templates) | ❌ (Email only) | ✅ | High-volume newsletters |
| **Plunk** | Open Source | Node.js/Postgres | ✅ Editor | (Email-focused) | ✅ | All-in-one email + free tier |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Marketing Campaign Management tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The marketing campaign management space is **led by Mautic** for maturity and adoption, with a proven track record as the largest open-source marketing automation project [citation:1][citation:12]. A newer generation of modern, developer-friendly platforms has emerged: **Laudspeaker** (YC-backed, Braze alternative) [citation:6], **Notifuse** (Go-based email platform with visual automation and multi-provider support) [citation:11], and **Helio** (AI-native, free forever, with Temporal-based durable execution) . **erxes** offers a broader HubSpot-style platform combining marketing, sales, and support [citation:8]. For email-only needs, **Listmonk** excels at high-volume newsletters, while **Plunk** provides a generous free tier for combined marketing and transactional email [citation:14]. No single open-source project fully replicates Braze's enterprise-scale cross-channel orchestration, but these tools cover the core campaign workflow comprehensively for self-hosted deployments.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
