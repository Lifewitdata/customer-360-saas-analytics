<img src="https://capsule-render.vercel.app/api?type=waving&color=0:667eea,100:764ba2&height=170&section=header&text=Customer%20360&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=SaaS%20Product%20Adoption%20%C2%B7%20Retention%20%26%20Revenue%20Analytics&descAlignY=62&descSize=18" width="100%"/>

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=21&duration=2800&pause=900&color=667EEA&center=true&vCenter=true&width=720&lines=One+customer.+One+row.+Every+signal+that+matters.;500K+customers+%E2%80%A2+24+months+%E2%80%A2+5+tables;Adoption+%E2%86%92+Retention+%E2%86%92+Revenue+%E2%86%92+Risk)](https://git.io/typing-svg)

![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![lifelines](https://img.shields.io/badge/lifelines-667EEA?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

</div>

---

## ⚡ The headline dashboard

<div align="center">

| | |
|---|---|
| 🎯 **Activation rate** | `76.4%` — activated churn **33.6%** vs **74.4%** never-activated |
| ⏱️ **Median time-to-value** | `15 days` |
| 💰 **MRR growth** | `$4.06M → $100.37M` over 24 months |
| 📈 **NRR / GRR** | `98.3%` / `96.7%` |
| 🤖 **Churn model** | `AUC 0.715` — top decile **2.7x** lift |
| 🚨 **MRR at risk** | `$3.71M/month` in the two highest-risk segments |

</div>

### Retention by plan — the ladder

```
Enterprise  ████████████████████  85.5%
Scale       ████████████████░░░░  71.5%
Growth      ████████████░░░░░░░░  56.1%
Starter     ████████░░░░░░░░░░░░  39.1%
            └─ M12 retention ─┘
```

### The five segments

| Segment | Customers | Churn | Character |
|:---|---:|---:|:---|
| 🔴 **Critical** | 45,886 | 99.1% | Ghost accounts — almost no usage, already gone |
| 🟠 **Struggling** | 15,319 | 53.9% | Fighting the product — tickets, low breadth |
| 🟡 **Quiet majority** | 194,891 | 45.6% | Logging in, not expanding |
| 🟢 **Steady growers** | 135,610 | 42.3% | Healthy usage, upgrading slowly |
| 💜 **Power users** | 108,294 | 14.9% | Deep adoption, 6+ features, the crown jewels |

---

## 📓 The notebook

**`notebooks/customer360_analysis.ipynb`** — 43 cells, executed with outputs. Written the way a senior analyst actually works: one idea per cell, every number derived in the open. No data generation inside — it loads CSVs and reasons step by step.

<details>
<summary><b>🔍 The ten moves (click to expand)</b></summary>

1. **KPI definitions** — activation, DAU/MAU, stickiness, logo churn, MRR, NRR/GRR, ARPU, LTV
2. **Data cleaning** — validation gate: nulls, duplicates, foreign keys, ranges
3. **Customer 360 table** — one row per customer: usage, revenue, tickets, activation, tenure
4. **Adoption** — funnel by channel, time-to-value, the 33.6% vs 74.4% activation cliff
5. **Retention** — cohort curves, Kaplan-Meier survival, the January spike (**10.4%** vs 6.1%)
6. **Revenue** — MRR waterfall, NRR/GRR trends, LTV by plan
7. **Segmentation** — K-Means + 0–100 health score
8. **Churn model** — leakage-safe 90-day horizon, permutation importances, deciles
9. **Visuals** — every chart carries its own one-line takeaway
10. **Recommendations** — 5 prioritized plays with expected impact

</details>

**`data_csv/`** — the five source tables as gzipped CSVs, ready to load.

---

## 📖 The story the data tells

> **Activation is the whole game.** Three-quarters of signups activate — and churn at less than half the rate of those who don't. Every day shaved off the 15-day median time-to-value is retention earned.

> **Plan tier predicts everything.** Enterprise retains at 86% after a year; Starter at 39%. The Starter → Growth upgrade path is the single most valuable motion in the business.

> **January is dangerous.** Logo churn hits 10.4% against 6.1% in other months — renewals and budget cycles. Retention plays should start in Q4, not Q1.

> **Two segments hold $3.71M/month of exposed MRR.** Critical and Struggling are identifiable months before they leave — usage drop, support spikes, payment friction are the tells.

---

## 🚀 Run it yourself

```bash
# 1. unzip customer360-datasets-csv.zip so data_csv/ sits beside notebooks/
# 2. open the notebook, then Kernel → Restart & Run All   (~10 minutes)
jupyter notebook notebooks/customer360_analysis.ipynb
```

Needs `pandas numpy scikit-learn lifelines matplotlib` · Python 3.12 · scripts in `src/` are the original numbered pipeline if you prefer code over notebooks.

---

<details>
<summary><b>⚖️ A note on honesty</b></summary>

This is a **synthetic dataset**, seeded to mirror realistic B2B SaaS dynamics: acquisition seasonality, plan-tier churn hazards, engagement-driven usage, upgrades for engaged accounts, support-pain → churn causality, and a January renewal-season spike. The methodology is production-grade — but the findings describe the seeded world, not a real company. Every number above is a real output of real analysis on that data.

</details>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:764ba2,100:667eea&height=120&section=footer" width="100%"/>
