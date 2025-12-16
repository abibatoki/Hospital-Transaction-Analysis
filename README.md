## 🏥 Hospital Transaction Analysis
📁 Project Overview

In this project, I built an interactive Power BI dashboard using a hospital transaction dataset to give decision makers a centralised view of financial and operational performance. The goal was to move away from intuition-based decisions and instead use data to understand how much revenue is generated, where the hospital spends money, and who drives value. The dashboard summarises key performance indicators such as revenue, expenses, profit, profit margin, patient counts, and doctor performance.

---

## 🚀 Live Demo

You can explore the full dashboard here:  
🔗 **(https://app.powerbi.com/view?r=eyJrIjoiYmUwNmFmNTMtZWUzYS00MzFlLTk5YmQtMGI3NmU1M2M5ZTFhIiwidCI6IjFlNjMzNjFkLTJhODktNGMyNy04MTcwLTExNGE4MTVkZDA0ZiJ9&pageName=1fb029a0806996d8b000)**

---

## 💡 Business Objective

Hospitals operate with tight margins and complex services. Without a single source of truth, it’s hard to see which departments perform well, which procedures are profitable, or whether staffing levels align with patient demand. This project aims to:

- Provide leadership with a centralised view of revenue, expenses, and profit.

- Identify top revenue‑generating specialties and procedures to prioritise investment.

- Understand patient and doctor demographics to guide resource planning.

- Spot trends in revenue and patient visits to proactively address declines.

- Deliver recommendations for improving profitability and patient engagement.

---

## 💻 Code and Resources Used

This project was developed using **Microsoft Excel** and **Microsoft Power BI**.

- **Microsoft Excel** – used to explore the raw data, define the initial fact and dimension schema, and perform basic cleaning before importing into Power BI.

- **Power BI Desktop** – used to model the dataset, create relationships and measures, and design the interactive dashboards.

**Data:**

`Hospital Transactions Data.xlsx` – transaction records from a fictional hospital, including date, revenue and expense amounts, doctor and patient attributes, procedure and category details, and location information.

---

## 🗃 Dataset Description

The primary sheet of the dataset contains 230 transactions with 28 columns, covering financial figures, medical procedure details, and demographic information:

- **Financial:** `RevenueAmount`, `ExpensesAmount` – numeric fields capturing revenue generated and costs incurred per procedure.

- **Doctor:** `Doctors_FirstName`, `Doctors_LastName`, `Doctor_Gender`, `DoctorID`, and contact information.

- **Patient:** `Patients_FirstName`, `Patients_LastName`, `Patients_Gender`, `PatientID`, and contact details.

- **Procedure:** `ProcedureName`, `Category`, `Description` – describing the service performed (e.g., Skin Biopsy, Pediatric Vaccination).

- **Location:** `Country`, `State`, `City`, `PostalCode` – indicating where the service took place.

- **Date:** `Date` – the transaction date; used to derive reporting periods (year and quarter).

A secondary sheet outlines the fact and dimension tables for a star-schema model that powers the dashboard.

---

## 🧹 Data Cleaning & Preparation

Before creating the dashboard, I prepared the data using these steps:

- **Date conversion:** Parsed the Date column into a proper datetime type and derived Year and Quarter for time-series analysis.

- **Computed metrics:** Created a Profit column (RevenueAmount - ExpensesAmount) and a ProfitMargin field (profit/revenue) to assess procedure profitability.

- **Handled missing values:** Checked for and addressed nulls in key fields (replacing or removing as appropriate) and ensured numeric types for monetary fields.

- **Removed duplicates:** Verified that each TransactionID is unique to avoid double-counting.

- **Standardised categories:** Normalised values in Specialty, Category, and Location columns for consistent grouping.

---

## 📊 Analysis & Insights

After cleaning the data, I explored key metrics and built visualisations. Highlights include:

- **Financial performance:** Total revenue was **$274,000** and total expenses **$189,000**, resulting in **$84,000** profit and a **30.8 % profit margin**. The hospital employs **81 doctors** and serves **86 patients.**

- **Revenue trend:** Revenue climbed steadily during 2021 and 2022, peaking at $44 K in Q4 2022, but declined sharply in 2023 as patient visits fell. This suggests the need for patient retention strategies.

- **Top specialties:** Dermatology ($68 K), Cardiology ($61 K), and Neurology ($59 K) contributed the majority of revenue, while Orthopedics, Ophthalmology, and Pediatrics generated smaller shares. High‑margin procedures such as **Skin Biopsy** and **Pediatric Vaccination** delivered the largest profits.

- **Doctor & patient insights:** Five doctors (Ava Adams, Liam Turner, Benjamin Hill, Emma Wright, and William Carter) generated over half of the revenue. A small group of patients (Harper Young, Ethan Lopez, Mia Wilson, Mia Adams, and Olivia Anderson) also contributed disproportionately. Gender distribution is balanced, 39 female and 42 male doctors; 47 female and 39 male patients.

- **Specialty staffing:** Each specialty served only seven patients but employed 11–15 doctors, implying potential over‑staffing or underutilisation of physicians.

- **Patient visit trend:** Visits were flat in 2021, surged in 2022, and then fell to single digits by Q3 2023. Monitoring and counteracting this decline is critical.

---

## 🖥️ Power BI Dashboard

An interactive dashboard consolidates the analysis into a single view:

<img width="1700" height="1125" alt="image" src="https://github.com/user-attachments/assets/ac71667f-ce94-4180-9f7e-e7e618c0a348" />

**Revenue dashboard:** Displays total revenue, expenses, profit, and profit margin with cards and gauges. It includes a line chart showing revenue by quarter, bar charts summarising revenue by specialty and category, and a table of procedures with revenue, expenses, profit, and transaction counts.

<img width="1700" height="1125" alt="image" src="https://github.com/user-attachments/assets/14b08389-206e-402f-adaa-baee2d081eee" />

**Performance dashboard:** Highlights top doctors and patients by revenue, shows the number of doctors and patients by gender, and compares patient and doctor counts across specialties. A line chart tracks patient visits over time.

---

## ✅ Conclusion & Recommendations

The analysis reveals that while City Hospital maintains a healthy profit margin, revenue and patient visits dropped sharply in 2023. To sustain growth, I recommend the following:

- **Boost patient engagement:** Launch targeted outreach campaigns, tele‑health services and loyalty programs to re‑engage dormant patients and attract new ones.

- **Focus on high‑profit services:** Increase capacity and marketing for high‑earning specialties (Dermatology, Cardiology, Neurology) and high‑margin procedures (Skin Biopsy, Pediatric Vaccination).

- **Optimise staffing:** Assess doctor schedules and redistribute physicians to match patient demand; cross‑train doctors to minimise idle time.

- **Monitor trends:** Continue tracking revenue and patient visits quarterly to detect changes early and adjust strategies accordingly.

- **Enhance data quality:** Maintain a robust data model, clean data regularly, and expand metrics (e.g., patient satisfaction) for deeper insights.

By following these recommendations, the hospital can leverage its data to improve financial performance, patient care, and strategic planning.
