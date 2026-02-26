# Premium Kidswear & Teen Apparel — E-commerce Market Entry Analysis

## Overview

This project presents a data-driven market entry analysis for a hypothetical direct-to-consumer premium loungewear brand targeting the 11–19 age demographic in the UK, with secondary analysis of US expansion potential.

The analysis identifies a structural gap in the UK premium kidswear market: established luxury loungewear brands (e.g. Desmond & Dempsey, Roller Rabbit, Pink Chicken) are primarily adult-focused, while the 11–19 segment is underserved by brands offering genuine quality and aesthetic differentiation at a mid-luxury price point.

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
├── README.md
├── requirements.txt
├── .gitignore
│
├── 01_competitor_analysis/
│   ├── competitor_pricing.ipynb        # Price point scraping & positioning map
│   └── data/
│
├── 02_search_trends/
│   ├── google_trends.ipynb             # Demand trends, seasonality, UK vs US
│   └── data/
│
├── 03_social_analysis/
│   ├── social_metrics.ipynb            # Follower counts, engagement rates, posting cadence
│   └── data/
│
├── 04_financial_modelling/
│   ├── revenue_projections.ipynb       # Revenue scenarios, break-even, sensitivity analysis
│   └── data/
│
└── reports/
    └── summary_visualisations/         # Key charts exported for presentation use
```

---

## Methodology & Data Sources

| Component | Method | Data Source |
|---|---|---|
| Competitor pricing | Web scraping (BeautifulSoup) | Brand websites (public product pages) |
| Search trends | API via pytrends | Google Trends |
| Social metrics | Manual collection + Social Blade | Instagram, TikTok (public accounts) |
| Financial modelling | Scenario analysis | Industry benchmarks, Companies House filings |

---

## Key Findings

*This section will be updated as each analytical component is completed.*

---

## Notebooks

### 01 — Competitor Pricing Analysis
Scrapes publicly available product pricing from 6 comparable brands across UK and US markets. Maps the competitive landscape by price point and product category. Identifies pricing white space in the 11–19 segment.

**Skills demonstrated:** web scraping, BeautifulSoup, pandas, matplotlib, data cleaning

### 02 — Google Trends Analysis
Uses the pytrends API to analyse search volume trends for relevant terms (luxury pyjamas, teen loungewear, kids PJs gift, etc.) across UK and US markets. Identifies seasonality patterns, year-on-year demand growth, and geographic opportunity.

**Skills demonstrated:** API integration, time series analysis, pytrends, plotly, geographic data visualisation

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

- Social media metrics are point-in-time snapshots collected manually; they are indicative rather than longitudinal
- Web scraping reflects pricing at time of collection; fashion pricing changes seasonally
- Financial projections are illustrative scenario models, not forecasts; assumptions are documented within the notebook
- Google Trends data is relative (indexed 0–100) rather than absolute search volume

---

## Author

Independent market analysis project. Conducted using publicly available data sources only.

---

*Project status: In progress*
