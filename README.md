# n8n Automation Workflows

A curated library of **44 production-ready n8n workflows** covering AI research, social media automation, sales, video generation, and more. Import any workflow into your n8n instance and go live in minutes.

---

## Table of Contents

- [Overview](#overview)
- [Workflow Categories](#workflow-categories)
- [Quick Start](#quick-start)
- [Workflows](#workflows)
- [Required Credentials](#required-credentials)
- [Tech Stack](#tech-stack)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This repository is a collection of battle-tested n8n automation workflows built for real business use cases. Each workflow is a self-contained JSON file that can be imported directly into any n8n instance.

**What's inside:**
- 44 workflow JSON files across 21 categories
- AI-powered automations using GPT-4, Claude, and open-source models
- Integrations with 20+ services (Gmail, Telegram, WhatsApp, Airtable, Supabase, and more)
- Multi-platform content publishing (Instagram, TikTok, YouTube, LinkedIn)
- Voice, video, and image generation pipelines

---

## Workflow Categories

| Category | Workflows | Description |
|----------|-----------|-------------|
| [Avatar](#avatar) | 1 | YouTube channel analysis & content cloning |
| [Call Agent](#call-agent) | 3 | Voice-based booking & appointment management |
| [Cold Mail](#cold-mail) | 1 | Cold email campaign automation |
| [Deep Research](#deep-research) | 1 | Multi-step AI research report generation |
| [Instagram](#instagram) | 2 | Instagram content scheduling & posting |
| [Invoice Agent](#invoice-agent) | 1 | Invoice processing & data extraction |
| [MCP Servers](#mcp-servers) | 2 | Model Context Protocol server templates |
| [Nano Banana](#nano-banana) | 1 | AI image generation & multi-platform posting |
| [Newsletter](#newsletter) | 1 | AI-written newsletter creation & distribution |
| [Personal Army](#personal-army) | 9 | Multi-purpose Telegram media creation agent |
| [RAG](#rag) | 1 | Document ingestion & retrieval-augmented generation |
| [Sales Agent](#sales-agent) | 3 | Email-based sales automation & CRM updates |
| [SEO Reports](#seo-reports) | 1 | Automated weekly SEO report generation |
| [Social Media Creator](#social-media-creator) | 2 | End-to-end content creation & cross-posting |
| [Telegram](#telegram) | 3 | Telegram AI assistants with memory & integrations |
| [UGC Contents](#ugc-contents) | 1 | User-generated content pipeline |
| [Vapi Booking Agent](#vapi-booking-agent) | 1 | Voice AI appointment booking |
| [Video Generation](#video-generation) | 6 | AI video creation & social media publishing |
| [Wait Reply Automation](#wait-reply-automation) | 2 | n8n + custom web UI integration |
| [WhatsApp Bot](#whatsapp-bot) | 3 | WhatsApp chatbots with RAG |

---

## Quick Start

### Prerequisites

- A running [n8n](https://n8n.io) instance (self-hosted or cloud)
- API credentials for the services used in your chosen workflow (see [Required Credentials](#required-credentials))

### Import a Workflow

1. Clone or download this repository
2. Open your n8n instance
3. Go to **Workflows** → click **+** → **Import from file**
4. Select the `.json` file for the workflow you want
5. Add your credentials in the **Credentials** panel
6. Click **Activate**

> Tip: Start with `Newsletter/Newsletter Automation.json` or `Cold mail/Cold mail.json` for simple, low-dependency flows.

---

## Workflows

### Avatar

**`Avatar/Clone.json`**
Scrapes a YouTube channel using Apify, analyzes the content style with GPT-4.1, and generates a replication strategy.

- **Trigger:** Manual / Webhook
- **Services:** Apify, OpenAI GPT-4.1, YouTube Data API
- **Use case:** Reverse-engineer high-performing YouTube content strategies

---

### Call Agent

Voice-based calling workflows for automated appointment booking and follow-ups.

- **Trigger:** Inbound call / Webhook
- **Services:** Voice API, scheduling backend, email
- **Use case:** Automate inbound lead qualification and calendar bookings via voice

---

### Cold Mail

**`Cold mail/Cold mail.json`**
Randomly selects from a set of cold email templates and sends campaigns automatically.

- **Trigger:** Schedule / Manual
- **Services:** Gmail / SMTP, template store
- **Use case:** A/B tested cold outreach at scale

---

### Deep Research

**`Deep research/Deep Research.json`**
The most sophisticated workflow in the library. Accepts a topic, breaks it into 5 subtopics, performs parallel web searches, then synthesizes a structured multi-chapter research report.

- **Trigger:** Web form
- **Services:** OpenRouter (Claude 3.5 Sonnet), Tavily Search, Gmail
- **Use case:** On-demand deep-dive research reports delivered to email

**Flow:**
```
Form input → Topic decomposition → Parallel web search (×5)
→ Chapter generation → Report assembly → Email delivery
```

---

### Instagram

Workflows for scheduling and posting content to Instagram.

- **Trigger:** Schedule / Manual
- **Services:** Instagram Graph API, Google Drive
- **Use case:** Consistent Instagram presence without manual posting

---

### Invoice Agent

**`Incoice agent/`**
Extracts structured data from invoice documents and populates a database or spreadsheet.

- **Trigger:** Email attachment / File upload
- **Services:** OpenAI (document parsing), Google Sheets / Airtable
- **Use case:** Automate accounts payable data entry

---

### MCP Servers

Template workflows for setting up Model Context Protocol servers in n8n.

- **Use case:** Connect n8n to Claude Desktop or other MCP-compatible clients

---

### Nano Banana

**`nano banana/`**
Generates AI images via the Nano Banana API and posts them across multiple social platforms.

- **Trigger:** Manual / Schedule
- **Services:** Nano Banana API, Instagram, Telegram
- **Use case:** Automated AI-art social accounts

---

### Newsletter

**`Newsletter/Newsletter Automation.json`**
End-to-end newsletter pipeline. Takes a topic, tone, and audience description — returns a fully written, section-by-section newsletter ready to send.

- **Trigger:** Web form
- **Services:** OpenAI GPT-4o-mini, Gmail
- **Use case:** Weekly newsletters written and sent without manual editing

---

### Personal Army

9-workflow suite centered around a Telegram-triggered media creation agent.

- **Trigger:** Telegram message (text, photo, command)
- **Services:** Telegram Bot API, Google Drive, OpenAI, image/video generation APIs
- **Use case:** Command your own AI media team from Telegram — generate images, write documents, create videos, upload to Drive

---

### RAG

**`Rag/`**
Document ingestion and question-answering pipeline using vector search.

- **Trigger:** File upload / Webhook
- **Services:** Supabase (pgvector), OpenAI embeddings, PDF/Excel parsers
- **Use case:** Chat with your own documents — PDFs, spreadsheets, internal docs

---

### Sales Agent

3-workflow email sales automation suite.

**`Sales Agent/Email_sales_Agent.json`** — Core flow:

- **Trigger:** Gmail (polls every minute)
- **Services:** Gmail, OpenAI, Airtable, knowledge base
- **Use case:** AI reads incoming sales emails, updates CRM notes, searches knowledge base, and drafts replies — all automatically

---

### SEO Reports

**`SEO Reports/`**
Generates automated weekly SEO performance reports and emails them to stakeholders.

- **Trigger:** Schedule (weekly)
- **Services:** SEO API, Gmail
- **Use case:** Hands-free SEO monitoring and reporting

---

### Social Media Creator

End-to-end content creation and cross-platform publishing.

- **Trigger:** Form / Manual
- **Services:** OpenAI, Instagram, TikTok, YouTube, Google Drive
- **Use case:** Generate a post idea → produce content → publish everywhere automatically

---

### Telegram

3 Telegram bot workflows with AI, memory, and Google integrations.

- **Trigger:** Telegram message
- **Services:** Telegram Bot API, OpenAI, Gmail, Google Calendar
- **Highlights:** Conversation memory, email drafting, calendar event creation from chat
- **Use case:** Personal AI assistant living inside Telegram

---

### UGC Contents

User-generated content collection and moderation pipeline.

- **Trigger:** Form submission / Webhook
- **Use case:** Collect, review, and route UGC from customers or creators

---

### Vapi Booking Agent

**`Vapi booking agent/`**
Voice AI that handles inbound calls, understands booking intent, and schedules appointments.

- **Trigger:** Inbound call (Vapi webhook)
- **Services:** Vapi, calendar API, email confirmation
- **Use case:** 24/7 AI receptionist for service businesses

---

### Video Generation

6-workflow AI video creation and publishing suite.

| Workflow | Video Engine | Platform |
|----------|-------------|----------|
| Sora Video Generator | OpenAI Sora | Multi-platform |
| Veo3 Creator | Google Veo3 | Multi-platform |
| HeyGen Avatar | HeyGen | YouTube / LinkedIn |
| D-ID Face Animation | D-ID | Instagram / TikTok |
| LinkedIn Post Generator | Combined | LinkedIn |
| TikTok Publisher | Combined | TikTok |

- **Use case:** Script → AI video → auto-publish to social media, all in one workflow

---

### Wait Reply Automation

**`Wait reply autoamtionn/`**
Demonstrates how to pair n8n with a custom web frontend using the `resumeUrl` webhook pattern.

- **Backend:** Node.js + Express proxy
- **Use case:** Build custom UIs on top of n8n workflows with file streaming support
- **Docs:** See [`Wait reply autoamtionn/project-edited.md`](Wait%20reply%20autoamtionn/project-edited.md)

---

### WhatsApp Bot

3 workflows for WhatsApp automation including a full RAG-powered chatbot.

- **Trigger:** WhatsApp message (webhook)
- **Services:** WhatsApp Business API, OpenAI, Supabase (vector DB)
- **Use case:** Customer support bot that answers from your own documents

---

## Required Credentials

Configure these in your n8n **Credentials** settings before activating workflows:

| Credential | Used By |
|-----------|---------|
| OpenAI API Key | Most AI workflows |
| OpenRouter API Key | Deep Research |
| Google OAuth 2.0 | Gmail, Drive, Calendar |
| Telegram Bot Token | Telegram, Personal Army |
| Airtable Personal Access Token | Sales Agent |
| Supabase URL + Key | RAG, WhatsApp Bot |
| WhatsApp Business API | WhatsApp Bot |
| Instagram Graph API | Instagram, Social Media Creator |
| Apify API Key | Avatar |
| Tavily API Key | Deep Research |
| Nano Banana API Key | Nano Banana |
| HeyGen API Key | Video Generation |
| D-ID API Key | Video Generation |
| Vapi API Key | Vapi Booking Agent |

> Credentials are stored securely inside your n8n instance and never committed to this repository.

---

## Tech Stack

| Layer | Technologies |
|-------|-------------|
| **Orchestration** | n8n |
| **AI / LLMs** | OpenAI GPT-4o, GPT-4.1, Claude 3.5 Sonnet (OpenRouter) |
| **Vector DB** | Supabase pgvector |
| **CRM / Data** | Airtable, Google Sheets |
| **Storage** | Google Drive |
| **Messaging** | Telegram, WhatsApp, Gmail |
| **Social Media** | Instagram, TikTok, YouTube, LinkedIn |
| **Video AI** | OpenAI Sora, Google Veo3, HeyGen, D-ID |
| **Image AI** | Nano Banana, DALL-E |
| **Web Scraping** | Apify |
| **Search** | Tavily |
| **Custom Backend** | Node.js + Express.js |

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on submitting new workflows or improvements.

---

## License

[MIT](LICENSE)
