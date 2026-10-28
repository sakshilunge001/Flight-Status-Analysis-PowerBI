# ✈️ Flight Status Analysis Dashboard | Power BI

## 📌 Project Overview

This project showcases an interactive **Flight Status Analysis Dashboard** developed in **Power BI** using the **Flight Delays dataset from Maven Analytics**. The dashboard provides comprehensive insights into airline performance, flight operations, delays, cancellations, and overall flight status through interactive visualizations and KPI tracking.

The objective of this project was to transform raw flight data into actionable business insights, enabling users to monitor operational efficiency and identify patterns affecting flight performance.

---

## 📂 Dataset

- **Dataset Name:** Flight Delays Dataset
- **Source:** Maven Analytics
- **Tool:** Power BI Desktop

---

## 🎯 Business Requirements

This dashboard answers the following business questions:

- How does the overall flight volume vary by month and day of the week?
- What percentage of flights experienced departure delays in 2015?
- What was the average delay time for delayed flights?
- How does the percentage of delayed flights vary throughout the year?
- How does delay performance differ for flights departing from Boston (BOS)?
- How many flights were cancelled in 2015?
- What percentage of cancellations were caused by Weather, Airline/Carrier, and National Air System?
- Which airlines are the most and least reliable based on on-time departures?

---

# 📊 Dashboard KPIs

The dashboard includes the following Key Performance Indicators:

- ✈️ Total Flights
- ✅ On-Time Flights
- ⚠️ Delayed Flights
- ❌ Cancelled Flights
- 📈 On-Time %
- 📉 Delayed %
- 🚫 Cancelled %

---

# 📈 Dashboard Visualizations

- Total Flights KPI Card
- Delayed Flights KPI Card
- Cancelled Flights KPI Card
- Flight Status Distribution
- Top Airports by Flight Volume
- Airline Delay Percentage Analysis
- Cancellation Reason Analysis
- Monthly Delay Trend
- Flight Volume Analysis

---

# 🛠️ Tools & Technologies

- Power BI Desktop
- Power Query
- DAX
- Data Modeling
- Data Visualization

---

# 📐 DAX Measures Used

### Total Flights

```DAX
Total Flights =
COUNTROWS(Flights)
```

### On-Time Flights

```DAX
On Time Flights =
CALCULATE(
    COUNTROWS(Flights),
    Flights[Flight Status] = "On Time"
)
```

### Delayed Flights

```DAX
Delayed Flights =
CALCULATE(
    COUNTROWS(Flights),
    Flights[Flight Status] = "Delayed"
)
```

### Cancelled Flights

```DAX
Cancelled Flights =
CALCULATE(
    COUNTROWS(Flights),
    Flights[Flight Status] = "Cancelled"
)
```

### On-Time %

```DAX
On Time % =
DIVIDE(
    [On Time Flights],
    [Total Flights],
    0
)
```

### Delayed %

```DAX
Delayed % =
DIVIDE(
    [Delayed Flights],
    [Total Flights],
    0
)
```

### Cancelled %

```DAX
Cancelled % =
DIVIDE(
    [Cancelled Flights],
    [Total Flights],
    0
)
```

---

# 📊 Key Insights

- Analyzed nearly **1.9 million** flight records to evaluate airline operational performance.
- Identified the busiest airports based on total flight volume.
- Compared airline reliability by analyzing delayed flight percentages.
- Measured overall operational performance using On-Time, Delayed, and Cancelled flight KPIs.
- Determined that weather and airline-related issues were the primary contributors to flight cancellations.
- Identified monthly and seasonal delay patterns to better understand operational bottlenecks.

---

# 📁 Repository Structure

```text
Flight-Status-Analysis-PowerBI
│
├── README.md
├── Flight_Status_Analysis.pbix
├── Flights.csv
├── dashboard.png
└── LICENSE
```

---


# 🎯 Learning Outcomes

This project helped strengthen my skills in:

- Power BI Dashboard Development
- Power Query for Data Transformation
- DAX Measure Creation
- Data Modeling
- KPI Design
- Business Intelligence Reporting
- Interactive Dashboard Development
- Data Storytelling




