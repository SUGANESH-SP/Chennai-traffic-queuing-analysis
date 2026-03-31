# 🚦 Chennai Traffic Congestion Analysis  
## Comparative Study of M/M/1 and M/D/1 Queuing Models

**Author:** Suganesh SP  
**Degree:** B.Sc. Statistics (2023–2026)  
**Tools:** Python, pandas, numpy, scipy, statsmodels, matplotlib, seaborn  

---

## 📌 Project Overview

This project applies queuing theory to analyse traffic congestion at major signalised intersections in Chennai, including Kathipara, Koyambedu, Porur, and T. Nagar.

The study compares **M/M/1** and **M/D/1** queue models to evaluate system performance under different traffic conditions and quantify congestion levels.

---

## 🎯 Objectives

- Model urban traffic flow using queuing theory  
- Compare stochastic vs deterministic service systems  
- Evaluate congestion using statistical analysis  
- Derive insights for traffic system efficiency  

---

## 📊 Dataset

- **Total Records:** 17,472 hourly observations  
- **Time Period:** January – June 2024  

The dataset is **simulated using real-world traffic parameters** derived from sources such as the TomTom Traffic Index and related traffic studies.

---

## ⚙️ Methodology

### Distribution Analysis
- Index of Dispersion  
- Chi-Square Goodness-of-Fit  
- Kolmogorov–Smirnov Test  

**Result:** Vehicle arrivals follow a **Negative Binomial distribution**, indicating over-dispersion.

---

### Queuing Models

#### 🔹 M/M/1
- Poisson arrivals  
- Exponential service times  

#### 🔹 M/D/1
- Poisson arrivals  
- Deterministic service times  

---

### Key Parameters

- Arrival Rate (λ)  
- Service Rate (μ)  
- Traffic Intensity (ρ = λ / μ)  

---

## 📈 Statistical Tests

| Test | Purpose | Result |
|------|--------|--------|
| Index of Dispersion | Poisson diagnostic | Over-dispersed |
| Chi-Square GoF | Distribution fit | Rejected |
| KS Test | Distribution comparison | Negative Binomial selected |
| Paired t-test | MM1 vs MD1 | Significant difference |
| One-Way ANOVA | Period comparison | Significant |
| Tukey HSD | Pairwise analysis | All significant |
| Wilson CI | Breakdown probability | Estimated |

---

## 📊 Results Summary

| Period | λ (veh/hr) | μ (veh/hr) | ρ | MM1 Lq | MD1 Lq |
|--------|-----------|-----------|----|--------|--------|
| Night | 98.9 | 2340 | 0.042 | 0.002 | 0.001 |
| Midday | 758.3 | 1872 | 0.405 | 0.328 | 0.164 |
| Morning Peak | 1322 | 1620 | 0.816 | 8.357 | 4.178 |
| Evening Peak | 1450 | 1512 | 0.959 | 9.709 | 4.855 |

---

## 🔥 Key Findings

- Vehicle arrivals exhibit **over-dispersion** and deviate from Poisson assumptions  
- **M/D/1 queues reduce queue length by ~50%** compared to M/M/1  
- System performance deteriorates significantly as **ρ approaches 1**  
- Evening peak period shows highest congestion and breakdown probability  

---

## 🧠 Insight

> Reducing service-time variability (as in M/D/1 systems) significantly improves traffic flow efficiency in signalised intersections.

---

## 📁 Project Structure

```
📦 Chennai-Traffic-Queuing-Analysis
 ┣ 📜 traffic_congestion_chennai.ipynb
 ┣ 📜 Chennai_Raw_Data.csv
 ┗ 📜 README.md
```

---

## 💻 Technologies Used

- Python 3  
- pandas  
- numpy  
- scipy  
- statsmodels  
- matplotlib / seaborn  

---

## 📌 Conclusion

This study demonstrates how queuing theory and statistical methods can be applied to model and analyse urban traffic congestion, providing meaningful insights into system performance and efficiency.

---

## ⭐ Star this repository if you found it useful!
