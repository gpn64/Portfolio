# Guillaume Pien — Data & Analytics Portfolio

**PharmD · Data Analytics · Business Intelligence · Automation**  
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
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![OpenAI](https://img.shields.io/badge/GPT--4-412991?style=for-the-badge&logo=openai&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)

---

## About

I'm a pharmacist and data professional with 10+ years in the pharmaceutical industry. My edge is at the intersection of deep domain expertise and technical analytics: I understand the regulatory, quality, and manufacturing context behind the data — which means I ask the right questions, build relevant models, and deliver insights that actually change decisions.

My toolbox spans **Snowflake, Power BI** (PL-300 certified), **SQL, Python, and automation platforms**. I'm particularly drawn to projects that reduce manual toil, surface hidden patterns in messy operational data, and give leadership teams a clearer picture of what's actually happening.

This portfolio showcases personal and professional projects that reflect how I think about data problems.


---

## Projects

### 1. 🏥 GenAI Automation — Health Claim Database from Receipts

![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)
![Zapier](https://img.shields.io/badge/Zapier-FF4A00?style=for-the-badge&logo=zapier&logoColor=white)
![Airtable](https://img.shields.io/badge/Airtable-18BFFF?style=for-the-badge&logo=airtable&logoColor=white)
![OpenAI](https://img.shields.io/badge/GPT--4-412991?style=for-the-badge&logo=openai&logoColor=white)
![Regex](https://img.shields.io/badge/Regex-4A4A4A?style=for-the-badge&logo=gnubash&logoColor=white)

A fully automated pipeline that ingests healthcare invoices from Gmail, extracts structured fields using an LLM prompt, and builds a live reimbursement tracking database — with zero manual data entry on the intake side.

**What it does:**
- Gmail label-based filter routes provider emails to a Zapier automation
- Zapier captures email links and PDF attachments, creates Airtable records
- An Airtable AI field runs a structured GPT-4 prompt against each invoice, extracting: clinic name, patient name, care type, appointment date, practitioner, duration, and amount billed
- Regex formula columns parse the AI output into individual structured fields
- Two manual columns close the loop: insurer reimbursement amount and claim reference ID

**Why it's interesting:** The prompt is deliberately constrained to produce a fixed-label output format, which makes downstream regex extraction deterministic. The raw AI output is always preserved, so formulas can be updated without re-running the automation. A clean example of designing for maintainability in a no-code stack.

📁 [View project README](./genai-health-claims/README.md)

---

### 2. 📊 Dashboard — Regulatory SaaS Data Quality Control

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![RLS](https://img.shields.io/badge/Row--Level%20Security-E8423F?style=for-the-badge&logo=microsoftazure&logoColor=white)

A monitoring dashboard built to control data quality inside a cloud-based Regulatory Information Management System (RIMS) used across a global pharmaceutical company.

**Context:** Regulatory data in large pharma is notoriously fragmented — product records, submission timelines, document statuses, and health authority interactions all live in different modules and get updated by distributed teams across dozens of markets. Quality gaps directly affect compliance reporting and regulatory strategy.

**What it does:**
- Tracks completeness, consistency, and timeliness of key regulatory records across global markets
- Flags outliers and missing mandatory fields at the product, market, and submission level
- Provides drill-through capability from executive summary to individual record
- Row-level security ensures market teams see only their own data while global teams have full visibility

**Impact:** Contributed to achieving 75%+ compliance for priority document categories through targeted data remediation campaigns driven by dashboard findings.

---

### 3. 🌐 Dashboard — Labeling Translation Request & Tracking

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![Pharma](https://img.shields.io/badge/Regulatory%20Affairs-00897B?style=for-the-badge&logo=bookstack&logoColor=white)

An end-to-end tracking dashboard for pharmaceutical labeling translation workflows — from identifying translation needs to monitoring completion across global markets.

**Context:** Labeling documents (SmPC, PIL, packaging) must be translated and approved for every market where a product is sold. With hundreds of products and dozens of languages, translation bottlenecks can delay launches and trigger compliance issues. Visibility into this pipeline is typically poor.

**What it does:**
- Maps outstanding translation needs by product, document type, and target market
- Tracks translation progress through workflow stages: requested → in translation → under review → approved
- Surfaces aging requests and identifies recurring bottlenecks by language pair or document type
- Supports capacity planning for translation vendors and internal review teams

**Why it matters:** Transforms a chaotic email-and-spreadsheet process into a single source of truth for regulatory operations leadership.

---

### 4. 🏅 True Olympic Powerhouse — Sanofi-Wide Analytics Competition

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-4A4A4A?style=for-the-badge&logo=microsoftexcel&logoColor=white)
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

![Introduction](./screenshots/TOP0.PNG)

📁 [View full project README & report](https://github.com/gpn64/TOP-Dashboard-PowerBI/tree/main)

---

### 5. 🎫 Ancillary Document Request & Ticketing System

![Power Apps](https://img.shields.io/badge/Power%20Apps-742774?style=for-the-badge&logo=powerapps&logoColor=white)
![Power Automate](https://img.shields.io/badge/Power%20Automate-0066FF?style=for-the-badge&logo=powerautomate&logoColor=white)
![SharePoint](https://img.shields.io/badge/SharePoint-0078D4?style=for-the-badge&logo=microsoftsharepoint&logoColor=white)
![Pharma](https://img.shields.io/badge/Regulatory%20Affairs-00897B?style=for-the-badge&logo=bookstack&logoColor=white)

A structured ticketing system enabling internal teams to formally request ancillary documents from a third-party contractor, as required under pharmaceutical regulatory frameworks.

**Context:** Certain regulatory activities — particularly those involving contract manufacturing organizations (CMOs) or contract research organizations (CROs) — require formally documented exchanges of ancillary documents (e.g., certificates, specifications, batch records). Without a structured process, these requests were tracked via email threads, creating audit trail gaps and compliance risk.

**What it does:**
- Provides a structured intake form for submitting document requests, capturing: document type, associated product/submission, regulatory deadline, and priority level
- Routes requests automatically to the appropriate contractor contact and internal owner via Power Automate
- Tracks request status through a defined workflow: submitted → acknowledged → in progress → delivered → closed
- Generates a complete audit trail of all exchanges, with timestamps and version history, meeting regulatory traceability requirements
- Surfaces SLA compliance and open request aging in a summary dashboard

**Why it matters:** Turns a compliance-critical process that lived in inboxes into an auditable, measurable, and manageable workflow — directly reducing regulatory risk and improving contractor relationship governance.

---

### 6. 📈 Momentum-Based Stock Picker — TFSA Portfolio

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![yfinance](https://img.shields.io/badge/yfinance-6B8E23?style=for-the-badge&logo=yahoo&logoColor=white)
![Quant Finance](https://img.shields.io/badge/Quantitative%20Finance-1A237E?style=for-the-badge&logo=cashapp&logoColor=white)

A systematic stock selection tool built for a Canadian Tax-Free Savings Account (TFSA), using price momentum as the core signal.

**The idea:** Momentum investing — buying assets that have outperformed recently and selling laggards — is one of the most robust and replicated anomalies in empirical finance. This project operationalizes it for a self-managed retail portfolio with Canadian tax constraints in mind.

**What it does:**
- Pulls historical price data for a defined stock universe via `yfinance`
- Calculates momentum scores using trailing returns over multiple lookback windows (e.g., 12-1 month, adjustable)
- Ranks and filters candidates based on momentum rank, with optional volatility adjustment
- Outputs a ranked watchlist and suggested rebalancing actions based on current holdings
- Designed around TFSA rules: contribution room tracking, no foreign income tax implications for eligible holdings

**Design choices:** Lookback windows and universe filters are configurable. The tool is intentionally simple — no overfitting to historical data, no black-box ML. The signal is transparent and the logic is auditable.

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

## Background

| | |
|---|---|
| **PharmD** | Université de Caen Basse-Normandie |
| **MEng — Industrial Management & Supply Chain** | École Centrale Paris |
| **MBA** | IAE Caen |
| **MS — Drug Design & Medicinal Chemistry** | Université de Caen Basse-Normandie |

**Certifications:** PL-300 Power BI Data Analyst · NLP (Natural Language Processing) · CPIM Basics of Supply Chain · Data Analyst Professional Certificate

---

## What I'm Looking For

Senior IC or team lead roles in **data analytics and business intelligence**, ideally in regulated industries (pharma, biotech, health) or environments where domain complexity adds real value to the analytics function. I'm most effective when I can own problems end-to-end — from business question to deployed solution — and work closely with cross-functional stakeholders who care about getting decisions right.

---

📬 **guillaume.pien@outlook.com** · [LinkedIn](https://www.linkedin.com/in/gpn)
