# Sales Performance & Operational Analytics — Excel MIS Dashboard

## 📊 Project Overview
This project demonstrates an end-to-end Management Information System (MIS) data pipeline built entirely within Microsoft Excel. The project converts raw, unorganized flat-file transactional rows into a dynamic, single-page executive decision support tool tracking ₹17,988.66 in total revenue metrics.

## 🔄 Data Transformation: From Raw Rows to Executive Insights

### 1. The Input (Raw Transactional Data)
The project initiated with a raw dataset containing transactional fields across Order Dates, Geographic Regions, Categories, Unit Quantities, and individual Sales Rep allocations.
![Raw Transactional Sales Data](raw_data_view.png)

### 2. The Output (Interactive Dashboard Engine)
Using conditional formatting, dynamic Pivot Tables, and strict layout architecture, those rows were compressed into a clean, gridline-free executive canvas with automated visual data models.
![Polished Corporate Dashboard View](dashboard_view.png)

---

## 🛠️ Technical Workflow & Implementation Details

### 1. Data Ingestion & Feature Engineering
* Converted the initial structural range ($A1$ to $I23$) into an official **Excel Table with Headers** to protect database integrity and enable dynamic range expansion.
* Engineered a temporal data dimension in column B using the text parsing formula:
  ```excel
  =TEXT(A2, "mmm")
