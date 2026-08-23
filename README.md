# 🚗 Uber Ride Analytics Dashboard

> An interactive Power BI analytics project designed to analyze **ride performance, revenue trends, trip status, cancellation behavior, vehicle performance, payment preferences, and operational demand patterns**.

---

## 📌 Project Overview

This project analyzes Uber ride data using **Power BI** to transform raw trip-level data into meaningful business insights.

The dashboard provides an interactive view of:

- 🚕 Overall ride performance
- 💰 Revenue and fare analysis
- 📊 Trip completion and cancellation behavior
- 🚗 Vehicle-type performance
- 🏙️ City-wise revenue contribution
- 💳 Payment method preferences
- ⏰ Hourly ride demand
- 📅 Monthly revenue trends
- 📍 Average trip distance

The goal is not only to visualize data, but also to identify **actionable business insights that can support operational and revenue-related decisions**.

---

## 🎯 Business Objective

The primary objective of this project is to answer important business questions such as:

- How many trips were completed successfully?
- What is the overall cancellation rate?
- Which cities contribute the most revenue?
- Which vehicle types generate the highest trip volume?
- Which payment methods are most commonly used?
- During which hours is ride demand highest?
- How does revenue change month by month?
- How does cancellation behavior vary across vehicle types?
- What vehicle types and operational areas require greater attention?

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power BI** | Interactive dashboard development and data visualization |
| **DAX** | KPI calculations and analytical measures |
| **Power Query** | Data cleaning, transformation, and preparation |
| **Data Modeling** | Organizing data for efficient analysis |

---

# 📊 Dashboard Overview

The dashboard consists of **three analytical pages**, each focused on a different business perspective.

---

## 1️⃣ Executive Overview

The Executive Overview provides a high-level summary of Uber's ride and revenue performance.

### Key KPIs

- **Total Trips:** 12K
- **Completed Trips:** 10K
- **Total Revenue:** ₹2M
- **Average Fare:** ₹240
- **Cancellation Rate:** 14.2%

### Business Questions Answered

- What is the overall ride performance?
- How much revenue was generated?
- What percentage of trips were cancelled?
- Which cities contribute strongly to revenue?
- How does revenue vary month by month?

### Dashboard Preview

![Executive Overview](Executive%20Overview.png)

---

## 2️⃣ Trip Analysis

The Trip Analysis page focuses on customer trip behavior and operational patterns.

### Analysis Includes

- Trip status distribution
- Trips by hour
- Payment method distribution
- Cancellation rate by vehicle type
- Average trip distance by vehicle type

### Business Questions Answered

- When is ride demand highest?
- What percentage of trips are completed or cancelled?
- Which payment method is most frequently used?
- Which vehicle types have relatively higher cancellation rates?
- How does average trip distance vary across vehicle types?

### Dashboard Preview

![Trip Analysis](Trip%20Analysis.png)

---

## 3️⃣ Vehicle & Revenue Analysis

This page evaluates vehicle-level performance and revenue contribution.

### Analysis Includes

- Total trips by vehicle type
- Cancellation rate by vehicle type
- Average fare by vehicle type
- Average trip distance by vehicle type
- Total trips vs. total revenue
- Monthly revenue trend

### Business Questions Answered

- Which vehicle type generates the highest trip volume?
- Which vehicle types have higher cancellation rates?
- Which vehicle types generate higher average fares?
- How does revenue contribution vary across vehicle types?
- How does revenue change throughout the year?

### Dashboard Preview

![Vehicle & Revenue Analysis](Vehicle%20%26%20Reveue%20Analysis.png)

---

# 🔍 Key Business Insights

Based on the dashboard analysis, the following insights were identified:

### 🚕 Ride Performance

- The dataset contains approximately **12K total trips**, out of which around **10K trips were completed**.
- The overall **cancellation rate is 14.2%**, highlighting an opportunity to improve successful ride completion.
- Completed trips represent the majority of overall ride activity.

### 💰 Revenue Performance

- Total revenue generated is approximately **₹2M**.
- The average fare per trip is approximately **₹240**.
- Revenue remains relatively consistent across most months, with visible fluctuations throughout the year.
- City-level analysis highlights **Jaipur, Bengaluru, and Delhi** among the stronger revenue-contributing cities.

### 🚗 Vehicle Performance

- **Uber Go** records the highest trip volume among the displayed vehicle categories.
- Vehicle categories show different cancellation-rate patterns.
- **Uber XL** shows the highest cancellation rate among the vehicle types displayed in the analysis.
- Average fares vary across vehicle categories, with premium vehicle categories generally showing higher average fares.

### 💳 Payment Behavior

- **UPI** is the most frequently used payment method in the analyzed dataset.
- Card and Cash also represent significant portions of total trips, while Wallet contributes a smaller share.

### ⏰ Demand Pattern

- Ride demand varies significantly throughout the day.
- The dashboard indicates stronger ride activity during the **evening hours**, suggesting a need for effective driver availability during peak periods.

---

# 💡 Business Recommendations

Based on the identified patterns, the following actions could help improve operational performance:

### 1. Reduce Trip Cancellations

Investigate the major causes of cancellations, particularly for vehicle categories with relatively higher cancellation rates.

**Potential business benefit:** Improved trip completion and better customer experience.

### 2. Optimize Peak-Hour Driver Availability

Increase driver availability during high-demand evening hours.

**Potential business benefit:** Better ride fulfillment and reduced demand-supply gaps.

### 3. Focus on High-Revenue Cities

Monitor and prioritize cities contributing strongly to overall revenue.

**Potential business benefit:** Better allocation of operational and marketing resources.

### 4. Optimize Vehicle Allocation

Use trip volume, cancellation rate, fare, and distance patterns to optimize the availability of different vehicle categories.

**Potential business benefit:** Better utilization of vehicles and improved operational efficiency.

### 5. Leverage Digital Payment Adoption

Since UPI represents the largest share of payment usage, targeted digital-payment campaigns could be explored to improve customer engagement.

**Potential business benefit:** Increased adoption of convenient digital payment methods.

---

# 📈 Business Impact

This project transforms raw ride-level data into **actionable business intelligence**.

The analysis helps stakeholders understand:

- 📊 Overall ride performance
- 💰 Revenue contribution
- 🚕 Trip completion and cancellation behavior
- 🚗 Vehicle-level performance
- 🏙️ City-level revenue patterns
- 💳 Customer payment preferences
- ⏰ Peak demand periods

These insights can support better decisions related to **driver allocation, cancellation reduction, operational planning, customer experience, and revenue optimization**.

> **The key focus of this project is not just "what happened", but also "what the business can do about it."**

---

# 📐 Key DAX Measures

### Total Trips

```dax
Total Trips = COUNT(Raw_Data[Trip_ID])
---
Total Revenue = SUM(Raw_Data[Revenue])
---
Cancellation Rate =
DIVIDE(
    CALCULATE(
        COUNT(Raw_Data[Trip_ID]),
        Raw_Data[Trip_Status] IN {
            "Cancelled by Rider",
            "Cancelled by Driver"
        }
    ),
    [Total Trips],
    0
)
---
Average Fare = AVERAGE(Raw_Data[Fare_Amount])
---
| KPI                  |     Value |
| -------------------- | --------: |
| 🚕 Total Trips       |   **12K** |
| ✅ Completed Trips    |   **10K** |
| 💰 Total Revenue     |   **₹2M** |
| 💵 Average Fare      |  **₹240** |
| ⚠️ Cancellation Rate | **14.2%** |
---
🚀 Skills Demonstrated

Through this project, I demonstrated practical skills in:

Power BI Dashboard Development
Data Cleaning & Transformation
Power Query
DAX
KPI Development
Data Visualization
Business Intelligence
Exploratory Data Analysis
Business Insight Generation
Data-Driven Decision Making
---
```

👨‍💻 Author
Rahul Kumar

Aspiring Data Analyst | Computer Science & Engineering Student

🔗**LinkedIn:** [Rahul Raigar](https://www.linkedin.com/in/rahul-raigar-data3293/)
📧 Email: rahulraigar13@gmail.com
---
⭐ If you found this project useful

Feel free to star ⭐ the repository and explore the dashboard.

Built with Power BI | Focused on turning data into actionable business insights.
