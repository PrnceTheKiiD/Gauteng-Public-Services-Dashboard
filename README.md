# Analysis of Gauteng Citizen Services & Applications

## A Comprehensive Report on Citizen Services Rendered by Data Capturers across Gauteng Departments (Home Affairs, Municipal, Clinics, and SASSA)

---

## 📋 Project Overview & Background

This repository contains an end-to-end data analytics and business intelligence project tracking citizen applications and public services rendered across the Gauteng province. The operational workflow captures frontline service delivery data managed by government and municipal data capturers across four key public service sectors:
- **Department of Home Affairs** (Identity documents, passports, civil registrations)
- **Municipal Offices** (Utility accounts, municipal service requests, local registrations)
- **Local Clinics** (Primary healthcare consultations, patient records, immunizations)
- **SASSA / Social Services** (Social grant applications, status verifications, grant management)

The dataset simulates highly realistic government service delivery logs comprising **1,079 total records**, capturing citizen demographics, service turnaround times, departmental workflows, processing statuses, and staff performance metrics. The entire project—from data ingestion, cleaning, and transformation to advanced analytics and interactive dashboard visualization—was executed within **Microsoft Excel**.

---

## 🎯 Project Objectives

The primary objectives of this analysis and dashboard suite are to:
* **Quantify Transaction Volumes:** Determine total records and service throughput handled per department (**1,079 total records** analyzed).
* **Analyze Service Execution:** Compare requested applications against successfully fulfilled services (**265 complete** and **115 approved** document statuses).
* **Evaluate Operational Bottlenecks:** Identify processing backlogs, pending verifications (**102 records**), and escalation trends (**104 escalated cases**).
* **Measure Staff Performance:** Isolate and rank top-performing data capturers across departments (e.g., top officers logging up to **9 transactions** per department domain).
* **Inform Resource Allocation:** Provide actionable data insights to optimize staffing across heavy foot-traffic Gauteng regional branches (such as **Emfuleni Municipal Office** with **167 records** and **Vereeniging Home Affairs** with **153 records**).

---

## 🛠️ Tools & Technologies Used

* **Microsoft Excel:** 
  * *Data Cleaning & Transformation:* Power Query, text manipulation functions (`TRIM`, `CLEAN`, `SUBSTITUTE`), and deduplication.
  * *Exploratory Data Analysis (EDA):* Advanced Pivot Tables, summary statistics, and conditional aggregations.
  * *Dashboard Visualization:* Interactive KPI summary cards, dynamic charts, and slicers for cross-departmental filtering.
* **GitHub:** Version control, project documentation, and repository management.

---

## 📊 Dashboard & Key Analytical Insights

![](Assets/Picture.png)

An executive-grade Microsoft Excel Dashboard was built to monitor core operational KPIs. Below is a summary of the key insights supported by precise dataset metrics:

### 1. Departmental Transaction Volumes & Branch Distribution
* **Dominant Sectors:** Department of Home Affairs leads with **350 records** (32.4%), closely followed by SASSA with **318 records** (29.5%), Municipal Offices with **204 records** (18.9%), and Local Clinics with **203 records** (18.8%).
* **Top Service Requests:** **SASSA Grant Applications** represent the highest individual service volume at **208 requests**, followed by **Home Affairs ID Applications** (**143 requests**) and **SASSA Grant Status Enquiries** (**110 requests**).
* **Branch Activity Hotspots:** High-density transaction clusters were recorded at **Emfuleni Municipal Office** (**167 records**), **Vereeniging Home Affairs** (**153 records**), and **Vanderbijlpark Home Affairs** (**131 records**).

![](Assets/Picture.png)

### 2. Services Rendered vs. Applications Processed
* **Fulfillment Rate:** Out of 1,079 total logs, **265 records** are marked as *Complete* and **115 records** as *Approved*, demonstrating strong primary throughput across service channels.
* **Friction & Verification Delays:** Operational friction is highlighted by **108 records** awaiting Home Affairs confirmation, **108 rejected documents**, **106 cases under review**, and **102 records pending verification**. Furthermore, **88 incomplete ID copies** and **87 missing proof of residence** logs point to primary document intake bottlenecks.

![](Assets/Picture.png)

### 3. Processing Status & Queue Dynamics
* **Case Resolution Breakdown:** Tracking across processing statuses reveals **313 captured** logs, **117 re-opened cases**, **114 closed cases**, **104 escalated cases**, **103 fully resolved cases**, **102 awaiting documents**, and **98 pending cases**.
* **Operational Resilience:** Frontline officers utilized queue ticket tracking (`Q001`–`Q300+`) and logged system-offline workarounds in notes to ensure continuity during network outages.

![](Assets/Picture.png)

### 4. Top-Performing Data Capturers
* **Home Affairs Top Performer:** **Deon Mahlangu** led Home Affairs output with **9 recorded transactions**, supported by **Werner Khumalo** and **Deon Radebe** (**8 transactions** each).
* **Municipal Offices Top Performer:** **Andries Mahlangu**, **Deon Sithole**, and **Werner Mahlangu** tied as top contributors with **7 transactions** each.
* **Clinics Top Performer:** **Marius Khumalo** and **Refilwe Swart** achieved top clinic logging output with **6 transactions** each.
* **SASSA Top Performer:** **Refilwe Swart** and **Deon Khumalo** led SASSA processing performance with **9 transactions** each, closely followed by **Palesa Nel** (**8 transactions**).

![](Assets/Picture.png)

---

## 🗂️ Dataset Structure & Schema

![](Assets/Picture.png)

The cleaned dataset consists of structured records tracking individual citizen interactions across the following attributes:

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| **Case Reference** | Text | Unique transaction identifier (e.g., `SASSA-000796`, `DHA-001034`, `MUN-000761`) |
| **Date Captured** | Date | Timestamp of when the service log was recorded (`YYYY-MM-DD`) |
| **Service Type** | Text | Specific service requested (e.g., Passport Application, Grant Application, Service Request) |
| **Branch/Office** | Text | Service center or municipal office location |
| **Applicant Full Name** | Text | Anonymized citizen full name |
| **ID Number** | Text / Numeric | Citizen identification number |
| **Date of Birth** | Date | Applicant date of birth |
| **Gender** | Text | Applicant gender classification |
| **Ward/Area** | Text | Gauteng municipal ward designation (e.g., Ward 7, Ward 18, Ward 20) |
| **Grant Type** | Text | Specific social grant classification (applicable to SASSA records) |
| **Document Status** | Text | Status of required paperwork (e.g., Complete, Pending Verification, Under Review) |
| **Processing Status** | Text | Operational progress (e.g., Resolved, Closed, Captured, Escalated) |
| **Queue/Ticket Number** | Text | Frontline queue tracking reference |
| **Capturing Official** | Text | Staff member responsible for logging the transaction |
| **Follow-Up Date** | Date | Scheduled follow-up or review timestamp |
| **Notes** | Text | Operational remarks, exception logs, and system offline notes |

![](Assets/Picture.png)

---

## 🧹 Data Cleaning & Preparation Pipeline

To ensure high data integrity prior to dashboard visualization, a rigorous cleaning process was executed in Excel:
* **Standardization:** Standardized text casing across departmental names, branch locations, and service categories.
* **Whitespace Elimination:** Removed leading, trailing, and double spaces from text fields using Excel text cleaning functions.
* **Missing Value Management:** Handled missing departmental tags, incomplete citizen IDs, and unassigned fields through systematic imputation and flagging.
* **Date & Numeric Formatting:** Standardized date serial numbers into consistent `YYYY-MM-DD` formatting and validated integer/decimal types for processing metrics.
* **Deduplication:** Filtered out duplicate transaction logs and anomalous records to ensure accurate aggregate counts across the **1,079 total records**.
![](Assets/Picture.png)

---

## 💡 Recommendations & Strategic Improvements

1. **Targeted Resource Allocation:** Deploy additional data capturers and administrative support staff to high-demand Gauteng hubs—specifically **Emfuleni Municipal Office** (**167 records**) and **Vereeniging Home Affairs** (**153 records**)—during peak grant payout and document renewal cycles.
2. **Performance Benchmarking & Incentives:** Formalize recognition programs for top-performing data capturers across departments (such as **Deon Mahlangu**, **Refilwe Swart**, and **Andries Mahlangu**), establishing peer-learning workshops to share best practices in data entry speed and accuracy.
3. **Workflow Streamlining:** Digitize and streamline verification workflows for high-volume application types (**208 Grant Applications** and **143 ID Applications**) to reduce citizen waiting times and lower the **102 pending verification** backlogs.
4. **Enhanced System Reliability Logging:** Implement standardized digital fallback protocols for periods when municipal systems experience downtime, ensuring seamless offline capture and reconciliation.
