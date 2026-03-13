# Kids Sleepwear Market Analysis — E-commerce Market Entry

A data-driven market entry analysis for the UK children's and teen sleepwear category, exploring whether a gap exists for a new direct-to-consumer brand.

The analysis uses publicly available data — competitor pricing, Google Trends, social media metrics, and ONS demographic data — to assess market structure, demand signals, and competitive dynamics. It finds a structural gap: established UK brands largely stop serving children at age 10–14, while the teen segment (11–19) is underserved by brands offering genuine quality, aesthetic differentiation, and identity at an accessible price point.

---

## Research Questions

1. How are competitors priced, and what does the competitive landscape look like across the UK sleepwear market?
2. What does consumer search behaviour reveal about demand patterns, seasonality, and category language?
3. How do competitor brands perform on social media, and what engagement patterns exist across segments?
4. What strategic models and business approaches do comparable brands use?
5. How large is the addressable UK demographic, and is it growing or shrinking?
6. What does a realistic financial model look like for a bootstrapped e-commerce brand entering this space?

---

## Project Structure

```
kids-sleepwear-market-analysis/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── 01_competitor_analysis/
│   ├── competitor_pricing.ipynb
│   └── data/
│       └── competitor_prices_all.csv
│
├── 02_search_trends/
│   ├── google_trends.ipynb
│   └── data/
│
├── 03_social_analysis/
│   ├── social_metrics.ipynb
│   ├── key_findings.md
│   └── data/
│       └── social_media_data_collection_v8.xlsx
│
├── 04_strategic_context/
│   └── strategic_models_competitive_context.ipynb
│
├── 05_market_opportunity/
│   ├── market_gap_analysis.ipynb
│   ├── market_demographics.ipynb
│   └── data/
│       └── uk_ons_population_age.xlsx
│
└── 06_financial_modelling/                  ← coming soon
    ├── revenue_projections.ipynb
    └── data/
```

---

## Analytical Flow

Each notebook builds on the previous, moving from raw data collection through to strategic synthesis and quantification.

| # | Notebook | What it does |
|---|----------|-------------|
| 01 | Competitor Pricing | Maps pricing and brand positioning across UK and US markets; identifies price tiers and white space |
| 02 | Google Trends | Analyses search demand via the pytrends API — seasonality, term selection, geographic comparison |
| 03 | Social Media Analysis | Benchmarks 21 brands across Instagram and TikTok on follower scale, engagement, and content strategy |
| 04 | Strategic Context | Synthesises business models across the competitor set; produces a competitive positioning map |
| 05 | Market Opportunity | Quantifies the addressable demographic using ONS data and a cohort-component forecast; frames the gap with evidence from notebooks 01–04 |
| 06 | Financial Modelling | Revenue scenarios, unit economics, and break-even analysis for a bootstrapped DTC launch *(coming soon)* |

---

## Key Findings

### Competitor Pricing (Notebook 01)
- The UK mass-market cluster sits between £6–28 (SHEIN, George, Primark, H&M, Matalan, M&S, Next)
- Premium kids brands (Boden, Desmond & Dempsey) stop at age 10–12 — none targets the teen segment with a distinct identity
- US comparables (Katie J NYC, Pink Chicken) price at £54–75 GBP, validating demand at a higher price point than any UK brand currently occupies for teens

### Search Trends (Notebook 02)
- November drives a ~5x uplift in search interest vs summer — Christmas gifting dominates the category
- `girls pyjamas` tracks almost identically to `kids pyjamas` — gender-specific search is as common as generic
- No premium brand appears in any top related queries — mass-market retailers (Next, Primark, M&S) own search entirely
- `luxury pyjamas` returns near-zero volume — consumers do not use "luxury" as search language in this category
- Implication: a new premium entrant needs a social-first discovery strategy, not an SEO-first one

### Social Media (Notebook 03)
- Mass-market brands dominate scale (Next 3.4M IG, M&S 2.4M IG), but engagement rates are lowest in the dataset (<0.1%)
- Engagement inverts with scale: Pink Palm Puff leads at ~2.37%, Roller Rabbit at ~1.16% — smaller identity-led brands generate disproportionate interaction
- Carousel is the dominant content format across premium brands (8–12 of last 12 posts); static images are largely obsolete
- TikTok is underutilised by UK premium brands — most sit below 10K–70K followers
- Pink Palm Puff is the standout benchmark: TikTok-dominant (59% of 1.64M combined followers), founder-led, all-carousel IG, highest engagement in the dataset

### Market Opportunity (Notebook 05)
- The UK 11–19 population is ~7.5 million (mid-2025 base forecast from ONS data)
- The 5–19 pipeline remains stable to slightly growing through 2035, with reliable cohort replenishment
- Full demographic analysis, cohort-component forecast model, and gap sizing in the notebook

---

## Methodology & Data Sources

| Component | Method | Source |
|-----------|--------|--------|
| Competitor pricing | Web scraping (BeautifulSoup) + manual collection | Brand websites (public product pages) |
| Search trends | pytrends API | Google Trends |
| Social metrics | Manual collection + Countik | Instagram, TikTok (public accounts) |
| Demographics | ONS mid-year population estimates (2011–2024) | Office for National Statistics |
| Financial modelling | Scenario analysis | Industry benchmarks *(coming soon)* |

---

## Tech Stack

- Python 3.11+
- Jupyter Notebooks
- pandas · numpy
- matplotlib · seaborn · plotly
- BeautifulSoup4 · requests
- pytrends
- scipy
- openpyxl

---

## Setup

```bash
git clone https://github.com/rosesparrow/kids-sleepwear-market-analysis.git
cd kids-sleepwear-market-analysis
pip install -r requirements.txt
jupyter notebook
```

---

## Limitations

- Social media metrics are point-in-time snapshots (Feb/Mar 2026); engagement rates shift over time
- Web scraping reflects pricing at time of collection; fashion pricing changes seasonally
- Google Trends data is relative (indexed 0–100), not absolute search volume
- Financial projections are illustrative scenario models, not forecasts — all assumptions are documented within the notebook
- Competitor pricing uses a representative sample per brand; full range audits are noted as a future enhancement

---

## Skills Demonstrated

Data collection and web scraping · API integration (pytrends, Google Trends) · Data cleaning and transformation (pandas) · Exploratory data analysis · Data visualisation (matplotlib, seaborn, plotly) · Time series analysis · Market sizing and demographic analysis (ONS data) · Cohort-component population forecasting · Competitive benchmarking · Financial modelling and scenario analysis · Strategic synthesis and opportunity framing

---

*Independent market analysis project. All data is publicly available.*
*Project status: In progress — financial modelling section forthcoming*
*Last updated: March 2026*
