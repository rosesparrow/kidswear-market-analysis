# Premium Kidswear & Teen Apparel — E-commerce Market Entry Analysis

## Overview

This project presents a data-driven market entry analysis for a hypothetical direct-to-consumer premium loungewear brand targeting the 11–19 age demographic in the UK, with secondary analysis of US expansion potential.

The analysis identifies a structural gap in the UK premium kidswear market: established luxury loungewear brands are primarily adult-focused, while the 11–19 segment is underserved by brands offering genuine quality and aesthetic differentiation at a mid-luxury price point.

All data used is publicly available. No proprietary or commercially sensitive data is included.

---

## Research Questions

1. How large is the UK premium children's and teen apparel market, and what is the e-commerce growth trajectory?
2. How are direct competitors priced, and what does the competitive landscape look like across product categories?
3. What does consumer search behaviour reveal about demand trends, seasonality, and geographic opportunity?
4. How do competitor brands perform on social media relative to their size, and what engagement patterns exist?
5. What does a realistic financial model look like for a bootstrapped e-commerce brand entering this space?

---

## Project Structure

```

premium-kidswear-market-analysis/
│
├── README.md                  # Update to describe the full flow + notebook purposes
├── requirements.txt
├── .gitignore
│
├── 01_competitor_analysis/    # (pricing, positioning map – still to do)
│ ├── competitor_pricing.ipynb
│ └── data/
│
├── 02_search_trends/          # ← done, key findings below
│ ├── google_trends.ipynb
│ └── data/
│
├── 03_social_analysis/        # ← Now complete – push with key findings export
│ ├── social_metrics.ipynb
│ ├── key_findings.md          # ← Or .ipynb with markdown export of the printout
│ └── data/                    # social_media_data_collection_v7.xlsx + charts
│
**├── 04_strategic_context/**  # ← New folder: models, adjacent brands, gap analysis**
**│ ├── strategic_models_competitive_context.ipynb**  # ← Main notebook for models table, adjacents, positioning map, gap statement**
**│ └── data/**                # ← Any additional CSVs, screenshots, or notes (brand websites captures)**
**│**
**├── 05_market_opportunity/** # ← new folder to separate pure gap/opportunity framing**
**│ ├── market_gap_analysis.ipynb**  # ← Short notebook with the one-sentence gap + supporting evidence from 03 & 04**
**│ └── data/**
│
├── 06_financial_modelling/    # ← Renumbered to reflect new flow (was 04)
│ ├── revenue_projections.ipynb
│ └── data/
│
└── reports/
    └── summary_visualisations/ # Key charts from 03 + any new from 04 (e.g., positioning map)

```

---

## Methodology & Data Sources

| Component | Method | Data Source |
|---|---|---|
| Competitor pricing | Web scraping (BeautifulSoup) | Brand websites (public product pages) |
| Search trends | API via pytrends | Google Trends |
| Social metrics | Manual collection + Countik| Instagram, TikTok (public accounts) |
| Financial modelling | Scenario analysis | Industry benchmarks, Companies House filings |

---

## Key Findings

*This section will be updated as each analytical component is completed.*

From competitor pricing:

- UK mass market ceiling ~£28 (M&S, Next, Primark)
- UK premium floor £89 (D&D), stops at age 10
- ~£60 gap with no UK brand serving 11-19 at premium price point
- US equivalent (Katie J NYC) at £62-75 GBP — validates demand exists

From Google Trends:

- November peak — 5x uplift vs summer trough, Christmas gifting dominates
- girls pyjamas tracks almost identically to kids pyjamas — gender-specific search as common as generic
- No premium brand appears in any top related queries — mass market owns search
- luxury pyjamas near-zero — consumers don't search "luxury" to find premium
- White Fox explosive growth from 2023 — social-first brands can scale fast
- matching kids pjs rising — family gifting behaviour signal

From Social Analysis:

- Mass-market brands dominate scale: Next (3.4M IG), White Fox (4.2M combined), M&S (2.4M IG) hold 60–65% of total audience; most UK premiums stay sub-300K IG and negligible on TikTok.
- Engagement inverts with scale: Pink Palm Puff leads at ~2.37% (highest), followed by Roller Rabbit (~1.16%); mass-market brands fall below 0.1–0.2%.
- Carousel dominates content: 8–12 of last 12 posts for most brands (especially premiums); static images obsolete; Reels used selectively by mass-market and White Fox.
- TikTok underutilized by UK brands: Most sub-10K–70K followers with low recent video views; only Pink Palm Puff (~967K TikTok, ~33.4K avg views/top 3) and White Fox (~1.5M TikTok) show strong presence.
- Pink Palm Puff is the clear outlier: TikTok-dominant (59% of 1.64M combined followers), top engagement (2.37%), elite ratio (~12,291:1), all-carousel IG — benchmark for authentic, founder-led premium teen content.

---

## Notebooks

### 01 — Competitor Pricing Analysis
Scrapes publicly available product pricing from 6 comparable brands across UK and US markets. Maps the competitive landscape using manually collected pricing data from 6 comparable brands across UK and US markets. Identifies pricing white space in the 11–19 segment.

**Skills demonstrated:** web scraping, BeautifulSoup, pandas, matplotlib, data cleaning

### 02 — Google Trends Analysis
Uses the pytrends API to analyse search volume trends for relevant terms (kids pyjamas, girls pyjamas, kids pjs, kids pajamas) across UK and US markets. Identifies seasonality patterns, year-on-year demand growth, and geographic opportunity.

**Skills demonstrated:** API integration, time series analysis, pytrends, seaborn heatmap

### 03 — Social Media Analysis
Collects public social metrics (follower count, estimated engagement rate, posting frequency) for comparable brands across Instagram and TikTok. Benchmarks brand performance and identifies which brands have the strongest community relative to their size.

**Skills demonstrated:** data collection, pandas, comparative analysis, seaborn visualisation

### 04 — Financial Modelling
Builds a three-scenario revenue projection model (conservative, base, optimistic) for a bootstrapped e-commerce launch. Includes break-even analysis, margin sensitivity, and CAC (customer acquisition cost) assumptions based on industry benchmarks.

**Skills demonstrated:** financial modelling in Python, scenario analysis, sensitivity tables, plotly

---

## Tech Stack

- Python 3.11
- Jupyter Notebooks
- pandas, numpy
- matplotlib, seaborn, plotly
- BeautifulSoup4, requests
- pytrends
- scipy (financial modelling)

---

## Setup & Installation

```bash
# Clone the repository
git clone https://github.com/rosesparrow/premium-kidswear-market-analysis.git
cd premium-kidswear-market-analysis

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

---

## Limitations & Caveats

- Social media metrics are point-in-time snapshots collected manually
- Web scraping reflects pricing at time of collection; fashion pricing changes seasonally
- Financial projections are illustrative scenario models, not forecasts; assumptions are documented within the notebook
- Google Trends data is relative (indexed 0–100) rather than absolute search volume

---

Independent market analysis project. Conducted using publicly available data sources only.

---

*Project status: In progress*
