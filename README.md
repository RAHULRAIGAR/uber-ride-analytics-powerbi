# 🚗 Uber Ride Analytics Dashboard

> An interactive Power BI dashboard that transforms Uber ride data into actionable business insights across trip performance, revenue, cancellations, vehicle types, cities, payment methods, and demand patterns.

---

## 📌 Project Overview

This project analyzes **12,000 Uber ride records** using Power BI to understand operational performance, revenue contribution, cancellation behavior, customer payment preferences, and ride-demand patterns.

The goal is to move beyond visualization and identify **measurable business outcomes and actionable recommendations**.

---

## 🎯 Business Objectives

- Analyze completed and cancelled trips
- Measure overall cancellation rate
- Identify high-revenue cities
- Compare vehicle-type performance
- Identify peak demand periods
- Analyze customer payment preferences
- Identify opportunities for operational improvement

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Power BI** | Dashboard development & visualization |
| **DAX** | KPI calculations & analytical measures |
| **Power Query** | Data cleaning & transformation |
| **Excel** | Raw data source |
| **Data Modeling** | Structuring data for analysis |

---

# 📊 Dashboard Preview

## 1️⃣ Executive Overview

Provides a high-level view of ride performance, revenue, cancellations, and key operational KPIs.

| KPI | Result |
|---|---:|
| 🚕 Total Trips | **12,000** |
| ✅ Completed Trips | **10,297** |
| ❌ Cancelled Trips | **1,703** |
| 💰 Net Revenue | **₹23.54 Lakh** |
| 💵 Average Fare | **₹239.93** |
| ⚠️ Cancellation Rate | **14.19%** |

![Executive Overview](Executive%20Overview.png)

---

## 2️⃣ Trip Analysis

Analyzes trip behavior, cancellation patterns, payment preferences, and demand.

**Key Analysis:**
- Trip status distribution
- Hourly trip demand
- Payment method usage
- Cancellation rate by vehicle type
- Average trip distance

![Trip Analysis](Trip%20Analysis.png)

---

## 3️⃣ Vehicle & Revenue Analysis

Evaluates vehicle performance and revenue trends across cities and time periods.

**Key Analysis:**
- Trips by vehicle type
- Vehicle cancellation rate
- Average fare
- Average trip distance
- City-wise revenue
- Monthly revenue trends

![Vehicle & Revenue Analysis](Vehicle%20%26%20Reveue%20Analysis.png)

---

# 🔍 Key Business Insights

### 🚕 1. Cancellation Opportunity

**1,703 trips** were cancelled, resulting in a **14.19% cancellation rate**.

- Rider cancellations: **1,009**
- Driver cancellations: **694**

**Insight:** Reducing cancellations can improve trip completion and customer experience.

---

### 🏙️ 2. Revenue Concentration

| City | Net Revenue |
|---|---:|
| 🥇 Jaipur | **₹3.64 Lakh** |
| 🥈 Bengaluru | **₹3.61 Lakh** |
| 🥉 Delhi | **₹3.61 Lakh** |

The top three cities contribute approximately **46.10% of total net revenue**.

**Insight:** These markets should receive focused operational and growth strategies.

---

### 🚗 3. Vehicle Performance

**Uber Go** has the highest trip volume with **4,076 trips**, while **Uber XL** has the highest cancellation rate at **16.04%**.

**Insight:** Uber Go represents the strongest volume driver, while Uber XL requires further investigation into cancellation drivers.

---

### ⏰ 4. Peak Demand

**7 PM** records the highest trip volume with **1,098 trips**.

**Insight:** Driver availability should be optimized during peak evening demand.

---

### 💳 5. Payment Preference

**UPI** is the most-used payment method with **5,436 trips**, representing **45.30%** of all trips.

**Insight:** UPI-focused offers and loyalty campaigns could improve customer engagement.

---

# 💡 Business Recommendations

1. **Reduce Cancellations**  
   Investigate the causes behind the **14.19% cancellation rate** and target high-cancellation vehicle categories.

2. **Improve Uber XL Operations**  
   Analyze driver availability, wait times, and acceptance behavior to reduce the **16.04% cancellation rate**.

3. **Prioritize High-Revenue Cities**  
   Focus operational resources and campaigns on **Jaipur, Bengaluru, and Delhi**.

4. **Optimize Peak-Hour Availability**  
   Increase driver availability around the **7 PM peak-demand period**.

5. **Leverage UPI Adoption**  
   Explore UPI-based promotions and loyalty incentives to increase customer engagement.

---

# 📊 KPI Summary

| Metric | Value |
|---|---:|
| Total Trips | **12,000** |
| Completed Trips | **10,297** |
| Cancelled Trips | **1,703** |
| Cancellation Rate | **14.19%** |
| Net Revenue | **₹23.54 Lakh** |
| Average Fare | **₹239.93** |
| Top Revenue City | **Jaipur** |
| Top 3 Revenue Share | **46.10%** |
| Highest Volume Vehicle | **Uber Go – 4,076 trips** |
| Highest Cancellation Vehicle | **Uber XL – 16.04%** |
| Peak Demand | **7 PM – 1,098 trips** |
| Most Used Payment | **UPI – 45.30%** |

---

# 📐 Key DAX Measures

### Total Trips

```dax
Total Trips = COUNT(Raw_Data[Trip_ID])
---Total Revenue = SUM(Raw_Data[Net_Revenue])
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
Business Intelligence
Exploratory Data Analysis
Data-Driven Decision Making
---
```
🔗 Project Links

📊 **Project:** [Uber Ride Analytics Dashboard](https://github.com/RAHULRAIGAR/uber-ride-analytics-powerbi)

📁 **GitHub Repository:** [RAHULRAIGAR/uber-ride-analytics-powerbi](https://github.com/RAHULRAIGAR/uber-ride-analytics-powerbi)
---
# 👨‍💻 Author

**Rahul Raigar**

Aspiring Data Analyst | Computer Science & Engineering Student

🔗 **LinkedIn:** [Rahul Raigar](https://www.linkedin.com/in/rahul-raigar-data3293/)

📧 **Email:** [rahulraigar13@gmail.com](mailto:rahulraigar13@gmail.com)
---
⭐ If you found this project useful, consider starring the repository.

Built with Power BI | Turning ride data into actionable business insights.
