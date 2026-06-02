# Nigeria Economic Shock Analysis: Subsidy Removal & Currency Reform (2019–2026)

**Analyst:** Philip Ohejira | **Project:** 10 of 14 | **Date:** May 2026  
**Tools:** Python · Power BI · Matplotlib · Seaborn · Scikit-learn  
**Data Sources:** NBS · CBN · World Bank · NBS Petrol Price Watch

---

## Problem Statement

On **29 May 2023**, the Tinubu administration removed Nigeria's fuel subsidy, pushing petrol prices from ₦185 to ₦617 per litre overnight — a 234% increase in a single day. Fifteen days later, the Central Bank of Nigeria unified its exchange rate windows, devaluing the naira by over 40% against the dollar overnight, from ₦460 to ₦750 per USD.

These two decisions triggered Nigeria's worst cost-of-living crisis in nearly three decades. Yet no public analytical resource consolidates the full data story — what happened, which sectors were hit hardest, how the naira collapse amplified the inflation shock, and where the economy is heading.

This project fills that gap.

---

## Objectives

1. Quantify the inflation shock before and after the May–June 2023 policy events
2. Analyse the exchange rate collapse and its relationship with headline inflation
3. Identify which CPI sectors were most severely impacted
4. Assess GDP and poverty trajectory against petrol price movements
5. Forecast Nigeria's inflation trajectory through end-2026

---

## Data Sources

| Source | Dataset | Format |
|---|---|---|
| NBS (nigerianstat.gov.ng) | Monthly CPI — Headline, Food, Core (2019–2026) | CSV |
| CBN (cbn.gov.ng) | Monthly exchange rate — Official & Parallel (2019–2026) | CSV |
| World Bank (data.worldbank.org) | Annual GDP growth & poverty headcount ratio | CSV |
| NBS Petrol Price Watch | Annual petrol pump price (2019–2026) | CSV |

---

## Project Structure

```
Nigeria-Economic-Shock-Analysis/
├── data/
│   ├── raw/                         # Original source CSV files
│   └── processed/                   # Cleaned and merged datasets
├── notebooks/
│   └── nigeria_economic_shock_analysis.ipynb
├── dashboard/                       # Power BI .pbix file
├── reports/                         # All generated figures (PNG)
└── README.md
```

---

## Key Findings

### Inflation
| Era | Average Headline Inflation |
|---|---|
| Pre-Reform (2019 – May 2023) | 15.75% |
| Shock Period (Jun – Dec 2023) | 26.26% |
| Crisis Peak (2024) | 33.07% |
| Recovery (2025 – present) | 18.81% |

- Inflation peaked at **34.80% in April 2024** — the highest in 28 years
- Current rate (April 2026): **15.69%** following the NBS CPI rebase in January 2025
- Food inflation was the hardest-hit sector, reaching **40.53%** at peak
- Transport inflation surged immediately after subsidy removal, jumping from 18.10% to 28.70% within two months

### Exchange Rate
- Pre-unification official rate: **₦462/USD**
- Peak rate: **₦1,680/USD** (late 2024)
- Current rate (May 2026): **₦1,374/USD**
- Total naira depreciation since June 2023: **197.4%**

### Petrol Price
- Pre-removal: **₦185/litre**
- Day after removal: **₦617/litre (+234%)**
- Current estimate (2026): **₦1,100/litre (+495% from 2019 baseline)**

### Poverty
- 2019 headcount: **40.1%**
- 2024 headcount: **45.0%** — approximately 11 million additional Nigerians pushed below the poverty line
- 2026 forecast: **43.5%** — gradual improvement as inflation moderates

### Correlation
- Exchange rate and headline inflation show a **strong positive correlation (0.94)** — naira depreciation was the primary transmission mechanism for the inflation shock
- Core inflation and the official exchange rate correlate at **0.97**, confirming import cost passthrough as the dominant driver

---

## Visualisations

| Figure | Description |
|---|---|
| fig01_headline_inflation.png | Nigeria headline inflation timeline with event markers (2019–2026) |
| fig02_inflation_breakdown.png | Headline vs Food vs Core inflation comparison |
| fig03_exchange_rate.png | Official vs parallel market rate — the naira collapse |
| fig04_era_comparison.png | Average inflation by policy era (bar chart) |
| fig05_sector_impact.png | CPI sector impact: pre-reform vs peak vs recovery |
| fig06_correlation_heatmap.png | Correlation matrix: inflation components vs exchange rate |
| fig07_gdp_petrol_poverty.png | GDP growth, petrol price & poverty trajectory |
| fig08_inflation_forecast.png | Inflation forecast May–December 2026 |

---

## Conclusion

The 2023 dual-reform shock — fuel subsidy removal and exchange rate unification — was necessary for long-term fiscal sustainability but triggered a severe short-term humanitarian cost. The data shows that the naira's 197.4% depreciation was the primary amplifier of Nigeria's inflation crisis, transmitting through import costs into food and transport prices that hit low-income households hardest.

While the NBS CPI rebase in January 2025 repositioned the inflation series, the structural cost-of-living impact remains unresolved for the estimated 45% of Nigerians still below the poverty line. The forecast trajectory suggests inflation stabilising between 13–16% through end-2026, provided energy costs remain stable — a genuine moderation, but still far above the pre-reform baseline of 15.75%.

---

## How to Reproduce

```bash
# 1. Clone the repository
git clone https://github.com/Pheezo-SQ/nigeria-economic-shock-analysis.git

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# 3. Run the notebook
# Open notebooks/nigeria_economic_shock_analysis.ipynb in VS Code or Jupyter
# Run cells section by section
```

---

*Philip Ohejira · PGD Information Technology · NOUN Abuja · 2026*  
*github.com/Pheezo-SQ · linkedin.com/in/philip-o-821b17116*
