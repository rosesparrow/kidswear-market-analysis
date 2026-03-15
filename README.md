# Kids Sleepwear Market Analysis — E-commerce Market Entry

A data-driven market entry analysis for the UK children's and teen sleepwear category, exploring whether a gap exists for a new direct-to-consumer brand.

The analysis uses publicly available data — competitor pricing, Google Trends, social media metrics, and ONS demographic data — to assess market structure, demand signals, and competitive dynamics. It finds a structural positioning gap: no UK brand sits at the intersection of teen-specific identity (ages 11–19), sleepwear focus, and accessible pricing above the mass-market ceiling. US brands like Pink Palm Puff and Katie J NYC validate the model — but neither has a UK equivalent.

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
│   └── strategic_context.ipynb
│
├── 05_market_opportunity/
│   ├── market_opportunity.ipynb
│   └── data/
│       └── uk_ons_population_age.xlsx
│
└── 06_financial_modelling/
    └── financial_modelling.ipynb
```

---

## Analytical Flow

Each notebook builds on the previous, moving from raw data collection through to strategic synthesis and quantification.

| # | Notebook | What it does |
|---|----------|-------------|
| 01 | Competitor Pricing | Maps pricing and brand positioning across 20 UK and US brands; identifies price tiers, age coverage, and the positioning gap |
| 02 | Google Trends | Analyses search demand via the pytrends API — seasonality, term selection, geographic comparison, brand discovery channels |
| 03 | Social Media Analysis | Benchmarks 21 brands across Instagram and TikTok on follower scale, engagement, content strategy, and platform balance |
| 04 | Strategic Context | Synthesises business models across the competitor set; produces competitive positioning maps showing the structural gap |
| 05 | Market Opportunity | Quantifies the addressable demographic using ONS data and a cohort-component forecast model; sizes the gap and assesses risks |
| 06 | Financial Modelling | Unit economics (POD vs direct manufacturing), 3-year revenue scenarios, break-even analysis, and model comparison |

---

## Key Findings

### Competitor Pricing (Notebook 01)
- The UK mass-market cluster sits between £6–33 (SHEIN through to Next)
- Lifestyle/young adult brands (Brandy Melville, White Fox, Lounge) operate at £18–60 but target adults, not teens with sleepwear
- US comparables validate above-mass-market pricing: Katie J NYC (£54–75), Pink Palm Puff (£70), Pink Chicken kids (£44–50)
- The pure price gap (£33–45) is narrower than initially apparent, but the positioning gap — no UK brand at the intersection of teen identity + sleepwear + accessible pricing — is wide

### Search Trends (Notebook 02)
- November drives a ~5x uplift in search interest vs summer — Christmas gifting dominates the category
- `girls pyjamas` tracks almost identically to `kids pyjamas` — gender-specific search is as common as generic
- No above-mass-market brand appears in any top related queries — Next, Primark, and M&S own search entirely
- Pink Palm Puff has near-zero UK Google search presence despite 1.6M social followers — discovery is social, not search

### Social Media (Notebook 03)
- Engagement inverts with scale: Pink Palm Puff leads at ~2.37%, mass-market brands sit below 0.1%
- TikTok is underutilised by UK brands — most sit below 10K–70K followers
- Pink Palm Puff is the standout benchmark: TikTok-dominant, founder-led, highest engagement in the dataset

### Strategic Context (Notebook 04)
- The competitive positioning map plots 20 brands by price vs target age — the teen zone (11–19) above mass-market pricing is structurally empty in the UK
- Pink Palm Puff is the only brand inside the gap — and it is US-only, TikTok-native
- Three converging gaps identified: positioning (no UK teen sleepwear brand), identity (no teen-specific aesthetic), channel (no UK sleepwear brand with meaningful TikTok presence)

### Market Opportunity (Notebook 05)
- The UK 11–19 population is ~7.5 million and remains stable through 2035 across all forecast scenarios
- Conservative estimate (1% penetration, £40 AOV derived from pricing data): ~£1.5M addressable market for girls' teen sleepwear. Moderate scenario (3%) reaches ~£4.5M. Penetration rate is the most sensitive assumption — these scenarios illustrate the range of outcomes rather than predict a specific market size
- Key open question: US brands validate above-mass-market pricing for kids apparel and kids sleepwear separately, but whether teen-specific sleepwear commands these prices as a standalone category is untested

### Financial Modelling (Notebook 06)
- POD margins range from 23–53% depending on SKU and price point, requiring near-zero upfront capital; break-even at ~148–281 orders depending on pricing
- Direct manufacturing margins are strong (66–79%) but require £5K+ inventory investment and ~322–449 orders to break even in Year 1
- The cumulative profit crossover occurs around Year 2: Direct overtakes POD as the superior model once volume supports the inventory investment
- ~90% of DTC startups close by year 5 (Source: One Fourth) — volume assumptions are deliberately conservative

---

## Methodology & Data Sources

| Component | Method | Source |
|-----------|--------|--------|
| Competitor pricing | Manual collection from public product pages | Brand websites, Feb/Mar 2026 |
| Search trends | pytrends API | Google Trends |
| Social metrics | Manual collection + Countik | Instagram, TikTok (public accounts) |
| Demographics | ONS mid-year population estimates (2011–2024) | Office for National Statistics |
| Financial modelling | Scenario analysis with sourced assumptions | Industry benchmarks (Shopify, BoF/McKinsey, IRP Commerce, One Fourth, BusinessDojo) |

---

## Tech Stack

- Python 3.11+
- Jupyter Notebooks
- pandas · numpy
- matplotlib · seaborn
- pytrends
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
- Pricing reflects time of collection; fashion pricing changes seasonally
- Google Trends data is relative (indexed 0–100), not absolute search volume
- Financial projections are illustrative scenario models, not forecasts — all assumptions are documented within the notebook
- Direct manufacturing COGS are estimated from industry benchmarks; actual costs require a supplier costing exercise
- Competitor pricing uses a representative sample per brand (2–5 products); full catalogue audits are noted as a future enhancement

---

## Skills Demonstrated

Data collection and cleaning · API integration (pytrends) · Exploratory data analysis · Data visualisation (matplotlib, seaborn) · Market sizing and demographic analysis · Cohort-component population forecasting · Competitive benchmarking and positioning analysis · Financial modelling and scenario analysis · Unit economics and break-even analysis · Strategic synthesis and opportunity framing

---

*Independent market analysis project. All data is publicly available.*
*Last updated: March 2026*