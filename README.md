# Guillaume Pien — Data & Analytics Portfolio

**Data Analytics · Business Intelligence · Automation · AI**  
📍 Greater Ottawa Metropolitan Area · [LinkedIn](https://www.linkedin.com/in/gpn)

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Microsoft Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=googlesheets&logoColor=white)
![Zapier](https://img.shields.io/badge/Zapier-FF4A00?style=for-the-badge&logo=zapier&logoColor=white)
![Power Automate](https://img.shields.io/badge/Power%20Automate-0066FF?style=for-the-badge&logo=powerautomate&logoColor=white)
![Power Apps](https://img.shields.io/badge/Power%20Apps-742774?style=for-the-badge&logo=powerapps&logoColor=white)
![OpenAI](https://img.shields.io/badge/GPT--4-412991?style=for-the-badge&logo=openai&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Data Visualization](https://img.shields.io/badge/Data%20Visualization-E84393?style=for-the-badge&logo=googleanalytics&logoColor=white)
![Storytelling](https://img.shields.io/badge/Data%20Storytelling-FF6B6B?style=for-the-badge&logo=chartdotjs&logoColor=white)

---

## About

## About

I'm a PharmD and data professional with 10+ years of experience in the 
pharmaceutical industry, turning complex operational data into decisions that 
actually get made. I work across the full analytics stack — from data modeling 
and SQL to Power BI dashboards, Python pipelines, and AI-powered automation — 
with a consistent focus on building things that are actually used, not just built.

My background combines deep pharmaceutical domain knowledge with hands-on 
technical expertise. That combination means I spend less time learning the 
business context and more time solving the right problems — whether that's 
a KPI framework for a leadership team, a data quality monitoring system, or 
an AI-powered automation pipeline.

What drives my work is a strong belief that analytics tools are only as good 
as the experience of using them. I invest heavily in UX — report layout, 
navigation flow, the right level of detail at the right level of the 
organisation — because a dashboard that people actually open every morning 
is worth ten technically perfect reports that nobody reads. Good data products 
earn their place in someone's workflow; they don't need to be explained.

---

## Projects

### 1. 🏅 True Olympic Powerhouse — Sanofi-Wide Analytics Competition

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-4A4A4A?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Storytelling](https://img.shields.io/badge/Data%20Storytelling-FF6B6B?style=for-the-badge&logo=chartdotjs&logoColor=white)
![Data Visualization](https://img.shields.io/badge/Data%20Visualization-E84393?style=for-the-badge&logo=googleanalytics&logoColor=white)
![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)
![Top 5](https://img.shields.io/badge/🏅%20Top%205%20%2F%2080%20Teams-FFD700?style=for-the-badge&logoColor=black)

A Power BI dashboard exploring 120 years of Olympic history — built for a company-wide analytics competition at Sanofi, open to all global teams. **Finished Top 5 out of 80 competing teams.**

**The central question:** The IOC does not officially rank countries. Yet every broadcaster publishes its own medal table, using different methods for different reasons. This dashboard makes that ambiguity the subject — letting users choose their own ranking methodology and discover who the *True Olympic Powerhouse* really is, depending on what they value.

**What makes it technically strong:**
- Star schema data model with dedicated fact tables, parameter tables, and a 40+ measure DAX layer
- Field parameters drive metric switching across 5 medal counting methodologies (Gold First, weighted counts, normalized by delegation size) — no page duplication, no bookmarks
- Composite scoring on the Results page uses rank-based normalization so metrics with different scales (medal counts vs. number of Games organized) contribute proportionally
- SVG flags rendered inline, personalized greetings via `USERPRINCIPALNAME()`, interactive sport icon grid as a slicer

**What makes it stand out as a product:** The dashboard is structured as a guided narrative — each of the 4 analytical sections (Medal & Performance, Organizations & Participations, Sports & Athletes, Final Results) builds toward a conclusion the user reaches themselves. The answer to "who wins the Olympics" is genuinely theirs to decide.

![TOP Dashboard](./screenshots/TOP.gif)

📁 [View full project README & report](https://github.com/gpn64/TOP-Dashboard-PowerBI/tree/main)

---

### 2. 🏥 Healthcare AutoClaims — AI-Powered Receipt Tracker

![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)
![Zapier](https://img.shields.io/badge/Zapier-FF4A00?style=for-the-badge&logo=zapier&logoColor=white)
![Airtable](https://img.shields.io/badge/Airtable-18BFFF?style=for-the-badge&logo=airtable&logoColor=white)
![OpenAI](https://img.shields.io/badge/GPT--4.1%20mini-412991?style=for-the-badge&logo=openai&logoColor=white)
![Regex](https://img.shields.io/badge/Regex-4A4A4A?style=for-the-badge&logo=gnubash&logoColor=white)

A fully automated pipeline that watches a Gmail inbox for healthcare receipts, extracts structured data from PDF invoices using GPT-4.1 mini, and builds a live reimbursement tracking database — with zero manual data entry on the intake side.

**What it does:**
- Gmail auto-tags incoming provider emails with a `healthcare` label; Zapier fires on each match, capturing the email link and PDF attachment into Airtable
- An AI Assist column runs a constrained GPT-4.1 mini prompt against each invoice, extracting: clinic name, patient name, care type, appointment date, practitioner, duration, and amount billed
- Regex formula columns parse each field out of the AI output into clean, queryable cells
- A `type_of_service` formula normalizes raw care descriptions into insurance categories (Paramedical, Dental, Optical, Mental Health) — ready for claim submission without manual interpretation
- Four manual columns close the loop: claim ID, reimbursement amount, total refund, and % reimbursed

**Why it's interesting:** The prompt is deliberately constrained to a fixed `key: value` format, making downstream regex extraction deterministic and robust. The raw AI output is always preserved — if the prompt or a formula needs updating, no re-running the Zap. A clean example of designing for maintainability in a no-code stack, with real domain logic baked into the formula layer.

📁 [View project README](https://github.com/gpn64/healthcare-autoclaims)

---

### 3. 📈 TFSA Stock Screener

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![yfinance](https://img.shields.io/badge/yfinance-6B8E23?style=for-the-badge&logo=yahoo&logoColor=white)
![Quant Finance](https://img.shields.io/badge/Quantitative%20Finance-1A237E?style=for-the-badge&logo=cashapp&logoColor=white)

A Python screener that generates a quarterly TSX rebalancing recommendation for a TFSA — 15 primary positions + 4 backups, all in CAD, combining momentum signals with fundamental quality filters.

**The idea:** Momentum investing — buying assets that have recently outperformed and trimming laggards — is one of the most replicated anomalies in empirical finance. This screener operationalizes it for a self-managed TSX portfolio, with a fundamental scoring gate to avoid chasing deteriorating businesses.

**How the pipeline works:**
- **Coarse filter** — eliminates illiquid names below $5 CAD or $500K daily dollar volume (thresholds calibrated for TSX liquidity)
- **Fundamental scoring** — composite score across ROE, profit margins, revenue growth, P/E, dividend yield, and sector tilt; top 80 pass forward
- **Momentum scoring** — combined 90d × 0.7 + 30d × 0.3 signal applied to the fundamental survivors
- **Portfolio construction** — top 15 equal-weighted as primary positions; next 4 as labeled backups

**Design choices:** TSX-only scope eliminates currency risk and ensures full TFSA eligibility on all positions. The fundamental gate runs before momentum — not after — to avoid selecting names accelerating into deteriorating financials. A historical simulation mode lets you pass any past date to reconstruct what the screener would have recommended on that day.

📁 [View full project README](https://github.com/gpn64/TFSA_Screener-V1)

---

### 4. 📊 Dashboard — Data Quality Monitoring at Scale

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![RLS](https://img.shields.io/badge/Row--Level%20Security-E8423F?style=for-the-badge&logo=microsoftazure&logoColor=white)

A monitoring dashboard built to control data quality inside a cloud-based SaaS platform used by a global organisation across dozens of markets and hundreds of users.

**Context:** In large, distributed organisations, data entered by many teams across many markets quickly becomes inconsistent — missing fields, outdated records, conflicting values. Without visibility into data health, reporting becomes unreliable and operational decisions are made on faulty foundations. This dashboard was built to surface those gaps and drive remediation at scale.

**What it does:**
- Tracks completeness, consistency, and timeliness of key records across markets and business units
- Flags outliers and missing mandatory fields at multiple levels of granularity — from executive summary to individual record drill-through
- Row-level security ensures local teams see only their own data while global teams retain full visibility
- Feeds directly into targeted remediation campaigns, with measurable progress tracked over time

**Impact:** Contributed to achieving 75%+ compliance for priority data categories — a measurable improvement driven by dashboard findings, not manual audits.

---

### 5. 🌐 Dashboard — Multi-Market Deliverable Tracking

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)

An end-to-end pipeline tracking dashboard — from identifying outstanding deliverables to monitoring completion progress across a global network of markets and external vendors.

**Context:** In any organisation operating across dozens of markets with external partners, tracking the status of deliverables through email threads and spreadsheets creates blind spots. Bottlenecks go unnoticed, deadlines slip, and capacity planning is reactive. This dashboard was built to replace that chaos with a single source of truth.

**What it does:**
- Maps outstanding deliverables by type, market, and responsible party
- Tracks progress through defined workflow stages: requested → in progress → under review → completed
- Surfaces aging requests and recurring bottlenecks by partner or deliverable type
- Supports capacity planning for vendors and internal review teams

**Why it matters:** Turns a pipeline that lived in inboxes into a measurable, manageable workflow visible to all stakeholders — from operational teams to leadership.

---

### 6. 🎫 Contractor Request & Ticketing System

![Power Apps](https://img.shields.io/badge/Power%20Apps-742774?style=for-the-badge&logo=powerapps&logoColor=white)
![Power Automate](https://img.shields.io/badge/Power%20Automate-0066FF?style=for-the-badge&logo=powerautomate&logoColor=white)
![SharePoint](https://img.shields.io/badge/SharePoint-0078D4?style=for-the-badge&logo=microsoftsharepoint&logoColor=white)

A structured ticketing system enabling internal teams to formally request documents from third-party contractors — replacing an ad hoc email-based process with an auditable, trackable workflow.

**Context:** Document exchanges with external contractors are often compliance-critical but poorly tracked — requests sent by email, no status visibility, no audit trail. This system was built to bring structure and traceability to a process that previously lived entirely in inboxes.

**What it does:**
- Structured intake form captures: document type, associated project, deadline, and priority level
- Routes requests automatically to the appropriate contractor and internal owner via Power Automate
- Tracks status through a defined workflow: submitted → acknowledged → in progress → delivered → closed
- Generates a complete audit trail with timestamps and version history
- Summary dashboard surfaces SLA compliance and open request aging

**Why it matters:** Turns a compliance-critical process into an auditable, measurable workflow — reducing risk and giving management real visibility into contractor responsiveness.

---

## Project Delivery

Beyond the technical work, I operate as a full-cycle analytics project owner. Whether the project is a Power BI dashboard, a process automation, or a data pipeline, I drive it from first conversation to production:

**Requirements & scoping** — translating ambiguous business problems into precise, deliverable analytics requirements; facilitating workshops with subject matter experts to surface what's actually needed (vs. what's initially asked for); writing functional specs that development and stakeholders can align on.

**Design & development** — data modeling, report architecture, UX decisions, and iterative builds with regular stakeholder checkpoints. I default to building for the end user, not for the analyst.

**Stakeholder management** — managing expectations across technical and non-technical audiences, from data engineers to C-suite sponsors; communicating progress, trade-offs, and delays clearly; keeping cross-functional teams aligned without over-meeting.

**UAT & quality assurance** — structuring user acceptance testing with real users, capturing and triaging feedback, distinguishing scope from defect, and ensuring edge cases are covered before go-live.

**Deployment & adoption** — managing rollout, training, and documentation; setting up governance for ongoing data quality and report maintenance; tracking post-launch adoption to close the loop on whether the solution is actually being used.

This end-to-end ownership — not just the code, but the process around it — is what turns analytics deliverables into decisions.

---

📬 **guillaume.pien@outlook.com** · [LinkedIn](https://www.linkedin.com/in/gpn)
