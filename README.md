# Kidswear Market Analysis — E-commerce Market Entry

A data-driven market entry analysis for a direct-to-consumer kidswear brand targeting the UK market, with secondary analysis of US expansion potential.

The analysis identifies a structural gap in the UK kidswear market: established brands largely stop at age 10, while the 11–19 segment is underserved by brands offering genuine quality and aesthetic differentiation at an accessible price point. All data used is publicly available. No proprietary or commercially sensitive data is included.

---

## Research Questions

1. How large is the UK children's and teen apparel market, and what is the e-commerce growth trajectory?
2. How are direct competitors priced, and what does the competitive landscape look like across product categories?
3. What does consumer search behaviour reveal about demand trends, seasonality, and geographic opportunity?
4. How do competitor brands perform on social media relative to their size, and what engagement patterns exist?
5. What does a realistic financial model look like for a bootstrapped e-commerce brand entering this space?

---

## Project Structure

```
kidswear-market-analysis/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── 01_competitor_analysis/
│   ├── competitor_pricing.ipynb
│   └── data/
│
├── 02_search_trends/
│   ├── google_trends.ipynb
│   └── data/
│
├── 03_social_analysis/
│   ├── social_metrics.ipynb
│   ├── key_findings.md
│   └── data/
│
├── 04_strategic_context/
│   ├── strategic_models_competitive_context.ipynb
│   └── data/
│
├── 05_market_opportunity/
│   ├── market_gap_analysis.ipynb
│   ├── market_opportunity_demographics.ipynb
│   └── data/
│
└── 06_financial_modelling/
    ├── revenue_projections.ipynb
    └── data/
```

---

## Analytical Flow

**Raw data → Strategic interpretation → Opportunity framing → Quantification**

| # | Notebook | Purpose |
|---|----------|---------|
| 01 | Competitor Pricing Analysis | Pricing points and brand positioning map across UK and US markets |
| 02 | Google Trends Analysis | Demand signals, seasonality, and geographic opportunity via pytrends API |
| 03 | Social Media Analysis | Instagram/TikTok metrics, engagement benchmarking, content analysis |
| 04 | Strategic Context | Competitive synthesis, business model comparison, positioning map |
| 05 | Market Opportunity | Market sizing, demographic analysis, gap quantification |
| 06 | Financial Modelling | Revenue scenarios, unit economics, break-even analysis |

---

## Key Findings

### Competitor Pricing
- UK mass market ceiling ~£28 (M&S, Next, Primark)
- UK premium brands stop at age 10 — no established brand serves the 11–19 segment at a premium price point
- US equivalent (Katie J NYC) pricing at £62–75 GBP — validates that demand exists at this price point

### Google Trends
- November peak: 5x uplift vs summer trough — Christmas gifting dominates demand
- `girls pyjamas` tracks almost identically to `kids pyjamas` — gender-specific search as common as generic
- No premium brand appears in any top related queries — mass market owns search entirely
- `luxury pyjamas` near-zero — consumers do not search "luxury" to find premium products
- White Fox explosive growth from 2023 — social-first brands can scale fast in this category
- `matching kids pjs` rising — family gifting behaviour signal

### Social Media Analysis
- Mass-market brands dominate scale: Next (3.4M IG), White Fox (4.2M combined), M&S (2.4M IG) hold 60–65% of total audience; most UK premium brands stay sub-300K IG with negligible TikTok presence
- Engagement inverts with scale: Pink Palm Puff leads at ~2.37%, followed by Roller Rabbit (~1.16%); mass-market brands fall below 0.1–0.2%
- Carousel dominates content: 8–12 of last 12 posts for most premium brands; static images largely obsolete
- TikTok underutilised by UK brands: most sub-10K–70K followers; only Pink Palm Puff (~967K TikTok) and White Fox (~1.5M TikTok) show meaningful presence
- Pink Palm Puff is the clear benchmark: TikTok-dominant (59% of 1.64M combined followers), top engagement (2.37%), elite follower-to-following ratio (~12,291:1) — the model for authentic, founder-led premium teen content

### Market Opportunity
- Stable 11–19 demographic base provides dependable demand volume
- Full sizing and quantification in `05_market_opportunity`

---

## Notebook Detail

### 01 — Competitor Pricing Analysis
Scrapes publicly available product pricing from comparable brands across UK and US markets. Maps the competitive landscape and identifies pricing white space in the 11–19 segment.

**Skills demonstrated:** web scraping, BeautifulSoup, pandas, matplotlib, data cleaning

### 02 — Google Trends Analysis
Uses the pytrends API to analyse search volume trends for relevant terms (`kids pyjamas`, `girls pyjamas`, `kids pjs`, `kids pajamas`) across UK and US markets. Identifies seasonality patterns, year-on-year demand growth, and geographic opportunity.

**Skills demonstrated:** API integration, time series analysis, pytrends, seaborn heatmap

### 03 — Social Media Analysis
Collects public social metrics (follower count, engagement rate, posting frequency) for comparable brands across Instagram and TikTok. Benchmarks brand performance and identifies which brands have the strongest community relative to their size.

**Skills demonstrated:** data collection, pandas, comparative analysis, seaborn visualisation

### 04 — Strategic Context
Maps business and social models across adjacent brands. Synthesises competitive dynamics and produces a positioning map of the market landscape.

**Skills demonstrated:** competitive analysis, strategic frameworks, data visualisation

### 05 — Market Opportunity
Quantifies the addressable market using UK demographic data. Frames the market gap with supporting evidence from notebooks 02–04.

**Skills demonstrated:** market sizing (TAM/SAM/SOM), demographic analysis, opportunity framing

### 06 — Financial Modelling
Builds a three-scenario revenue projection model (conservative, base, optimistic) for a bootstrapped e-commerce launch. Includes break-even analysis, margin sensitivity, and CAC assumptions based on industry benchmarks.

**Skills demonstrated:** financial modelling in Python, scenario analysis, sensitivity tables, plotly

---

## Methodology & Data Sources

| Component | Method | Data Source |
|-----------|--------|-------------|
| Competitor pricing | Web scraping (BeautifulSoup) | Brand websites (public product pages) |
| Search trends | API via pytrends | Google Trends |
| Social metrics | Manual collection + Countik | Instagram, TikTok (public accounts) |
| Financial modelling | Scenario analysis | Industry benchmarks, Companies House filings |

---

## Tech Stack

- Python 3.11
- Jupyter Notebooks
- pandas, numpy
- matplotlib, seaborn, plotly
- BeautifulSoup4, requests
- pytrends
- scipy

---

## Setup & Installation

```bash
# Clone the repository
git clone https://github.com/rosesparrow/kidswear-market-analysis.git
cd kidswear-market-analysis

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

---

## Limitations & Caveats

- Social media metrics are point-in-time snapshots collected manually; engagement rates will shift over time
- Web scraping reflects pricing at time of collection; fashion pricing changes seasonally
- Financial projections are illustrative scenario models, not forecasts; all assumptions are documented within the notebook
- Google Trends data is relative (indexed 0–100) rather than absolute search volume
- Social engagement metrics are directional proxies; correlation with commercial outcomes is not established

---

*Independent market analysis project. Conducted using publicly available data sources only.*

*Project status: In progress — last updated March 2026*
