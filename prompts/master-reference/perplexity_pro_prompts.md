# PERPLEXITY PRO RESEARCH PROMPTS

<!-- USE THESE PROMPTS IN: Perplexity Pro with your configured Space -->

---

## MASTER RESEARCH PROMPT

```
ROLE: Deep Market Scout with forensic-accountant skepticism

OBJECTIVE: Build evidence-backed intelligence for [TOPIC]

CONSTRAINTS:
  - Recency window: [START_DATE] to [END_DATE]
  - Authority-only sources (SEC filings, engineering blogs, API docs, academic papers)
  - BANNED: SEO-spam, "Top 10" listicles, affiliate content, LinkedIn thought leadership

DELIVERABLES:
  1. Source Pack (40-60 authoritative sources with URL + date + metric supported)
  2. Market Size Table (multi-source, conflicting scopes labeled)
  3. Voice of Customer quotes (verbatim from Reddit, HN, G2 reviews)
  4. Gap Analysis (unmet needs + what competitors are NOT doing)

FORMAT RULES:
  - Start immediately with data—no introductory paragraphs
  - Every claim backed by specific citation
  - Missing data stated as: "Data point unavailable in public search"
  - Estimations explicitly declared as such
```

---

## SOURCE HIERARCHY

| TIER | SOURCES | TRUST | ACTION |
|------|---------|-------|--------|
| TIER_1 | Engineering blogs, API docs, GitHub repos, SEC filings, Baremetrics | HIGH | Use freely |
| TIER_2 | Reddit (r/SaaS, r/indiehackers), Hacker News, critical G2/Capterra reviews | MEDIUM | Use with attribution |
| TIER_3 | Company press releases, landing pages | SKEPTICAL | Cross-verify required |
| BANNED | SEO blogs, listicles, affiliate content, LinkedIn thought leadership | NEVER | Exclude entirely |

---

## PAIN DISCOVERY PROTOCOL

| STEP | ACTION | SEARCH_TRIGGERS |
|------|--------|-----------------|
| STEP_1 | Pain Discovery: Identify "Hair on Fire" problems | `"I hate X"`, `"Why doesn't Y exist"`, `"sucks"`, `"nightmare"` |
| STEP_2 | Technical Dissection: Tech stack, API limits, integrations | Documentation + job postings |
| STEP_3 | Pricing Physics: Normalize to monthly; expose hidden costs | Setup fees, seat minimums |
| STEP_4 | Negative Space: What competitors are NOT doing | The "Wedge Opportunity" |

---

## PROMPT: SOURCE PACK BUILDER

```
Build a source pack for [TOPIC].

REQUIREMENTS:
  - 40-60 authoritative sources (priority: [RECENCY_WINDOW])
  - Each entry must include: URL, Publication Date, Specific metric supported

CATEGORY_MINIMUMS:
  | Category               | Minimum |
  |------------------------|---------|
  | Market Size / CAGR     | 5+      |
  | Adoption / ROI data    | 5+      |
  | Vendor intelligence    | 5+      |
  | Regulatory / Compliance| 3+      |

IF_UNSATISFIED: Output [DATA GAP: Need X sources for Y category]
```

---

## PROMPT: MARKET SIZE NORMALIZER

```
Analyze these market size sources for [TOPIC]:
[PASTE SOURCE EXCERPTS]

REQUIRED_OUTPUTS:
  1. "Market Size by Source" table with:
     - Source name, 2024-2030 figures, CAGR, Definition/Scope, Notes, URL, Date
  2. Conflict Analysis:
     - Where do scope definitions diverge?
     - Which sources use "AI agents" vs "agent orchestration" vs "agentic AI"?
  3. CSV export block

RULES:
  - Leave missing years BLANK (no fabrication)
  - Explicitly label conflicting scope definitions
```

---

## PROMPT: VENDOR MATRIX BUILDER

```
Build a competitive vendor matrix for [TOPIC].

TARGET_VENDORS: [LIST 8-12 VENDORS]

REQUIRED_OUTPUTS:
  1. Scoring Rubric with explicit weights:
     | Criterion | Weight | Scoring Method |

  2. Score Table:
     | Vendor | Score | Evidence Bullets | URLs |

  3. Quadrant Categories: Leaders / Visionaries / Challengers / Niche Players

  4. JSON for plotting:
     {"players": [{"name": "VendorX", "vision": 8.5, "execution": 7.2}]}

RULES:
  - No "leader" designation without rubric + evidence
  - Every score must cite supporting URL (even if imperfect)
```

---

## PROMPT: VOICE OF CUSTOMER

```
Find authentic user sentiment for [TOPIC].

SEARCH_LOCATIONS:
  - Reddit: r/SaaS, r/indiehackers, r/startups, r/[INDUSTRY]
  - Hacker News discussions
  - G2/Capterra reviews (critical reviews prioritized)
  - Product Hunt comments

REQUIRED_OUTPUTS:
  1. Verbatim quotes (with source URL)
  2. Pain points table:
     | Pain | Frequency | Source URLs |
  3. Feature requests table:
     | Request | Frequency | Source URLs |

FORMAT: Use `site:reddit.com` or Reddit Focus mode for best results.
```

---

## PROMPT: REGULATORY SCANNER

```
Scan regulatory landscape for [TOPIC] in [GEOGRAPHY].

REQUIRED_OUTPUTS:
  1. Regulatory Timeline table:
     | Regulation | Jurisdiction | Status | Effective Date | Impact | Required Controls |

  2. Compliance risk summary

  3. Upcoming deadlines (next 24 months)

SOURCES TO PRIORITIZE:
  - Government regulatory sites (.gov)
  - Industry association announcements
  - Legal/compliance firm publications
```

---

## OPTIMIZATION TIPS

| ENHANCEMENT | PROMPT_ADDITION |
|-------------|-----------------|
| Real-time citations | `"Cite 5+ recent sources per section."` |
| Reddit sentiment | Use Reddit Focus mode or `site:reddit.com` |
| Academic validation | Use Academic Focus mode |
| Deep traversal | Chain queries: `"CRM for Plumbers"` → `"Plumber software complaints"` → `"ServiceTitan pricing"` |

---

<!-- END OF PERPLEXITY PRO PROMPTS -->
