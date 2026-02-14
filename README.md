# Ticket Time Intelligence

## Phase 1 – Business Understanding & Data Foundation

---

## 📌 Project Overview

This project focuses on calculating, analyzing, and visualizing ticket working durations across organizational processes. The main objective is to evaluate operational performance, measure compliance with defined OLA/SLA targets, and support data-driven decision-making within the operations and service departments.

The analysis is based on operational ticket status change data and is structured using a Fact-Dimension analytical model to enable scalable reporting and KPI tracking.

---

## 1️⃣ Business Understanding

### 1.1 Business Domain

Based on process names and operational roles, the dataset belongs to the **Telecommunications / ISP / Service Operations** industry. The organization operates across:

* B2C services
* B2B solutions
* Technical support operations
* Financial processing
* Wireless and infrastructure services

The project focuses specifically on **Operational Performance Management** within ticket handling workflows.

---

### 1.2 Business Problem

The core business question identified during stakeholder discussions:

> Are tickets being processed within the committed operational time, and where are the operational bottlenecks?

This analysis aims to determine:

* Whether OLA commitments are respected
* Which roles or categories cause delays
* How stable and predictable ticket resolution times are
* Where operational improvements are required

---

### 1.3 Decision Objectives

The analysis supports decisions such as:

* Resource allocation or redistribution
* Workflow redesign
* OLA redefinition
* Performance monitoring across categories (B2B, B2C, Tech)
* Identifying operational inefficiencies

The analysis is not exploratory for its own sake. It is designed to support **operational decision-making**.

---

## 2️⃣ Data Understanding

### 2.1 Data Sources

The dataset includes three main tables:

### Fact Table

**TrReport**
Contains ticket status change records (44,000+ rows).
Each row represents a transition between statuses.

### Dimension Tables

**ProcessName** – Process definitions
**Process Roles** – Organizational roles and departments

---

### 2.2 Data Model Approach

A Star Schema design is proposed:

* Fact_ProcessStatusChange (TrReport)
* Dim_Process
* Dim_Role
* Dim_Date
* Dim_Category
* Dim_Status

This structure supports KPI calculation and scalable reporting in Power BI.

---

### 2.3 Column Roles (Summary)

The dataset includes:

* Numeric variables (Duration, OLA, Ticket Count)
* Categorical variables (Role, Category, Process)
* Time variables (Created Date, Resolved Date)

Duration is derived from Created and Resolved timestamps and used as the core analytical measure.

---

## 3️⃣ KPI Framework

KPIs were selected based on business decision needs, not data availability.

Selected KPIs include:

* Average Resolution Time
* Median Resolution Time
* SLA/OLA Compliance Rate
* SLA Breach Rate
* Duration by Role
* Duration by Category
* P90 Resolution Time
* Ticket Volume

Each KPI satisfies three conditions:

* Measurable
* Actionable
* Explainable in one sentence

---

## 4️⃣ Visualization Strategy

The visualization design focuses on:

* Clarity
* Fast interpretation
* Operational decision support

Recommended structure:

Top Layer:

* KPI Cards (Average Duration, SLA Compliance, Ticket Volume)

Middle Layer:

* Trend Line (Time-based performance)
* Bar Charts (Duration by Role & Category)

Lower Layer:

* Histogram (Duration Distribution)
* Detailed Matrix (Drill-down analysis)

The reporting approach supports both executive and operational audiences.

---

## 5️⃣ Data Risks & Limitations

Potential risks identified:

* Missing Resolved timestamps
* Delayed status registrations affecting time accuracy
* Lack of complexity indicators per ticket
* Limited predictive variables
* Possible inconsistencies in status descriptions

The dataset is sufficient for descriptive and diagnostic analysis but limited for predictive modeling.

---

## 6️⃣ Type of Analysis

Current Phase Scope:

* Descriptive Analysis
* Diagnostic Analysis

Future expansion may include:

* Predictive modeling
* Prescriptive recommendations

---

## 7️⃣ Deliverables of Phase 1

* Business problem definition
* Decision-oriented KPI framework
* Data model design
* Column role identification
* Risk assessment
* Visualization strategy

This phase establishes the analytical foundation for performance measurement.

---

## 📎 Data Reference

For detailed column-level description, schema design, and KPI logic, refer to:

> Section: Data Understanding & KPI Framework

---

## 🚀 Next Phase

Phase 2 will focus on:

* Power BI implementation
* DAX measure development
* Distribution analysis
* OLA compliance visualization
* Operational bottleneck identification
