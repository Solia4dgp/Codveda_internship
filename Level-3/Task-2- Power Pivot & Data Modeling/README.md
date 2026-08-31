# Task 2: Power Pivot & Data Modeling

# Telecom Customer Churn Analysis Using Excel Power Pivot & DAX 📊

## Project Overview

For this task, I used Excel Power Pivot and DAX to transform telecom customer data into a relational data model and generate business insights into customer churn.

The analysis moved through the following workflow:

Data Preparation → Relational Data Model → Calculated Columns → DAX Measures → PivotTables & Slicers → KPI Metrics → Business Insights
---

## 🎯 Objectives

* Use Power Pivot to create relational data models.
* Write DAX (Data Analysis Expressions) formulas.
* Optimize calculations using Measures & Calculated Columns.
* Create interactive KPI Metrics for business insights

---

## 🗂️ Dataset

The analysis uses telecom customer data containing information about:

* Customer demographics
* Account length
* International plan status
* Customer churn status
* Area codes
* Day, evening, night and international usage

A separate **AreaCodeRegion** lookup table was created to map customer area codes to their corresponding regions.

To view the [dataset](https://docs.google.com/spreadsheets/d/1ZmPher_te-OKuEpOsWDIAMNLGkIc2y8A/edit?usp=drive_link&ouid=102712416489497756938&rtpof=true&sd=true)

---

## 🔄 Relational Data Model

I structured the customer data and created a separate AreaCodeRegion lookup table containing distinct area codes and their corresponding regions.

The two tables were connected through the Area Code field in Power Pivot.

This relationship allowed customer records to be analyzed according to their respective regions rather than keeping all information in one flat dataset.

<img width="446" height="526" alt="image" src="https://github.com/user-attachments/assets/1b273bca-f071-4735-92b7-afcf6fde2413" />


This transformed the dataset from a flat table into a more structured **relational data model**.

---

## 🧮 Calculated Columns

Calculated columns were created to prepare the data for further analysis.

### Total Usage

Total Usage combines customer usage across day, evening, night and international services.

<img width="1593" height="127" alt="image" src="https://github.com/user-attachments/assets/c142e414-b83f-4b57-9f9d-a25a00af00f2" />

### Churn Flag

The Churn Flag converts the TRUE/FALSE churn status into a numeric value.

```excel
=IF([@Churn]=TRUE(),1,0)
```

* `1` = Churned
* `0` = Retained

This made churn easier to aggregate in calculations and analysis.

These calculated fields provided a consistent basis for the subsequent DAX calculations.

---

## 📐 DAX Measures

DAX measures were created in Power Pivot to calculate key customer and churn metrics.

### Total Customers

```DAX
Total Customers =
COUNTROWS(CustomerData1)
```

**Purpose:** Counts the total number of customer records.
<img width="778" height="681" alt="image" src="https://github.com/user-attachments/assets/4bef9bf9-40c4-487f-be41-889d8bd8d51e" />

### Churned Customers

```DAX
Churned Customers =
CALCULATE(
    COUNTROWS(CustomerData1),
    CustomerData1[Churn] = TRUE()
)
```

**Purpose:** Counts customers who churned.
<img width="889" height="640" alt="image" src="https://github.com/user-attachments/assets/5c432858-1c8a-4f0b-a5f5-d5b966878b8a" />


### Churn Rate

```DAX
Churn Rate =
DIVIDE(
    [Churned Customers],
    [Total Customers],
    0
)
```

The result was formatted as a percentage.

**Purpose:** Measures the percentage of customers who churned.
<img width="792" height="664" alt="image" src="https://github.com/user-attachments/assets/31663df8-2714-4ae2-8037-21c0359790c2" />

### Average Account Length

```DAX
Average Account Length =
AVERAGE(CustomerData1[Account length])
```

**Purpose:** Measures average customer tenure.
<img width="780" height="663" alt="image" src="https://github.com/user-attachments/assets/3d9fedc3-c9eb-45f4-a85c-56d8d8cb8db6" />

### Average Total Usage

```DAX
Average Total Usage =
AVERAGE(CustomerData1[Total usage])
```

**Purpose:** Measures average customer usage.
<img width="788" height="662" alt="image" src="https://github.com/user-attachments/assets/342ab0d3-b690-44f5-b118-8dc0e309ef0b" />

---

## Pivot Table & Slicers
The DAX measures were used in PivotTables to summarize customer churn and usage from different perspectives.

Slicers were added to make the analysis interactive and allow users to filter the results.

<img width="392" height="80" alt="image" src="https://github.com/user-attachments/assets/424e74f2-65f2-42e1-9cbc-0b5b9a44dde0" />

The interactive analysis made it possible to explore customer churn based on dimensions such as:

Region
State
International Plan
Churn status

---

## 📊 KPI Metrics
The DAX measures were brought together into an interactive KPI view.

<img width="693" height="64" alt="image" src="https://github.com/user-attachments/assets/92541520-141e-450f-b8bc-1e529510e35f" />

The overall churn rate was calculated as:

```text
483 ÷ 3,333 × 100 = 14.49%
```

---

## 🔍 Key Business Insights 
The overall analysis identified several patterns in customer churn.

- Overall Churn

    There were 3,333 customers, of which 483 churned.

    483 ÷ 3,333 × 100 = 14.49%

    The overall customer churn rate was therefore 14.49%.

- Churn by Region

    Churn rates were relatively similar across the three regions:

    East Bay: 14.88%
    Santa Clara: 14.56%
    Marin: 14.26%

    This suggests that region alone was not a major driver of customer attrition.

- International Plan & Churn

    Customers with an International Plan had a substantially higher churn rate:

    Without International Plan: approximately 11.5%
    With International Plan: approximately 42.4%

    This makes International Plan enrollment an important factor for further investigation.

- Highest-Churn States

    The highest individual state churn rates included:

    California: 26.47%
    New Jersey: 26.47%
    Texas: 25.00%
    Maryland: 24.29%
    
    These states represent higher-risk customer segments where targeted retention strategies could be explored.

- Total Usage by Churn

    Retained customers accounted for: 1,665,857 total usage units
    
    Churned customers accounted for: 306,829 total usage units
    
    The difference suggests that customer engagement and usage behavior may be useful signals when investigating churn.

Business Insights Evidence







---

## 📊 Visualizations

The analysis was extended beyond the required data model and DAX calculations by creating visualizations to make the findings easier to interpret.

### Visuals included:

* Churn Rate by Region
* Churn Rate by International Plan
* Top 10 States by Churn Rate
* Total Usage by Churn Status

<img width="1378" height="612" alt="image" src="https://github.com/user-attachments/assets/960d7207-40f8-46dd-94f1-de823435e54d" />

These visuals were used to explore customer behavior and identify potential churn patterns.

---

## 💡 Business Questions Answered

The analysis was designed to answer questions such as:

1. What is the overall customer churn rate?
2. How many customers have churned?
3. Is International Plan enrollment associated with higher churn?
4. How does churn vary across regions?
5. Which states have the highest churn rates?
6. How does customer usage differ between churned and retained customers?
7. Can usage behavior provide an indication of customer engagement?

---

## 🛠️ Tools & Technologies

* Microsoft Excel
* Power Query
* Power Pivot
* DAX
* PivotTables
* Slicers
* Data Visualization

---


## Linkedin Post
See the full project walkthrough on [LinkedIn](https://www.linkedin.com/posts/aileru-solia-471407285_dataanalysis-excel-powerpivot-activity-7499676510983790592-Awg2?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEVLMdUBDlhp6fhuqXMKrvomaXej1w4FXQI)
