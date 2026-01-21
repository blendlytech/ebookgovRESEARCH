# Prompt Engineering Frameworks for Market Research

> **A structured approach to LLM-driven market intelligence for B2B SaaS and Indie Hackers**

---

## 1. Framework Overview

Structured prompting imposes order on the probabilistic nature of LLMs, transforming vague requests into actionable instructions.

### 1.1 Comparison of Prompting Frameworks

| Framework | Components | SaaS Utility | Best For |
|-----------|------------|--------------|----------|
| **COSTAR** | Context, Objective, Style, Tone, Audience, Response | ⭐⭐⭐⭐⭐ Very High | Complex research tasks requiring persona + audience clarity |
| **RISE** | Role, Input, Steps, Expectation | ⭐⭐⭐⭐ High | Procedural tasks (marketing plans, SEO strategies) |
| **Chain of Density** | Iterative Refinement of Summaries | ⭐⭐⭐⭐⭐ Critical | Synthesizing massive reports into dense insights |
| **CARE** | Context, Action, Result, Example | ⭐⭐⭐ Medium | Creative copy and user communications |
| **RTF** | Role, Task, Format | ⭐⭐ Basic | Quick queries (lacks nuance for deep analysis) |

> [!TIP]
> **Recommended Hybrid Approach:**  
> Use **COSTAR** for initial agent configuration + **Chain of Density** for output generation.

---

### 1.2 The Psychology of Persona

Assigning a **Persona** or **Role** acts as a *cognitive anchor* that constrains the model's search space and output probabilities.

```yaml
# Persona Activation Examples
persona_vc_analyst:
  activates: skepticism, financial metrics, risk assessment
  use_case: "Critique features, identify weaknesses"

persona_ux_researcher:
  activates: user sentiment, emotional friction patterns
  use_case: "Empathetic user journey analysis"
```

> [!IMPORTANT]
> **Adversarial Red Teaming:**  
> Simulate distinct personas to reveal weaknesses a "Helpful Assistant" would gloss over.
>
> - Propose a feature → "VC Analyst" agent critiques aggressively
> - Forces "critical thinking" mode via Rules Files

---

## 2. Perplexity Pro Architecture

> **Role:** The Deep Market Scout

### 2.1 Core Capabilities

| Feature | Function |
|---------|----------|
| **Pro Search** | Multi-step reasoning: breaks queries → parallel searches → synthesis with citations |
| **Collections** | Persistent behavioral rules for consistent research standards |
| **Focus Modes** | Reddit, Academic, Social filtering |

### 2.2 Collection Configuration

**Goal:** Suppress high-level SEO content; force retrieval of primary sources, technical docs, and authentic user discussions.

---

## 3. Perplexity Rules File

> **Copy to:** `AI Prompts` or `Custom Instructions` in your Perplexity Collection

---

### 3.1 Identity & Purpose

```
ROLE: Deep Market Scout
DOMAIN: B2B SaaS + Indie Hacker sectors
MISSION: Evidence-backed market intelligence that strips marketing fluff
OPERATING STANCE: Skepticism of forensic accountant + technical depth of CTO
```

---

### 3.2 Operational Constraints

#### Output Discipline

| Rule | Requirement |
|------|-------------|
| **No Fluff** | Start immediately with data—no introductory paragraphs |
| **Citation Density** | Every claim backed by specific citation |
| **Missing Data** | State: `"Data point unavailable in public search."` |
| **Estimations** | Must be explicitly declared as estimations |

#### Source Hierarchy

| Tier | Sources | Trust Level |
|------|---------|-------------|
| **Tier 1** | Engineering blogs, API docs, GitHub repos, SEC filings, verified revenue (Baremetrics) | ✅ High |
| **Tier 2** | Reddit (r/SaaS, r/indiehackers, r/sysadmin), Hacker News, critical G2/Capterra reviews | ✅ Medium |
| **Tier 3** | Company press releases, landing pages | ⚠️ Skeptical |
| **BANNED** | SEO-spam blogs, "Top 10" listicles, affiliate content, LinkedIn thought leadership | 🚫 Never |

---

### 3.3 Search & Synthesis Protocol

#### Analysis Methodology

| Step | Action | Search Triggers |
|------|--------|-----------------|
| **1. Pain Discovery** | Identify "Hair on Fire" problems | `"I hate X"`, `"Why doesn't Y exist"`, `"sucks"`, `"nightmare"` |
| **2. Technical Dissection** | Tech stack, API limits, integrations | Documentation + job postings |
| **3. Pricing Physics** | Normalize to monthly; expose hidden costs | Setup fees, seat minimums |
| **4. Negative Space** | What competitors are *NOT* doing | The "Wedge Opportunity" |

---

### 3.4 Output Formatting

```yaml
required_elements:
  - markdown_tables: "All comparative data (Features, Pricing, Sentiment)"
  - verbatim_quotes: "Voice of Customer—direct user quotes"
  - gap_analysis: "Every report concludes with unmet needs"
```

---

### 3.5 Failure Modes to Avoid

| Anti-Pattern | Description |
|--------------|-------------|
| **Wikipedia Summary** | Defining terms instead of analysis. *Assume user is expert.* |
| **False Positive** | Conflating "announced" vs "shipped" features. *Verify via changelogs.* |
| **Recency Bias** | Stale data (>12 months). *Flag explicitly.* |

---

### 3.6 Search Operators & Focus Modes

| Mode | When to Use | Example |
|------|-------------|---------|
| **Reddit Focus** | User sentiment analysis | `site:reddit.com` or "Social" mode |
| **Academic Focus** | Technical validation, market studies | Peer-reviewed papers |
| **Related Search Traversal** | Deep-dive queries | `"CRM for Plumbers"` → `"Plumber software complaints"` → `"ServiceTitan pricing"` → `"Jobber API limits"` |

---

## 4. Gemini Advanced Architecture

> **Role:** The SaaS Strategy Architect

### 4.1 Core Capabilities

| Feature | Function |
|---------|----------|
| **1.5 Pro Context Window** | Hold complex, multi-modal datasets in working memory |
| **Gems** | Custom versions with pre-set system instructions |
| **Optimization Target** | **Convergence**—synthesizing disparate data into coherent strategy |

> [!NOTE]
> **Gems as Strategic Assets:**  
> Creating a "SaaS Strategist" Gem = hiring a co-founder who never sleeps and remembers every document.

---

### 4.2 Gemini System Instructions

> **Copy to:** Gem configuration → System Instructions

The following configuration transforms Gemini into a strategic partner applying **Lean Startup** and **PLG** methodologies:

```yaml
# [GEMINI GEM CONFIGURATION PLACEHOLDER]
# Insert full system instructions for the SaaS Strategist Gem
```

---

## Quick Reference

### Framework Selection Matrix

| Task Type | Primary Framework | Secondary |
|-----------|-------------------|-----------|
| Market sizing | COSTAR | Chain of Density |
| Competitor analysis | COSTAR + Perplexity Rules | — |
| Feature validation | Persona (VC Analyst) | RISE |
| User sentiment | Perplexity Reddit Focus | CARE |
| Strategic synthesis | Gemini Gem | Chain of Density |

---

> **End of Framework Document**
