# Hi, I'm Dikri! 👋

# Superstore Sales & Profitability Optimization Analysis
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-orange.svg)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Data_Visualization-green.svg)](https://seaborn.pydata.org/)

## 📌 Executive Summary
This project delivers an end-to-end Exploratory Data Analysis (EDA) on retail performance using the **Global Superstore Dataset**. Rather than just looking at surface-level metrics, this analysis digs deep into financial leakages, logistics efficiencies, and customer lifecycles. By building data-driven frameworks like **Break-Even (BE) Discount Limits** and **RFM (Recency, Frequency, Monetary) Customer Segmentation**, this notebook bridges the gap between raw data and actionable strategic initiatives to recover lost profit margins and drive revenue growth.

---

## 🛠️ Project Structure & Workflow

### 1. Data Ingestion & Quality Assurance
* **Automated Pipeline:** Programmatically fetched data via `kagglehub` from the `vivek468/superstore-dataset-final` repository.
* **Data Cleansing:** Standardized raw object formats into unified `datetime` schemas for analytical continuity.
* **Integrity Validation:** Implemented advanced programmatic sanity checks including missing value detection, data duplication scans, mathematical bounds enforcement, and business logic validations (e.g., verifying `Ship Date` $\ge$ `Order Date`).

 

### 2. Deep-Dive Analytical Insights

#### 📉 Insight 1: Discount Optimization & Financial Leakages
* **The Problem:** Aggressive sales discounting was severely eroding profit margins.
* **Methodology:** Calculated customized engineered metrics: `Total Cost`, `Unit Cost`, `Original Unit Price`, and a mathematical **Break-Even Discount (`BE_Discount`)** boundary per transaction line.
* **Key Finding:** Flat discounts at or above **20%** trigger exponential losses. Profitability drops into a deficit primarily driven by the *Binders* and *Appliances* sub-categories, with major geographic leakages localized in *Texas* and *Ohio*.
* **Business Strategy:** Cap flat item discounts at a maximum of 15% and switch to dynamic volume-based bundling models.

<img width="737" height="421" alt="image" src="https://github.com/user-attachments/assets/7c791706-de3d-4877-a645-199b00538b32" />

#### 🚚 Insight 2: Shipment Durations & SLA Assessment
* **Methodology:** Quantified the operational delta (`Ship Date` - `Order Date`) grouped across various transportation modes (`Same Day`, `First Class`, `Second Class`, `Standard Class`).
* **Key Finding:** Delivery timelines strictly conform to the expected priority tier hierarchies. However, variances within `Standard Class` indicate opportunities to streamline regional fulfillment bottlenecks.
* **Business Strategy:** Establish automated data alerts for orders nearing their SLA deadlines and leverage logistics reliability baselines to pitch premium delivery upsells.

<img width="558" height="478" alt="image" src="https://github.com/user-attachments/assets/699cc85e-0574-4c7c-8bdd-6f160c28274d" />
<img width="771" height="584" alt="image" src="https://github.com/user-attachments/assets/04f1bb16-9e69-442e-9c12-83c415f8a594" />


#### 👥 Insight 3: Customer Behavior & RFM Segmentation
* **Methodology:** Built a robust recency, frequency, and monetary valuation matrix evaluated against a master anchor baseline (`snapshot_date`). Divided scores into a 5-tier quintile matrix and mapped them using regular expressions (`re`) to construct an behavioral matrix.
* **Key Finding:** Identified clear divisions between high-value customer matrices (*Champions* and *Loyal Customers*) and fading segments (*About to Sleep*, *At Risk*, *Hibernating*). A major portion of total monetary revenue relies on a small segment of frequent shoppers.
* **Business Strategy:** Roll out zero-discount exclusive loyalty perks for *Champions* to maintain high margins, while targeting high-historical-value *At Risk* clients with automated reactivation workflows.

<img width="784" height="483" alt="image" src="https://github.com/user-attachments/assets/b0c6ddfd-e917-4b41-acd1-464a918aad51" />


#### 📅 Insight 4: Time-Series & Seasonality Growth
* **Methodology:** Deconstructed transactional records into aggregated temporal macro-windows (Monthly and Yearly trends across the historical timeline).
* **Key Finding:** Marked seasonal spikes consistently occur throughout the fourth quarter (**Q4 - September, November, December**), contrasted by a sharp post-holiday structural contraction during **Q1**.
* **Business Strategy:** Scale up inventory cycles 2-3 months ahead of the Q4 peak and schedule defensive clearance strategies or contract renewals during the dry Q1 phase.

<img width="984" height="584" alt="image" src="https://github.com/user-attachments/assets/0f52f8bd-b754-4004-ae3d-7172c3dac06e" />


---

## 💻 Tech Stack & Dependencies
* **Core Language:** Python 3.x
* **Data Manipulation:** `pandas`
* **Data Science Infrastructure:** `os`, `re`
* **Statistical Modeling Frameworks:** `statsmodels`, `patsy`
* **Data Visualization & Graphics:** `matplotlib`, `seaborn`

---

## 🚀 How to Run This Project
```bash
1. Clone the repository
git clone https://github.com/dikrifajar/Python-SuperStoreSales.git
cd Python-SuperStoreSales

2. Install dependencies
pip install -r requirements.txt

3. Run the analysis script
python Superstore.ipynb

```
---

## 🎯 Key Takeaways as a Professional Data Analyst

This project demonstrates analytical capability in:

* **Advanced Feature Engineering:** Translating abstract business constraints into concrete mathematical formulas (`BE_Discount`).
* **Marketing Analytics:** Implementing full-scale, programmatic behavioral customer segmentation (RFM) from scratch.
* **Operational Analytics:** Extracting business-critical timeline performance parameters out of raw timestamps.
* **Data Storytelling:** Translating raw Python graphs into concrete, actionable C-level executive strategies.


## Authors

- [Dikri F. Ramadhan](https://www.github.com/dikrifajar)
