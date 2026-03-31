# Chennai Traffic Congestion Analysis
## Comparative Study of M/M/1 and M/D/1 Queuing Models

**Author:** SUGANESH SP  
**Degree:** BSc Statistics, 2023–26  
**Tools:** Python, scipy, statsmodels, matplotlib, pandas

---

## Project Overview

This study applies M/M/1 and M/D/1 queuing models to analyse 
traffic congestion at four major signalised intersections in 
Chennai — Kathipara, Koyambedu, Porur, and T. Nagar.

The dataset contains 17,472 hourly records spanning 
January to June 2024, derived from the TomTom Traffic 
Index (2025) and supplementary published sources.

---

## Key Findings

- Vehicle arrivals follow a **Negative Binomial distribution** 
  (99.8% subgroup pass rate) — Poisson rejected due to 
  structural over-dispersion
- **M/D/1 produces queue lengths exactly half those of M/M/1** 
  for fixed-cycle signals (paired t-test: t = 27.39, p < 0.001)
- **Kathipara Junction Evening Peak** operates at ρ = 1.052 — 
  chronically oversaturated with 59.6% breakdown rate
- All four time periods are statistically distinct 
  (ANOVA: F = 26,531, p < 0.001)
- Evening Peak breakdown probability = 0.459 
  (95% Wilson CI: 0.441, 0.477)

---

## Statistical Tests Conducted

| Test | Purpose | Result |
|---|---|---|
| Index of Dispersion | Poisson diagnostic | ID = 23–107, over-dispersed |
| Chi-Square GoF | Poisson formal test | Rejected, p = 0.000 |
| KS Test | Multi-distribution fit | NegBin wins at 99.8% |
| Paired t-test | MM1 vs MD1 difference | t = 27.39, p < 0.001 |
| One-Way ANOVA | Period distinctness | F = 26,531, p < 0.001 |
| Tukey HSD | Pairwise comparisons | All 6 pairs significant |
| Wilson CI | Breakdown probability | EP: 0.459 (0.441, 0.477) |

---

## Results Summary

| Period | λ (veh/hr) | μ (veh/hr) | ρ | MM1 Lq | MD1 Lq |
|---|---|---|---|---|---|
| Night | 98.9 | 2,340 | 0.042 | 0.002 | 0.001 |
| Midday | 758.3 | 1,872 | 0.405 | 0.328 | 0.164 |
| Morning Peak | 1,322 | 1,620 | 0.816 | 8.357 | 4.178 |
| Evening Peak | 1,450 | 1,512 | 0.959 | 9.709 | 4.855 |

---

## Project Structure

| File | Description |
|---|---|
| `traffic_congestion_chennai.ipynb` | Main analysis notebook |
| `Chennai_Raw_Data.csv` | Dataset (17,472 records) |

---

## Technologies Used

- **Python 3** — core analysis
- **pandas** — data manipulation
- **scipy** — statistical tests and distribution fitting
- **statsmodels** — ANOVA, Tukey HSD, Wilson CI
- **matplotlib / seaborn** — visualisations
- **numpy** — numerical computation
```

---
