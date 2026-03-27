# LinkedIn Content Automation 🤖

> Automated pipeline that scrapes AI/ML news, processes it through an LLM, and publishes LinkedIn-formatted posts daily at 1 PM.

---

## How it works

```
Scraper (BeautifulSoup/RSS)
        ↓
Collects latest AI/ML news & articles
        ↓
LLM API
  → Summarizes and formats content for LinkedIn
  → Adds relevant hashtags and structure
        ↓
n8n Scheduler
  → Triggers daily at 1:00 PM
  → Posts directly to LinkedIn
```

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| n8n | Workflow automation & scheduling |
| Python | Web scraping & data processing |
| BeautifulSoup | News scraping |
| LLM API | Content formatting & generation |
| LinkedIn API | Auto-publishing |

---

## Setup

### Prerequisites
- Node.js 18+
- Python 3.10+
- n8n installed
- LinkedIn Developer account
- LLM API key (OpenAI / Anthropic / etc.)

### Run n8n locally

```bash
npx n8n
```
or 

'''bash 
docker run -it --rm --name n8n -p 5678:5678 -v ~/.n8n:/home/node/.n8n docker.n8nio/n8n
'''bash

Then open `http://localhost:5678` in your browser.

### Import the workflow

1. Open n8n at `http://localhost:5678`
2. Click **"Workflows"** → **"Import from File"**
3. Select `workflow.json` from this repo
4. Add your credentials (LinkedIn OAuth, LLM API key)
5. Toggle the workflow **Active**

---

## Environment Variables

```env
LLM_API_KEY=
LINKEDIN_CLIENT_ID=
LINKEDIN_CLIENT_SECRET=
```

---

## Author

**Sanskaar Thukral** — B.Tech ECE + AI Minor, MAIT (2026)  
📧 tsanskaar@gmail.com · [LinkedIn](https://linkedin.com/in/sanskaar-thukral) · [GitHub](https://github.com/Ghosty032)
