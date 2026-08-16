# 🚗 Uber Ride Analytics Dashboard

An interactive and comprehensive **Power BI Data Analytics Project** designed to analyze ride-hailing performance, revenue trends, trip statuses, and vehicle metrics.

---

## 🛠 Tools & Technologies Used

* **Power BI Desktop**: Core tool used for building interactive dashboards and custom visuals.
* **DAX**: Calculated dynamic KPI metrics such as Total Revenue, Cancellation Rate, and Average Fare.
* **Power Query**: Data cleaning, schema transformation, and custom column generation.

---

## 🖼 Dashboard Screenshots

![Executive Overview](Executive%20Overview.png)
![Trip Analysis](Trip%20Analysis.png)
![Vehicle Analysis](Vehicle%20%26%20Reveue%20Analysis.png)

---

## 📐 Key Calculated DAX Formulas

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
'''

👨‍💻 Author
Developed by Rahul Kumar

Aspiring Data Analyst / Computer Science & Engineering Student

LinkedIn: Rahul Raigar 
Email: rahulraigar13@gmail.com
* <b>LinkedIn:</b> <a href="https://www.linkedin.com/in/rahul-raigar-data3293/">Rahul Raigar</a>
* <b>Email:</b> <a href="mailto:rahulraigar13@gmail.com">rahulraigar13@gmail.com</a>
