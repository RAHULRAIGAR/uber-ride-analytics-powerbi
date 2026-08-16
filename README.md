# 🚗 Uber Ride Analytics Dashboard

An interactive and comprehensive **Power BI Data Analytics Project** designed to analyze ride-hailing performance, revenue trends, trip statuses, and vehicle metrics. This project translates raw trip data into strategic business insights to optimize driver utilization, reduce cancellation rates, and maximize revenue.

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Key Features & Pages](#-key-features--pages)
- [Tools & Technologies Used](#-tools--technologies-used)
- [Key Business Insights & Metrics](#-key-business-insights--metrics)
- [Data Model & Transformations](#-data-model--transformations)
- [Dashboard Screenshots](#-dashboard-screenshots)
- [How to Run / View](#-how-to-run--view)

---

## 📊 Project Overview

The objective of this project is to provide a multi-perspective analysis of Uber ride operations over a full year period (Jan 2025 – Dec 2025). 

The dashboard consists of three core interactive views:
1. **Executive Overview**: High-level KPIs, monthly revenue trends, and city-wise performance distribution.
2. **Trip Analysis**: Deep-dive into ride status, peak trip hours, payment mode breakdown, and cancellation distribution.
3. **Vehicle & Revenue Analysis**: Vehicle-type comparisons based on revenue, distance, average fare, and cancellation behavior.

---

## 🛠 Tools & Technologies Used

* **Power BI Desktop**: Core tool used for building interactive dashboards, custom visuals, and dynamic reports.
* **DAX (Data Analysis Expressions)**: Calculated dynamic KPI metrics such as *Total Revenue, Cancellation Rate, Average Fare, Total Completed Trips, and Distance Metrics*.
* **Power Query**: Utilized for data cleaning, type conversion, custom column generation, and schema transformation.
* **Data Modeling**: Built custom Date Table (`DateTable`) linked via relationships to the primary fact table (`Raw_Data`).
* **Excel / CSV**: Source datasets containing trip records, payment types, driver/rider statuses, and vehicle category information.

---

## 📈 Key Features & Pages

### 1️⃣ Executive Overview Page
* **KPI Cards**: Total Trips (`12K`), Completed Trips (`10K`), Total Revenue (`₹2M`), Average Fare (`₹240`), and Overall Cancellation Rate (`14.2%`).
* **Total Revenue by City**: Geographical breakdown across key cities (Jaipur, Mumbai, Hyderabad, Chennai, Pune, Kolkata).
* **Total Revenue by Month**: Monthly line chart analyzing revenue seasonality throughout the year.

### 2️⃣ Trip Analysis Page
* **Total Trips by Status**: Donut visual breaking down Completed vs. Cancelled by Rider vs. Cancelled by Driver.
* **Total Trips by Hour**: Hourly bar chart identifying peak demand windows.
* **Payment Type Distribution**: Pie visual highlighting preferences for Cash, Card, UPI, and Digital Wallet.
* **Cancellation Rate by Vehicle Type**: Bar chart comparing cancellation tendencies across Uber Auto, Uber Go, Uber Moto, Uber Premier, and Uber XL.
* **Average Distance by Vehicle Type**: Horizontal bar visual comparing trip length across vehicle classes.
  


## 🖼 Dashboard Screenshots

## 🖼 Dashboard Screenshots

![Executive Overview](Executive%20Overview.png)
![Trip Analysis](Trip%20Analysis.png)
![Vehicle Analysis](Vehicle%20%26%20Reveue%20Analysis.png)

### 3️⃣ Vehicle & Revenue Analysis Page
* **Performance by Vehicle Type**: Comparative analysis showing total volume vs. revenue generated per category.
* **Average Fare by Vehicle Type**: Detailed breakdown of pricing efficiency across vehicle classes.
* **Combined Revenue & Distance Matrix**: Tracking passenger volume trends alongside average trip length.

---

## 📐 Key Calculated DAX Formulas

Here are a few DAX expressions used in this dashboard:

```dax
// Total Trips Count
Total Trips = COUNT(Raw_Data[Trip_ID])

// Total Revenue Generated
Total Revenue = SUM(Raw_Data[Revenue])

// Cancellation Rate %
Cancellation Rate = 
DIVIDE(
    CALCULATE(COUNT(Raw_Data[Trip_ID]), Raw_Data[Trip_Status] IN {"Cancelled by Rider", "Cancelled by Driver"}),
    [Total Trips],
    0
)

// Average Fare Per Trip
Average Fare = AVERAGE(Raw_Data[Fare_Amount])


Developed by Rahul Kumar 

Aspiring Data Analyst / Computer Science & Engineering Student

Connect on LinkedIn:[https://www.linkedin.com/in/rahul-raigar-data3293/]

Email: [rahulraiger13@gmail.com]
