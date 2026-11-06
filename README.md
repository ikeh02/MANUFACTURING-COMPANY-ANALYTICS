# MANUFACTURING-COMPANY-ANALYTICS
An operational data analytics project tracking manufacturing line productivity, operator efficiency, and downtime root-cause metrics using Excel Pivot Tables, time-duration modeling, and interactive visual dashboards.
# 🏭 Manufacturing Analytics & Line Productivity Dashboard

An operational analytics project built in Microsoft Excel to evaluate manufacturing batch efficiency, operator performance, and root-cause downtime drivers for plant operations.

---

## 📊 Executive Summary

This project analyzes production batch performance across 38 operational runs (totaling 3,858 work minutes) to identify productivity bottlenecks, evaluate operator line efficiency, and map operational downtime factors.

### 🎯 Key Performance Metrics
* **Total Batches Processed:** 38 Batches
* **Total Production Duration:** 3,858 Minutes (~64.3 Hours)
* **Average Line Efficiency Rate:** ~67.1%
* **Top Downtime Driver:** Machine Adjustments (332 Minutes)

---

## 🔍 Core Analytical Components

### 1. Line Productivity & Operator Efficiency
Analyzes individual operator throughput against standard minimum batch runtimes (60 minutes per batch for 600ml products):
* **Operators Evaluated:** Charlie, Dee, Dennis, Mac
* **Metrics Calculated:** Work Duration ($\text{End Time} - \text{Start Time}$), Target Batch Time, and Line Efficiency Index ($\frac{\text{Target Time}}{\text{Actual Duration}}$).

### 2. Downtime Root-Cause Analysis (Pareto Breakdown)
Classifies and quantifies operational interruptions to separate equipment adjustments from operator errors:

| Downtime Factor | Total Lost Time (Mins) | Primary Classification |
| :--- | :---: | :--- |
| **Machine Adjustment** | 332 | Mechanical / Setup |
| **Machine Failure** | 254 | Equipment Breakdown |
| **Inventory Shortage** | 225 | Supply Chain Delay |
| **Batch Change** | 160 | Changeover / Setup |
| **Batch Coding Error** | 145 | Operator / Quality Control |
| **Other / Minor Stoppages** | 272 | Miscellaneous |

---

## 🛠️ Data Architecture & File Structure

```text
├── Machala manucfacturing coy analytics.xlsx
│   ├── Line productivity           # Raw batch start/end timestamp logs
│   ├── Products                    # Product master table (Flavor, Size, Min Batch Time)
│   ├── Downtime factors            # Master lookup table for downtime categories
│   ├── Line downtime               # Matrix tracking downtime minutes per batch factor
│   ├── pivottable                  # Summary aggregations of efficiency & downtime
│   └── dashboard                   # Executive visual KPI canvas
└── Screenshots/
    └── dashboard_preview.png       # High-resolution dashboard screenshot
