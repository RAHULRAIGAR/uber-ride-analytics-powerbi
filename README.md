# 🚗 Uber Ride Analytics Dashboard

> An interactive Power BI analytics project that transforms Uber ride data into actionable insights across **trip performance, revenue, cancellations, vehicle types, cities, payment methods, and demand patterns**.

---

## 📌 Project Overview

This project analyzes **12,000 Uber ride records** using Power BI to understand operational performance, revenue contribution, customer behavior, and ride-demand patterns.

The objective is not just to visualize data, but to identify **measurable business insights and actionable recommendations** that can support better operational and revenue decisions.

---

## 🎯 Business Objective

The analysis focuses on answering key business questions:

- How many trips were completed successfully?
- What is the overall cancellation rate?
- Which cities generate the most revenue?
- Which vehicle type has the highest trip volume?
- Which vehicle type has the highest cancellation rate?
- When is ride demand at its peak?
- Which payment method is most preferred?
- Where are the major opportunities for operational improvement?

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power BI** | Dashboard development and data visualization |
| **DAX** | KPI calculations and analytical measures |
| **Power Query** | Data cleaning and transformation |
| **Excel** | Raw data source |
| **Data Modeling** | Structuring data for analysis |

---

# 📊 Dashboard Preview

## 1️⃣ Executive Overview

The Executive Overview provides a high-level view of overall ride and revenue performance.

### Key KPIs

| KPI | Result |
|-----|-------:|
| 🚕 Total Trips | **12,000** |
| ✅ Completed Trips | **10,297** |
| ❌ Cancelled Trips | **1,703** |
| 💰 Net Revenue | **₹23.54 Lakh** |
| 💵 Average Fare | **₹239.93** |
| ⚠️ Cancellation Rate | **14.19%** |

### Dashboard

![Executive Overview](Executive%20Overview.png)

---

## 2️⃣ Trip Analysis

This page focuses on trip behavior, cancellation patterns, payment preferences, and demand by hour.

### Analysis Includes

- Trip status distribution
- Hourly trip demand
- Payment method usage
- Cancellation rate by vehicle type
- Average trip distance
- Operational demand patterns

### Dashboard

![Trip Analysis](Trip%20Analysis.png)

---

## 3️⃣ Vehicle & Revenue Analysis

This page evaluates vehicle-level performance and revenue patterns.

### Analysis Includes

- Trips by vehicle type
- Cancellation rate by vehicle type
- Average fare
- Average trip distance
- City-wise revenue
- Monthly revenue trends

### Dashboard

![Vehicle & Revenue Analysis](Vehicle%20%26%20Reveue%20Analysis.png)

---

# 🔍 Key Business Insights

The analysis of the 12,000 ride records produced the following measurable insights:

### 🚕 1. Cancellation Opportunity

A total of **1,703 trips were cancelled**, resulting in an overall cancellation rate of **14.19%**.

- Rider cancellations: **1,009**
- Driver cancellations: **694**

**Business Insight:**  
The cancellation rate represents a significant opportunity to improve successful trip completion and customer experience.

---

### 🏙️ 2. Revenue Concentration

The top three revenue-generating cities are:

| City | Net Revenue |
|------|------------:|
| 🥇 Jaipur | **₹3.64 Lakh** |
| 🥈 Bengaluru | **₹3.61 Lakh** |
| 🥉 Delhi | **₹3.61 Lakh** |

Together, these three cities contribute approximately **46.10% of total net revenue**.

**Business Insight:**  
Revenue is significantly concentrated in these three markets, making them important cities for operational and growth strategies.

---

### 🚗 3. Vehicle Performance

**Uber Go** has the highest trip volume with **4,076 trips**.

However, **Uber XL** has the highest cancellation rate at **16.04%**.

**Business Insight:**  
Uber XL requires further investigation into vehicle-specific cancellation drivers, while Uber Go represents the strongest source of ride volume.

---

### ⏰ 4. Peak Demand

The highest number of trips occurs at **7 PM**, with **1,098 trips**.

**Business Insight:**  
Evening demand is a critical operational period where maintaining sufficient driver availability can help improve ride fulfillment.

---

### 💳 5. Payment Preference

**UPI** is the most frequently used payment method with **5,436 trips**, representing approximately **45.30%** of all trips.

**Business Insight:**  
Digital payment adoption is strong, creating an opportunity to use UPI-focused offers and incentives to improve customer engagement.

---

# 💡 Business Recommendations

Based on the findings, the following recommendations can be considered:

### 1. Reduce Cancellations

Investigate the causes behind the **14.19% cancellation rate**, especially for vehicle categories with higher cancellation levels.

**Expected Impact:**  
Higher trip completion and improved customer experience.

---

### 2. Improve Uber XL Operations

Uber XL has the highest cancellation rate at **16.04%**.

Investigating driver availability, wait times, trip acceptance, and operational issues for this category could help reduce cancellations.

**Expected Impact:**  
Improved vehicle utilization and trip completion.

---

### 3. Prioritize High-Revenue Cities

Jaipur, Bengaluru, and Delhi together generate **46.10% of total net revenue**.

**Expected Action:**  
Prioritize operational resources, driver availability, and targeted campaigns in these markets.

**Expected Impact:**  
Better resource allocation and stronger revenue performance.

---

### 4. Optimize Peak-Hour Driver Availability

Since **7 PM records the highest trip volume with 1,098 trips**, driver availability should be closely monitored during this period.

**Expected Impact:**  
Better demand fulfillment and reduced waiting/cancellation opportunities.

---

### 5. Leverage UPI Adoption

UPI accounts for **45.30% of all trips**.

**Expected Action:**  
Explore UPI-based promotions, cashback campaigns, or loyalty incentives.

**Expected Impact:**  
Higher digital-payment engagement and customer retention opportunities.

---

# 📈 Business Impact

This project demonstrates how raw ride data can be converted into **measurable business intelligence**.

### Key outcomes identified:

- **1,703 cancelled trips** were identified as an operational improvement opportunity.
- **14.19% cancellation rate** highlights the need for better trip completion.
- **Top 3 cities contribute 46.10% of net revenue**, highlighting revenue concentration.
- **Uber XL was flagged with the highest cancellation rate of 16.04%**.
- **7 PM was identified as the peak demand hour with 1,098 trips**.
- **UPI was identified as the dominant payment method with 45.30% usage**.
- **Uber Go was identified as the highest-volume vehicle type with 4,076 trips**.

> **The analysis goes beyond reporting what happened — it identifies where the business can take action.**

---

# 📊 KPI Summary

| Metric | Value |
|--------|------:|
| Total Trips | **12,000** |
| Completed Trips | **10,297** |
| Cancelled Trips | **1,703** |
| Cancellation Rate | **14.19%** |
| Net Revenue | **₹23.54 Lakh** |
| Average Fare | **₹239.93** |
| Top Revenue City | **Jaipur** |
| Top 3 City Revenue Share | **46.10%** |
| Highest Volume Vehicle | **Uber Go – 4,076 trips** |
| Highest Cancellation Vehicle | **Uber XL – 16.04%** |
| Peak Hour | **7 PM – 1,098 trips** |
| Most Used Payment | **UPI – 45.30%** |

---

# 📐 Key DAX Measures

### Total Trips

```dax
Total Trips = COUNT(Raw_Data[Trip_ID])
---
Total Revenue = SUM(Raw_Data[Net_Revenue])
---
Completed Trips =
CALCULATE(
    COUNT(Raw_Data[Trip_ID]),
    Raw_Data[Status] = "Completed"
)
---
Cancellation Rate =
DIVIDE(
    CALCULATE(
        COUNT(Raw_Data[Trip_ID]),
        Raw_Data[Status] <> "Completed"
    ),
    [Total Trips],
    0
)
---
Average Fare = AVERAGE(Raw_Data[Fare])
---
🚀 Skills Demonstrated
Power BI Dashboard Development
DAX
Power Query
Data Cleaning & Transformation
Data Modeling
KPI Development
Data Visualization
Exploratory Data Analysis
Business Intelligence
Business Insight Generation
Data-Driven Decision Making
---
```
👨‍💻 Author
Rahul Raigar

Aspiring Data Analyst | Computer Science & Engineering Student

🔗 **LinkedIn:** [Rahul Raigar](https://www.linkedin.com/in/rahul-raigar-data3293/)

📧 Email: rahulraigar13@gmail.com
---
⭐ If you found this project useful

Feel free to star ⭐ the repository and explore the dashboard.
---

Built with Power BI | Turning raw data into actionable business insights.
