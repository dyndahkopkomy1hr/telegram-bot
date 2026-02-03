# telegram bot

## Introduction
Marketing and compliance teams often need to monitor paid ads for specific keywords, locations, or competitors—then alert stakeholders when something changes. The challenge is doing this **reliably and compliantly** without evasion tactics or fragile scraping.

<p align="center">
  <a href="https://Appilot.app" target="_blank"><img src="https://github.com/Instagram-Automations/Footer-test/blob/main/appilot-baner.png" alt="Appilot Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank"><img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"></a>
  <a href="mailto:support@appilot.app" target="_blank"><img src="https://img.shields.io/badge/Email-support@appilot.app-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"></a>
  <a href="https://Appilot.app" target="_blank"><img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website"></a>
  <a href="https://discord.gg/3YrZJZ6hA2" target="_blank"><img src="https://img.shields.io/badge/Join-Appilot_Community-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Appilot Discord"></a>
</p>



<p align="center">
Created by Appilot, built to showcase our approach to Automation! <br>
If you are looking for custom <strong> telegram bot </strong>, you've just found your team — Let’s Chat.&#128070; &#128070;
</p>

**Telegram bot** is a **policy-aware ads monitoring and alerting bot** that:
- ingests paid-ad signals from **permitted sources** (official transparency data, licensed SERP APIs, or first-party feeds),
- detects **net-new ad changes** per keyword,
- sends clean, clickable alerts to Telegram,
- stores history with audit logs and observability.

> This repository intentionally avoids stealth/fingerprinting evasion and unauthorised scraping.

---

## Why This Automation Matters
- Faster detection of new campaigns, creatives, and messaging shifts  
- Change tracking that avoids duplicate alerts and alert fatigue  
- Auditable history for reviews and reporting  
- More reliable than “stealth scraping” approaches  
- Safer long-term maintenance and fewer bans/outages  

---

## Core Features

| Feature | Description |
|---|---|
| Source Adapters | Plug-in adapters for approved data sources (transparency feeds, licensed APIs, exports) |
| Keyword/Location Watches | Configurable watch lists with optional geo/language tags |
| Paid-Ad Filtering | Extract only sponsored/paid ad entries (source-dependent) |
| Change Detection | Hash-based diffing to alert only on net-new ads |
| Telegram Alerts | Rich messages with previews, timestamps, and clickable URLs |
| Batching | Bundle multiple changes into one Telegram notification |
| Rate Limiting | Safe polling intervals, quotas, and backoff |
| Audit Logs | Store what was observed, when, and from which source |
| Observability | Structured logs + metrics + health checks |

---

## How It Works

| Stage | Operation | Safety Control |
|---|---|---|
| 1. Configure | Define keywords, locations, schedules | Allowlist + schema validation |
| 2. Collect | Pull ads from approved source | Rate-limited requests |
| 3. Normalize | Canonicalize fields (title/url/desc) | Deterministic parsing |
| 4. Diff | Hash + compare against history | Idempotent detection |
| 5. Alert | Send Telegram message(s) | Batch + cooldown |
| 6. Record | Save snapshots and outcomes | Audit-first storage |
| 7. Observe | Metrics + health endpoints | Alert on failures |

> **Safety principle:** Prefer official/licensed data sources over bypassing protections.

---

## Tech Stack
- Python
- Telegram Bot API (python-telegram-bot)
- PostgreSQL / SQLite (history + audits)
- Optional Playwright **only** for *your own* pages or explicitly permitted monitoring targets
- Structured JSON logging

---

## Directory Structure
```
telegram-bot/
├── app/
│ ├── main.py
│ ├── config/
│ │ ├── loader.py
│ │ └── schema.py
│ ├── sources/
│ │ ├── adapter_base.py
│ │ ├── transparency_feed.py
│ │ └── licensed_serp_api.py
│ ├── processing/
│ │ ├── normalize.py
│ │ ├── hashing.py
│ │ └── diff.py
│ ├── alerts/
│ │ ├── telegram_sender.py
│ │ └── formatter.py
│ ├── storage/
│ │ ├── db.py
│ │ └── models.py
│ ├── policies/
│ │ ├── rate_limits.py
│ │ └── compliance.py
│ └── observability/
│ ├── logging.py
│ ├── metrics.py
│ └── health.py
├── config/
│ ├── watches.yaml
│ └── settings.yaml
├── tests/
│ ├── test_diff.py
│ └── test_formatting.py
└── README.md
```

---

## Use Cases
- Monitor competitor paid ad messaging changes  
- Track brand compliance keywords and restricted claims  
- Alert teams when a new ad creative appears for a market  
- Build an internal “ads change log” for weekly reporting  
- Incident response: detect sudden ad copy changes quickly  

---

## FAQs

**Q: Can this scrape Google search ads using stealth plugins and proxy rotation?**  
No. Evasion and unauthorised scraping are excluded by design.

**Q: What data sources are supported?**  
This repo is built around **adapter modules**. You can plug in:
- official transparency datasets/feeds (when available),
- advertiser-provided exports,
- licensed SERP providers that permit automated access.

**Q: Why hashing and “net-new” detection?**  
To prevent repeated alerts when the same ad appears across multiple polls.

**Q: Can I batch alerts?**  
Yes. You can batch per keyword, per time window, or per run.

---

## Performance & Reliability Benchmarks
- Polling scales by keyword count with per-source rate limits  
- Sub-second diffing for typical batches (hundreds–thousands of ads)  
- Idempotent runs: safe restarts without duplicate alerts  
- Clear failure modes with structured logs and retry backoff  

---

<p align="center">
<a href="https://cal.com/app-pilot-m8i8oo/30min" target="_blank">
 <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
 <a href="https://www.youtube.com/@Appilot-app/videos" target="_blank">
  <img src="https://img.shields.io/badge/ð¥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
 </a>
</p>

