# 🛒 Olist Brazilian E-Commerce Analysis

**An end-to-end business analysis of Brazil's largest e-commerce marketplace — identifying the root causes of low retention and proposing data-driven growth strategies.**

---

## 📌 Project Background

[Olist](https://olist.com/) is Brazil's largest multi-vendor e-commerce platform, connecting thousands of sellers to major marketplaces. This project analyzes **93,000+ customers, 110,000+ orders, and 30+ product categories** across a 20-month window (Jan 2017 – Aug 2018) to answer one central question:

> **The platform is growing — so why aren't customers coming back?**

---

## 🗂️ Dataset

- **Source:** [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle)
- **Scope:** Delivered orders only | `customer_unique_id` for deduplication | `payment_value` as revenue | `order_approved_at` as revenue recognition timestamp
- **Analysis period:** 2017-01 to 2018-08

---

## 🔍 Analysis Architecture

```
Block 0 │ Platform Overview & Market Context
Block 1 │ Data Quality & Schema Understanding
Block 2 │ (Reserved)
Block 3 │ Revenue & Order Trends
Block 4 │ Growth Drivers — Orders vs. AOV
   └── Supplement: RFM Customer Segmentation
Block 5 │ Geographic Distribution (Customers & Sellers)
Block 6 │ Logistics Efficiency (Freight, Delivery Time, Delays)
Block 7 │ Seller Distribution & In-State Advantage
Block 8 │ Payment Structure
Block 9 │ Customer Reviews & Satisfaction Drivers
   └── Supplement: Keyword Analysis, Low-Score Sellers, Product Info Hypothesis
```

---

## 💡 Core Findings

| # | Finding | Key Number |
|---|---------|------------|
| 1 | **Platform growth is real, but fragile** | Monthly revenue grew steadily Jan 2017 → May 2018; AOV declined slightly — growth is volume-driven, not value-driven |
| 2 | **Retention crisis** | Repeat purchase rate: **2.99%**; 49% of customers are already churned; only 1.5% are VIP |
| 3 | **Geography is a structural constraint** | SP / RJ / MG = 66% of users & revenue; distance from São Paulo correlates with user counts (r = −0.55) and growth rate (r = −0.58) |
| 4 | **Logistics is the #1 pain point** | Remote states wait 3× longer (AM: 26.4 days vs. SP: 8.7 days); delayed orders average 2.57 stars vs. 4.29 for on-time |
| 5 | **In-state sellers reduce freight by ~30%** | BA state validation: customers buying from local sellers pay ~30% less in freight; expanding the seller network regionally is a direct lever |

---

## 📊 Business Recommendations

### 1. Fix Logistics Before Spending on Acquisition
Delivery delay is the single strongest predictor of low ratings (25.2% of negative reviews cite logistics). Prioritize fulfillment center expansion in AM, PA, and CE before investing in marketing.

### 2. Grow the Regional Seller Network
59.7% of sellers are concentrated in SP. In-state sellers reduce freight cost ~30% and implicitly reduce delivery time. Recruiting sellers in underserved states is a dual win on cost and satisfaction.

### 3. Activate the "Important Development" Segment
24.1% of users fall into the high-potential, mid-frequency RFM segment (avg. spend: 261 BRL). These customers have shown intent but not loyalty. Targeted re-engagement (personalized promotions, category recommendations) has the highest ROI.

### 4. Prioritize Payment UX for Credit Card Users
75.3% of transactions use credit card; 66.8% use installments. Any friction in installment flow or credit approval directly impacts conversion — this is a non-negotiable UX priority.

### 5. Address Product Quality at the Seller Level
56.9% of negative reviews cite product issues. Low-rated sellers show a statistically significant pattern of policy violations and inaccurate listings. A seller quality score with enforcement thresholds would raise platform-wide NPS.

---

## 🛠️ Tools & Technologies

| Category | Stack |
|----------|-------|
| Language | Python 3 |
| Data Wrangling | pandas, numpy |
| Visualization | matplotlib, seaborn |
| Database | SQLite (via pandas read_sql) |
| Segmentation | RFM scoring (custom implementation) |
| Environment | Google Colab |
| Version Control | Git / GitHub |

---

## 📁 Repository Structure

```
olist-ecommerce-analysis/
├── README.md
├── Olist_Analysis_Full.ipynb     # Complete analysis notebook (Blocks 0–9)
├── Olist_Analysis_Denny.pptx     # 10-slide executive presentation
└── data/                         # Kaggle dataset (not committed; see link above)
```

---

## 📓 Notebook

Full interactive notebook on Google Colab:
👉 [Open in Colab](https://colab.research.google.com/drive/1HQLELdl9P_INfKR2aM7NSl4uk08BYp9K)

---

## 👤 Author

**Denny Chang（張育誠）**
Background in retail operations planning (convenience store chain, Taiwan)
Transitioning into data analytics & business intelligence roles

> *"My edge is knowing which business questions are worth asking — and knowing when the numbers are telling a story the data alone can't see."*

---

*Analysis period: Jan 2017 – Aug 2018 | Delivered orders only | Revenue = payment_value*
