# Guillaume Pien — Data & Analytics Portfolio

**PharmD · Data Analytics · Business Intelligence · Automation**  
📍 Greater Ottawa Metropolitan Area · [LinkedIn](https://www.linkedin.com/in/gpn)

---

## About

I'm a pharmacist-turned-data professional with 10+ years in the pharmaceutical industry. My edge is at the intersection of deep domain expertise and technical analytics: I understand the regulatory, quality, and manufacturing context behind the data — which means I ask better questions, build more relevant models, and deliver insights that actually change decisions.

My toolbox spans **Snowflake, Power BI** (PL-300 certified), **SQL, Python, and automation platforms**. I'm particularly drawn to projects that reduce manual toil, surface hidden patterns in messy operational data, and give leadership teams a clearer picture of what's actually happening.

This portfolio showcases personal and professional projects that reflect how I think about data problems.

---

## Projects

### 1. 🏥 GenAI Automation — Health Claim Database from Receipts

**`Gmail · Zapier · Airtable AI · GPT-4 · Regex`**

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

**`Power BI · SQL · Snowflake · RLS`**

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

**`Power BI · SQL · Regulatory Affairs domain`**

An end-to-end tracking dashboard for pharmaceutical labeling translation workflows — from identifying translation needs to monitoring completion across global markets.

**Context:** Labeling documents (SmPC, PIL, packaging) must be translated and approved for every market where a product is sold. With hundreds of products and dozens of languages, translation bottlenecks can delay launches and trigger compliance issues. Visibility into this pipeline is typically poor.

**What it does:**
- Maps outstanding translation needs by product, document type, and target market
- Tracks translation progress through workflow stages: requested → in translation → under review → approved
- Surfaces aging requests and identifies recurring bottlenecks by language pair or document type
- Supports capacity planning for translation vendors and internal review teams

**Why it matters:** Transforms a chaotic email-and-spreadsheet process into a single source of truth for regulatory operations leadership.

---

### 4. 📈 Momentum-Based Stock Picker — TFSA Portfolio

**`Python · Pandas · yfinance · Quantitative Finance`**

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

## Skills & Tools

| Category | Tools |
|----------|-------|
| **BI & Visualization** | Power BI (PL-300 certified), Airtable |
| **Data Engineering** | Snowflake, SQL, dbt (basic) |
| **Programming** | Python (Pandas, NumPy, yfinance), regex |
| **Automation** | Zapier, Power Automate, Airtable AI |
| **AI/NLP** | Prompt engineering, GPT-4 via API, NLP (certified) |
| **Domain** | Pharmaceutical regulatory affairs, CMC, quality, supply chain |

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

📬 **guillaumepien@gmail.com** · [LinkedIn](https://www.linkedin.com/in/gpn)
