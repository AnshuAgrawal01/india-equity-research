---
description: Analyze quarterly earnings and create an earnings update report for Indian listed companies
argument-hint: "[company name or NSE/BSE ticker] [quarter, e.g. Q3 FY25]"
---

# Earnings Analysis Command

Create a professional equity research earnings update report analyzing quarterly results for Indian listed companies (NSE/BSE).

## Workflow

### Step 1: Gather Information

Parse the input for:
- Company name or NSE/BSE ticker
- Quarter (e.g., Q3 FY25, Q2 FY26)

If not provided, ask:
- "What company's earnings would you like to analyze?"
- "Which quarter? (e.g., Q3 FY25)"

### Step 2: Verify Timeliness

**CRITICAL**: Before proceeding, verify you have the latest data:
1. Search for "[Company] latest quarterly results [current year]"
2. Verify the results are within the last 3 months
3. Confirm con-call transcript date matches results date

If data is stale, inform the user and search for the latest.

### Step 3: Load Earnings Analysis Skill

Use `skill: "earnings-analysis"` to create the report:

1. **Data Collection** (search for latest):
   - Quarterly results (BSE/NSE filing under LODR Regulation 33)
   - Press release / investor presentation
   - Con-call transcript (company IR site / Trendlyne)
   - Investor presentation/supplemental materials
   - Consensus estimates (Bloomberg/Screener.in/Trendlyne)

2. **Beat/Miss Analysis**:
   - Revenue vs consensus: Beat/Miss by ₹X Cr or X%
   - EPS vs consensus: Beat/Miss by ₹X or X%
   - Key segment performance vs expectations
   - Explain WHY results differed

3. **Key Metrics Analysis**:
   - Revenue breakdown by segment/geography
   - Margin trends (gross, EBITDA, PAT)
   - Guidance: raised/maintained/lowered
   - Updated forward estimates

4. **Generate Charts** (8-12):
   - Quarterly revenue progression
   - Quarterly EPS progression
   - Margin trends
   - Revenue by segment
   - Beat/miss summary
   - Estimate revisions
   - Valuation charts

5. **Create Report** (8-12 pages):
   - Page 1: Summary with rating and target price
   - Pages 2-3: Detailed results analysis
   - Pages 4-5: Key metrics & guidance
   - Pages 6-7: Updated investment thesis
   - Pages 8-10: Valuation & estimates
   - Sources section with clickable hyperlinks

### Step 4: Deliver Output

Provide:
1. **DOCX report** - 8-12 page earnings update
2. **Summary** highlighting:
   - Beat/miss on key metrics
   - Guidance changes
   - Thesis impact (positive/negative/neutral)

## Report Structure Reference

```
PAGE 1: EARNINGS SUMMARY
┌─────────────────────────────────────────────────────────────────┐
│ [Company] Q3 FY25 Earnings Update                               │
│ Rating: BUY | Target Price: ₹X,XXX (from ₹X,XXX)               │
├─────────────────────────────────────────────────────────────────┤
│ KEY TAKEAWAYS                                                   │
│ • Revenue beat by X% on strong [segment] performance            │
│ • EPS beat by ₹X.XX driven by margin expansion                  │
│ • FY guidance raised to ₹X,XXX-X,XXX Cr (from ₹X,XXX Cr)      │
│ • Thesis intact; maintain BUY rating                            │
├─────────────────────────────────────────────────────────────────┤
│ RESULTS SNAPSHOT                                                │
│ ┌─────────────┬──────────┬──────────┬──────────┐               │
│ │ Metric      │ Actual   │ Consensus│ Beat/Miss│               │
│ │ Revenue     │ ₹X,XXX Cr│ ₹X,XXX Cr│ +X.X%   │               │
│ │ EPS         │ ₹XX.XX   │ ₹XX.XX   │ +₹X.XX  │               │
│ │ EBITDA Mrgn │ XX.X%    │ XX.X%    │ +XXbps   │               │
│ └─────────────┴──────────┴──────────┴──────────┘               │
└─────────────────────────────────────────────────────────────────┘

PAGES 2-3: DETAILED RESULTS
- Segment-by-segment analysis
- Geographic breakdown (domestic vs exports)
- Key drivers of beat/miss

PAGES 4-5: METRICS & GUIDANCE
- Margin analysis (EBITDA, PAT)
- Full-year guidance comparison
- Updated quarterly estimates

PAGES 6-7: THESIS UPDATE
- What's changed
- Risks and catalysts
- Investment recommendation

PAGES 8-10: VALUATION
- Updated DCF/comps if material
- Target price justification
- Scenario analysis

SOURCES SECTION (with clickable hyperlinks):
- Quarterly Results: [BSE/NSE filing hyperlink]
- Press Release: [company IR hyperlink]
- Con-call Transcript: [Trendlyne / company IR hyperlink]
- Consensus estimates: Bloomberg / Screener.in as of [date]
```

## Quality Checklist

Before delivery:
- [ ] Earnings data is from latest quarter (not stale)
- [ ] Beat/miss quantified with specific numbers (in ₹ Cr)
- [ ] All charts embedded (8-12 total)
- [ ] Sources section with clickable hyperlinks
- [ ] Every figure/table has source citation
- [ ] Guidance changes clearly documented
- [ ] Rating and target price stated upfront
- [ ] 8-12 pages, 3,000-5,000 words
