# MICROSOFT-ELEVATE-INTERNSHIP-POWERBI-PROJECT
# 📊 Revenue Hemorrhage Intelligence Dashboard
### A 360° Customer Churn Detection, Prevention & Recovery System

---

## 🏆 Problem Statement
### Turning the **$168 Billion Silent Business Killer** into a Competitive Advantage

---

## 🚨 Background & The Crisis

Most businesses are **bleeding revenue every single day — and they don't even know it.**

U.S. brands alone lose an estimated **$168 billion annually** due to customer attrition.

Key insights:

- Acquiring a new customer costs **5 to 25 times more** than retaining an existing one.
- A **5% improvement in retention** can increase profits by **25% to 95%**.
- **74% of customers** permanently switch brands after a single poor experience.

This project transforms raw churn data into **actionable business intelligence** to detect, prevent, and recover lost revenue.

---

## 🎯 Project Objectives

This **multi-layer Power BI analytics suite** converts raw churn data into actionable intelligence by:

- Detecting **customers showing early churn signals**
- Scoring customers using **dynamic churn risk levels (High / Medium / Low)**
- Quantifying **revenue at risk and revenue already lost**
- Analyzing churn across **contracts, services, and payment methods**
- Providing **strategic retention insights**

---

## 📂 Project Structure (5-Page Intelligence Suite)

The dashboard is divided into **five analytical modules**.

| Page | Title | Purpose |
|-----|------|------|
| P1 | Executive Overview | High-level health check & KPI monitoring |
| P2 | Churn Deep Dive | Detailed analysis of customers who churn |
| P3 | Revenue Intelligence | Financial impact and revenue leakage analysis |
| P4 | Customer Risk Profile | Demographic & behavioral churn analysis |
| P5 | Retention Strategy | Retention targets and recovery funnel |

---

## 🛠️ Technical Stack & Data Architecture

### Dataset Overview

The project uses the **Telco Customer Churn Dataset** containing:

- **7,043 customer records**
- **21 features**

| Category | Fields | Description |
|--------|--------|--------|
| Demographics | gender, SeniorCitizen, Partner, Dependents | Basic customer profile |
| Services | InternetService, OnlineSecurity, TechSupport, etc. | Service subscription details |
| Account | tenure, Contract, PaymentMethod | Billing and contract details |
| Financial | MonthlyCharges, TotalCharges | Revenue generated per customer |
| Target | Churn | Indicates whether the customer left |

---

## 📊 DAX Measure Library

### Volume Metrics

```DAX
Total Customers =
DISTINCTCOUNT(TelcoChurn[customerID])

Total Churned Customers =
CALCULATE(
COUNT(TelcoChurn[customerID]),
TelcoChurn[Churn] = "Yes"
)
```

### Rate Metrics

```DAX
Churn Rate % =
DIVIDE([Total Churned Customers], [Total Customers], 0)

Retention Rate % =
1 - [Churn Rate %]
```

### Financial Metrics

```DAX
Total Revenue =
SUM(TelcoChurn[TotalCharges])

Revenue Lost to Churn =
CALCULATE(
SUM(TelcoChurn[TotalCharges]),
TelcoChurn[Churn] = "Yes"
)

Average Monthly Charges =
AVERAGE(TelcoChurn[MonthlyCharges])

Average Tenure =
AVERAGE(TelcoChurn[tenure])
```

### Strategy Metrics

```DAX
Target Churn Rate = 0.15

Churn Deviation =
[Churn Rate %] - [Target Churn Rate]
```

---

## 🎨 Design Philosophy

### Theme
Modern **Dark Analytics Dashboard**

### Color Palette

| Element | Color |
|------|------|
| Background | #0b1e34 |
| Card Containers | #1b3148 |
| Churn Accent | #ff8c42 |
| Retained Accent | #42a5f5 |

### Interactivity

- Global **Tile Style Slicers**
- **Cross-filtering enabled across visuals**
- Interactive **drill-down analytics**

---

## 🚀 How to Use

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/revenue-hemorrhage-intelligence.git
```

### 2️⃣ Load Dataset

Ensure the dataset **TelcoChurn.csv** is connected in **Power BI Data Source Settings**.

### 3️⃣ Open Dashboard

Open the `.pbix` file using:

**Microsoft Power BI Desktop**

### 4️⃣ Explore Insights

Navigate through the **five dashboard pages** to analyze:

- Customer churn patterns
- Revenue leakage
- Risk segmentation
- Retention opportunities

---

## 👨‍💻 Author

**K. Avinash**  
B.Tech – Artificial Intelligence and Data Science  
Vasireddy Venkatadri Institute of Technology  

📅 March 2025  



---
