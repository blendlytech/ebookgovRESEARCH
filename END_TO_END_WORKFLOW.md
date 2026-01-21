# End-to-End Workflow

> **Perplexity Pro + Web-enabled Gemini Gems + Claude Opus 4.5 Thinking**

---

## 🎯 Objective

Generate a **"Gartner-style" market intelligence package** that converts via a tiered pricing model:

| Tier | Asset | Price |
|------|-------|-------|
| 1 | Free C‑Suite Trojan Horse Brief | $0 |
| 2 | Research Brief | $97 |
| 3 | Deep-Discount Full Report | $499 |

---

## 💡 Core Idea

| Tool | Role |
|------|------|
| **Perplexity** | Fastest source discovery + citations |
| **Gemini Gems** | Repeatable transformations (tables, models, briefs) |
| **Claude** | Final analyst narrative + strategic recommendations |

> [!IMPORTANT]
> All tools operate under strict **no-hallucination rules**.

---

## Phase 1: One-Time Setup

> **⏱️ Estimated Time: 60–90 minutes**

### 1.1 Create / Confirm Your Perplexity Space

1. Open **Perplexity** → **Spaces** → **Create Space**
2. Paste your full *"AI Agent Orchestration Market Intelligence Space"* rules file
3. Ensure the rules include:

| Rule Category | Requirement |
|---------------|-------------|
| **Recency** | Oct 2025–Jan 2026 |
| **Authority** | Authority-only sources |
| **Data Integrity** | "No estimate without data" |
| **Format** | Tables + citations requirements |

> [!TIP]
> Spaces exist specifically to keep workflows consistent across many queries.

---

### 1.2 Create the Gemini Gems (Web-enabled)

**Path:** `Gemini → Explore Gems → New Gem → Paste Instructions`

#### Required Gems (Minimum 6)

| Gem | Name | Purpose |
|-----|------|---------|
| **A** | Source Pack Builder (Web) | Aggregate authoritative sources |
| **B** | Market Size & CAGR Normalizer (Web) | Standardize market data |
| **C** | TAM/SAM/SOM Builder (Web) | Evidence-only market sizing |
| **D** | Vendor Matrix Scorer (Web) | Competitive analysis with rubric |
| **E** | C‑Suite Trojan Horse Brief Builder (Web) | Citation-locked executive brief |
| **F** | $97 Research Brief Compiler | Compile from full draft |

> [!CAUTION]
> **Rule for Every Gem:**
> *"Use web grounding + provide sources; if not found, output `[DATA GAP]`."*

---

### 1.3 Set Claude Opus 4.5 (Thinking) "Report Rules"

Use a **persistent rule block** (custom instructions / prompt prefix) that enforces:

- ❌ No invented numbers
- ✅ Inline citations for every datapoint
- ✅ Structured sections + self-audit checklist

---

## Phase 2: Run a New Report

> **🔄 Repeatable Weekly**

### Input Brief *(2 minutes)*

Fill this before starting:

```yaml
Topic: [Your Topic]
Audience: [CIO / CTO / COO / CEO / VC]
Geography: [Global / US / EU]
Use-case Focus: [Enterprise automation / Sales agents / IT/DevOps agents]
Delivery Date: [Month/Year]
Anchor Price: [Optional - e.g., "typical analyst report pricing"]
```

---

## Step 1: Build the Source Pack

> **Tools:** Perplexity Pro *OR* Gem A

### Option 1 *(Recommended)*: Perplexity Pro Inside Your Space

**Fastest for citations**

1. In your Perplexity Space, run:

   ```
   Build a source pack for [TOPIC]. List 40–60 authoritative sources 
   (Oct 2025–Jan 2026 priority) with URL/date and the metric each supports.
   ```

2. **Save output as:** `SOURCE_PACK_v1`

### Option 2: Gemini Gem A (Source Pack Builder Web)

1. Open **Gem A**
2. Prompt: *"Build a Source Pack for [TOPIC], focusing on Oct 2025–Jan 2026."*

#### ✅ Checkpoint *(Must Pass Before Moving On)*

| Category | Minimum Required |
|----------|------------------|
| Market Size / CAGR Sources | 5+ |
| Adoption / ROI Sources | 5+ *(or flagged gaps)* |
| Vendor Sources | 5+ |
| Regulatory Sources | 3+ *(or flagged gaps)* |

> [!WARNING]
> **Every entry must include URL + date.**

---

## Step 2: Normalize Market Size & CAGR

> **Tool:** Gem B

### Process

1. Open **Gem B (Market Size & CAGR Normalizer)**
2. Paste the market size/CAGR excerpts from `SOURCE_PACK_v1`
3. Request outputs:
   - ✅ "Market Size by Source" table
   - ✅ Conflicts (definition/scope differences)
   - ✅ CSV block

#### ✅ Checkpoint

- [ ] Missing years remain **blank** *(no fabricated numbers)*
- [ ] Conflicting scopes are **explicitly labeled**
  - *Example:* "AI orchestration" vs "agent orchestration"

---

## Step 3: Build TAM/SAM/SOM

> **Tool:** Gem C

### Process

1. Open **Gem C (TAM/SAM/SOM Builder)**
2. Provide:
   - Market size table output *(from Step 2)*
   - Your scope: `geo + segment focus + buyer persona`
3. Request:
   - ✅ Table: TAM/SAM/SOM by segment
   - ✅ Assumptions list *(separate from facts)*
   - ✅ Data gaps + required inputs
   - ✅ Chart specs *(pyramid + 2026–2030 line)*

#### ✅ Checkpoint

> [!NOTE]
> If segment sizing is **not defensible**, Gem C outputs:
>
> - `[DATA GAP]`
> - "What to source next" list
>
> **No guessing allowed.**

---

## Step 4: Build the Vendor Matrix

> **Tool:** Gem D

### Process

1. Open **Gem D (Vendor Matrix Scorer)**
2. Prompt with your target list *(start with 8–12 vendors)*
3. Required outputs:
   - ✅ Scoring rubric + weights
   - ✅ Score table with evidence bullets (URLs)
   - ✅ Categories *(Leaders / Visionaries / etc.)*
   - ✅ JSON for plotting

#### ✅ Checkpoint

- [ ] No "leader" language **without rubric + evidence**
- [ ] Every vendor score has **supporting URLs** *(even if imperfect)*

---

## Step 5: Draft the Full Report

> **Tool:** Claude Opus 4.5 (Thinking)

### Input to Claude

Paste the following:

| Asset | Source |
|-------|--------|
| Source Pack | Step 1 |
| Market Size Table | Step 2 |
| TAM/SAM/SOM Outputs | Step 3 |
| Vendor Matrix Outputs | Step 4 |
| Regulatory Links + Dates | Collected throughout |

### Prompt

> *"Write the full report in the required 6 sections + appendices, with citations and a self-audit at the end."*

### Required Output Structure

#### Main Sections

1. Market Definition & Scope
2. Current Market Size *(multi-source table)*
3. TAM/SAM/SOM *(table + assumptions)*
4. Drivers/Restraints *(quantified where possible)*
5. Regulatory Timeline table
6. Sources & Methodology

#### Appendices

- Vendor scoring rubric
- ROI model inputs checklist
- 90-day pilot plan

#### ✅ Checkpoint *(Claude Self-Audit Must Be Included)*

- [ ] *"List any unsourced stats as `[DATA GAP]`"*
- [ ] *"Confirm each table row has a URL/date"*

---

## Step 6: Create the Free Trojan Horse

> **Tool:** Gem E

### Process

1. Open **Gem E (C‑Suite Trojan Horse Brief Builder)**
2. Paste **ONLY**:
   - Headline market numbers *(with citations)*
   - One market-size mini-table
   - 3 vendor highlights
   - 2–3 regulatory deadlines

### Required Outputs

- ✅ 3-page executive brief *(markdown)*
- ✅ 3 subject lines
- ✅ 5-line email send copy

#### ✅ Checkpoint

- [ ] It's **"boardroom skim"** *(no deep tables)*
- [ ] CTA clearly points to the **$97 brief**

---

## Step 7: Create the $97 Research Brief

> **Tool:** Gem F

### Process

1. Open **Gem F ($97 Brief Compiler)**
2. Paste the full Claude report

### Required Outputs

- ✅ 8–12 page paid brief
- ✅ "Withheld for $499" list *(what unlocks)*
- ✅ Final CTA page: *"Upgrade to Full Report ($499 deep discount)"*

#### ✅ Checkpoint

| $97 Brief Includes | $499 Upgrade Unlocks |
|--------------------|----------------------|
| ✅ Enough value to feel "serious" | Full TAM workbook specs |
| | Full vendor weighting details |
| | Full ROI model templates |

---

## Step 8: Assemble the Sales Package

> **Tools:** Perplexity + Claude

### 8.1 Package Deliverables

| File | Description |
|------|-------------|
| `FREE_EXEC_BRIEF.pdf` | Trojan Horse |
| `$97_BRIEF.pdf` | Research Brief |
| `$499_FULL_REPORT.pdf` | Full Report |
| `SOURCES.csv` | *(Optional)* Credibility asset |
| `1-Pager CTA` | *(Optional)* Landing page copy |

### 8.2 Create the Upsell Email Sequence

**Prompt to Claude:**

> *"Write a 3-email sequence: send free brief → offer $97 → upsell $499. Use evidence-led language, not hype."*

---

## Operating Rules

> **Keep Quality "Gartner-Like"**

### 📌 Citation Discipline

> [!CAUTION]
> **No number enters any asset unless it has `URL + date`.**

### 📌 Data Gap Discipline

If a key metric can't be sourced:

1. Label it `[DATA GAP]`
2. Proceed with what **is** defensible

### 📌 Reusability Discipline

- ✅ Keep the Gems **stable**
- ✅ Only vary the **"brief inputs"** per report:
  - Topic
  - Scope
  - Audience

---

## Quick Reference Checklist

> **⏱️ "Run This Now" — 10 minutes**

| Step | Tool | Action |
|------|------|--------|
| 1 | Perplexity Space | Generate Source Pack v1 |
| 2 | Gem B | Normalize market size table |
| 3 | Gem D | Generate vendor matrix + JSON |
| 4 | Claude | Produce full report draft with citations |
| 5 | Gem E | Output 3-page free Trojan Horse PDF text |
| 6 | Gem F | Output $97 brief + $499 upsell CTA |

---

> **🎯 End of Workflow**
