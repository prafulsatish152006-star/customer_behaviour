# customer_behaviour
# End-to-End Retail & Customer Behavior Analytics Pipeline

A professional, corporate-level data analytics project tracking retail consumer decisions, optimizing loyalty engagement, and mapping store operations using an end-to-end modern data stack.

---

## 📌 Project Overview
This project simulates a production-grade data analytics lifecycle. Raw, unstructured retail transaction logs are ingested, cleaned using Python pipelines, pushed to relational databases for structured analytical querying, and ultimately translated into highly interactive visual dashboards. The insights derived specifically target operational efficiency, revenue leakage protection, and automated customer lifetime value (LTV) segmentation.

## 📊 The Dataset
The project utilizes a comprehensive **Customer Shopping Behavior Dataset**. Each record represents an individual customer transaction capturing the complete consumer profile:
* **Demographics:** Customer ID, Age, Gender, Location.
* **Transaction Details:** Item Purchased, Category, Purchase Amount (USD), Season, Payment Method.
* **Loyalty & Behavior Metrics:** Review Rating, Subscription Status, Shipping Type, Discount Applied, Previous Purchases, and Purchase Frequency.

## 🛠️ Tools & Tech Stack
* **Data Ingestion & Engineering:** Python (Jupyter Notebook, Pandas)
* **Relational Database Architecture:** SQL (PostgreSQL / MySQL / MS SQL Server)
* **Business Intelligence & Visualization:** Power BI
* **Executive Delivery:** Gamma AI (Automated Presentation Deck)

---

## 🚀 Execution Steps & Architecture

### Step 1: Python Data Engineering & EDA
* Loaded raw transactional data into **Jupyter Notebook** using Pandas dataframes.
* Handled missing metrics cleanly via structured, category-specific median imputation rather than basic global averages to prevent data bias.
* Refactored unorganized column layouts into clean, production-standard `snake_case` styling.
* Feature engineered text-based behavior data (e.g., converting text-based frequencies into explicit numeric day cycles).

### Step 2: Database Migration & SQL Analytics
* Built a custom `SQLAlchemy` and `psycopg2` pipeline to load the sanitized Python data frames directly into the relational database.
* Executed advanced business logic queries using complex metrics including `CASE WHEN` conditional statements for loyalty tier mapping, aggregations for revenue tracking, and `ROW_NUMBER()` window functions to rank category trends.

### Step 3: Interactive BI Dashboard Design
* Connected the relational database instances seamlessly into **Power BI Desktop**.
* Constructed custom KPI metrics, high-impact card indicators, and interactive filtering slicers.
* Formatted the user interface with distinct focus on visual aesthetics (drop shadows, rounded edges, targeted color typography) to deliver clean, presentation-ready dashboard layouts.

### Step 4: Documentation & Presentation
* Compiled a formal internal technical report detailing pipeline logic boundaries.
* Ported data documentation into **Gamma AI** to auto-generate a sleek, client-ready presentation deck exported as PDF for stakeholder review.

---

## 📉 Dashboard Preview & Metrics
*(Replace the placeholder below with a high-resolution screenshot of your actual Power BI layout!)*

![Power BI Dashboard Layout](Dashboards/your_dashboard_screenshot.png)

### Core Interactive Views Available:
1. **Revenue vs. Volume Matrix:** Dynamically tracks total spend profiles against categorical shopping volumes.
2. **Subscription Conversion Slicer:** Segments behavior layouts between loyalty members and non-members instantly.
3. **Demographic Performance Map:** Automatically tracks seasonal purchasing volume filtered by customer age brackets and gender splits.

---

## 💡 Key Business Results & Insights
* **Loyalty Disconnect:** Analytics isolated that a large percentage of repeat buyers are not yet part of the brand’s premium subscription model—highlighting a massive opportunity for targeted re-engagement marketing campaigns.
* **High-Margin Targets:** Young adults and middle-aged demographics generate the peak share of overall revenue, identifying exactly where marketing spend should be focused.
* **Premium Delivery Drivers:** Transactions using premium express shipping variants maintain a noticeably higher average cart valuation than baseline standard shipping profiles.

---

## 💻 How To Run This Project

### 1. Run the Python Pipeline
Ensure you have Jupyter and Pandas installed, then run the notebook to clean the raw data and export it:
```bash
pip install pandas sqlalchemy psycopg2
jupyter notebook Code/your_notebook_name.ipynb
