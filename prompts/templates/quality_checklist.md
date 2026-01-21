# QUALITY CHECKLIST

Use this checklist at each stage of report generation to ensure Gartner-level quality.

---

## CHECKPOINT 1: SOURCE PACK

Run after: Step 1 (Source Pack Builder)

| CATEGORY | MINIMUM | ACTUAL | PASS |
|----------|---------|--------|------|
| Market Size / CAGR Sources | 5+ | ___ | [ ] |
| Adoption / ROI Sources | 5+ | ___ | [ ] |
| Vendor Sources | 5+ | ___ | [ ] |
| Regulatory Sources | 3+ | ___ | [ ] |

**Additional Checks:**

- [ ] Every entry has URL
- [ ] Every entry has publication date
- [ ] No BANNED sources (SEO blogs, listicles, affiliate content)
- [ ] Sources within recency window

**If gaps exist:**

- Document as `[DATA GAP: Need X sources for Y category]`
- Proceed with what IS defensible

---

## CHECKPOINT 2: MARKET SIZE TABLE

Run after: Step 2 (Market Size Normalizer)

- [ ] Missing years remain BLANK (no fabricated numbers)
- [ ] Conflicting scopes are explicitly labeled
- [ ] Each row has URL + date
- [ ] Definition/Scope column filled for each source
- [ ] CSV export block included

**Conflict Analysis:**

- [ ] Scope definition divergences documented
- [ ] Terminology differences noted (e.g., "AI agents" vs "agentic AI")

---

## CHECKPOINT 3: TAM/SAM/SOM

Run after: Step 3 (TAM/SAM/SOM Builder)

- [ ] Table includes: Segment, TAM, SAM, SOM, Method, Inputs (URL/date)
- [ ] Assumptions clearly separated from facts
- [ ] Data gaps listed with "what to source next"
- [ ] No guessing on segment sizing
- [ ] Chart specs provided (pyramid + trend line)

**If not defensible:**

- Output `[DATA GAP]`
- List required inputs to make defensible

---

## CHECKPOINT 4: VENDOR MATRIX

Run after: Step 4 (Vendor Matrix Scorer)

- [ ] Scoring rubric with explicit weights provided
- [ ] No "leader" language without rubric + evidence
- [ ] Every vendor score has supporting URLs
- [ ] Quadrant categories assigned (Leaders/Visionaries/Challengers/Niche)
- [ ] JSON for plotting included

**Evidence Validation:**

- [ ] Each score backed by at least one URL
- [ ] Unverified claims marked as `[UNVERIFIED]`

---

## CHECKPOINT 5: FULL REPORT

Run after: Step 5 (Claude Full Report Draft)

**Structure Check:**

- [ ] Section 1: Market Definition & Scope
- [ ] Section 2: Current Market Size (multi-source table)
- [ ] Section 3: TAM/SAM/SOM (table + assumptions)
- [ ] Section 4: Growth Drivers & Restraints
- [ ] Section 5: Regulatory Timeline table
- [ ] Section 6: Sources & Methodology

**Appendices Check:**

- [ ] Vendor scoring rubric included
- [ ] ROI model inputs checklist included
- [ ] 90-day pilot plan included

**Citation Audit:**

- [ ] No unsourced numbers anywhere
- [ ] Every table row has URL + date
- [ ] Regulatory deadlines have specific dates
- [ ] Self-audit section completed by Claude

**Content Quality:**

- [ ] Clear separation: Facts vs Assumptions vs Implications
- [ ] No scope creep beyond stated parameters
- [ ] Stale data (>12 months) flagged explicitly

---

## CHECKPOINT 6: FREE TROJAN HORSE

Run after: Step 6 (C-Suite Brief Builder)

- [ ] Maximum 3 pages
- [ ] "Boardroom skim" format (no deep tables)
- [ ] Headlines include market size with citations
- [ ] 3 vendor highlights included
- [ ] 2-3 regulatory deadlines included
- [ ] CTA clearly points to $97 brief
- [ ] 3 subject lines generated
- [ ] 5-line email send copy generated

---

## CHECKPOINT 7: $97 RESEARCH BRIEF

Run after: Step 7 ($97 Brief Compiler)

- [ ] 8-12 pages length
- [ ] Enough value to feel "serious"
- [ ] "Withheld for $499" list clearly shows what unlocks:
  - [ ] Full TAM workbook specs
  - [ ] Full vendor weighting details
  - [ ] Full ROI model templates
  - [ ] 90-day pilot plan
- [ ] Final CTA page: "Upgrade to Full Report ($499 deep discount)"

---

## FINAL VALIDATION

Before delivery:

- [ ] All checkpoints passed
- [ ] All `[DATA GAP]` items documented
- [ ] No fabricated data anywhere
- [ ] Citation count verified
- [ ] Spell check completed
- [ ] Format consistency verified

---

<!-- END OF QUALITY CHECKLIST -->
