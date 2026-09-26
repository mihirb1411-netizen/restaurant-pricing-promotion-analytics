# Restaurant Pricing & Promotion Analytics

### DDMA Class Assignment | Business Analyst Decision-Support Model

A reproducible Python/Jupyter analysis of restaurant menu pricing, competitive benchmarking, and promotion experimentation.

> **Academic assignment:** This repository was created for a DDMA class assignment. It is a decision-support and experimentation framework, not a production pricing engine or machine-learning prediction system.

---

## Overview

The analysis uses a supplied restaurant menu master and a supplied competitor pricing profile to answer practical business questions around:

- Menu price structure and category positioning
- Item popularity and preparation-time patterns
- Price–popularity association
- Comparable category/segment competitive benchmarking
- Seasonal and promotional mechanics observed in the competitor profile
- Transparent test hypotheses for pricing and promotion decisions
- A repeatable commercial learning cycle for future transaction data

### Business logic

**Price + Promotion + Seasonality + Channel + Menu Mix → Demand → Revenue → Margin**

The current dataset does **not** contain the transaction-level evidence required to estimate the latter stages reliably.

---

## Key findings

Based on the supplied menu records:

| Metric | Result |
|---|---:|
| Menu items | 10 |
| Categories | 3 |
| Original variables | 15 |
| Price range | ₹40–₹550 |
| Average price | ₹254 |
| Average popularity | 4.66 / 5 |
| Pearson price–popularity association | 0.405 |

Category summary:

| Category | Items | Avg. Price | Avg. Popularity | Avg. Prep Time |
|---|---:|---:|---:|---:|
| Breads & Rice | 4 | ₹126 | 4.55 | 10.2 min |
| Desserts & Beverages | 2 | ₹145 | 4.65 | 12.5 min |
| Main Course | 4 | ₹435 | 4.78 | 22.5 min |

The price–popularity relationship is **cross-sectional and non-causal**. It should not be interpreted as evidence that changing price will cause popularity or demand to change.

---

## Competitive benchmarking

The supplied competitor profile is **segment-level**, rather than an exact dish-by-dish menu comparison. Therefore the analysis only compares mapped categories/segments where the comparison is meaningful.

The competitor profile provides seasonal price corridors and promotional mechanics. These are treated as **benchmark observations and test hypotheses**, not evidence of guaranteed sales uplift.

---

## Analytical workflow

```text
Source Data
    ↓
Data Validation & Cleaning
    ↓
Descriptive Menu Analytics
    ↓
Price / Popularity Analysis
    ↓
Competitive Benchmarking
    ↓
Promotion & Seasonal Hypotheses
    ↓
Controlled Test Design
    ↓
Measure → Compare → Scale / Stop
```

---

## What this model does NOT claim

This repository deliberately does not claim to:

- Estimate causal price elasticity
- Forecast restaurant demand
- Predict revenue from the current menu master
- Calculate profit-optimal prices
- Measure actual promotion uplift
- Calculate promotion ROI
- Train a reliable supervised ML model

Those analyses require transaction-level and cost data that are not present in the supplied dataset.

---

## Recommended future data

To move from descriptive decision support to measured commercial optimization, collect:

- Date / timestamp
- Item ID
- Listed price
- Discount amount or percentage
- Promotion ID
- Units sold
- Revenue
- Sales channel
- Day of week
- Season
- Footfall / covers
- Weather or major events
- Unit / ingredient cost

This would support promotion attribution, contribution-margin analysis, demand measurement, and eventually price-elasticity estimation.

---

## Repository structure

```text
restaurant-pricing-promotion-analytics/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── Restaurant_Pricing_Promotion_Analytics.ipynb
│
├── report/
│   └── Restaurant_Pricing_Promotion_Analytics_Report.docx
│
└── data/
    └── README.md
```

---

## Running the notebook

### Google Colab

1. Open the `.ipynb` file in Google Colab.
2. Run the notebook from top to bottom.
3. The final notebook is designed to keep the analytical logic reproducible.

### Local Jupyter

```bash
pip install -r requirements.txt
jupyter notebook notebooks/Restaurant_Pricing_Promotion_Analytics.ipynb
```

---

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook / Google Colab
- Excel source data

---

## Academic context

**Course:** DDMA

**Institution:** Symbiosis Artificial Intelligence Institute (SAII), Pune

**Type:** Class assignment / academic business analytics exercise

---

## Author

**Mihir Bhavigadda**  
BBA (Artificial Intelligence)  
Symbiosis Artificial Intelligence Institute, Pune

---

## Disclaimer

This repository is intended for academic and educational use. The analysis is based on the supplied assignment materials and should not be interpreted as a live commercial pricing recommendation without transaction, cost, operational, and market validation data.
