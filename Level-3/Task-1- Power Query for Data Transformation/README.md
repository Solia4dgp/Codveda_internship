# Task 1: Power Query – Data Transformation & Automation

## Objective

- Connect and import data from external sources.
- Perform Merging & Appending Queries.
- Apply Grouping and Data Shaping.
- Automate data refresh for real-time analysis

---

## Data Preparation & Power Query Techniques

For this task, I worked with two customer churn datasets containing information such as account details, usage patterns, service calls and churn status.

I used excel power query to connect to and transform the datasets rather than performing the preparation manually in the worksheet.

---

## Connect & Import Data

I imported both datasets into excel power query and treated them as separate source queries.

Keeping the datasets as separate queries allowed me to maintain the original sources while creating a structured transformation workflow.

---

## Append Queries

Because the two datasets shared the same column structure, I used append queries as new to combine their records into one consolidated dataset.

This allowed me to bring together the records while preserving the original fields.

**Purpose:** Combine datasets with the same structure into a single dataset for analysis.

---

## Region Reference Table & Merge

I created a separate region reference table using area codes.

I then used merge queries as new to connect the Region table with the consolidated customer dataset.

This allowed the customer records to be enriched with their corresponding region information based on the area code.

**Purpose:** Combine related datasets using a common field and add useful contextual information to the main dataset.

---

## Data Shaping & Data Types

I reviewed the structure of the transformed dataset and ensured that each column had the appropriate data type.

I also deliberately retained the original columns because they could contribute to the analysis. Rather than removing fields simply for the sake of cleaning, I focused on preserving useful information while improving the structure of the dataset.

---

## Grouping

I used grouping to transform customer-level records into higher-level summaries.

This made it easier to investigate patterns in customer behavior and churn by aggregating related records into meaningful groups.

**Purpose:** Transform detailed customer-level data into summarized information that can support analysis.

---

## Data Refresh & Automation

The Power Query workflow provides a repeatable transformation process.

Once the source data is updated, the queries can be refreshed so that the transformations, append, merge, grouping and other applied steps can be reapplied without rebuilding the process manually.

This reduces repetitive data preparation and makes the workflow easier to maintain when new records are introduced.

---

## Key Outcome

This task demonstrated how **Power Query can transform multiple source datasets into a structured, analysis-ready dataset through a repeatable workflow**.

The process involved:

**External Sources → Import → Append → Merge → Data Types → Group → Refresh**

Instead of manually combining and restructuring the datasets, I created a transformation workflow that can be refreshed as the source data changes.

---

## Skills Demonstrated

* Connecting and importing external data
* Excel power query
* Append queries
* Merge queries
* Data shaping
* Grouping
* Data type management
* Data transformation
* Repeatable ETL workflows
* Query refresh
* Customer churn analysis

---

## LinkedIn Post

Check out my [LinkedIn post](https://www.linkedin.com/posts/aileru-solia-471407285_codveda-codvedatech-dataanalysis-activity-7498240729740386304-dhJG?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEVLMdUBDlhp6fhuqXMKrvomaXej1w4FXQI) for a walkthrough of the Power Query workflow, transformation process and key lessons from the project.

---

## Dataset

To view the [dataset](https://docs.google.com/spreadsheets/d/1qo4Yn8JoGDcIXBJf7ze934PwJxEw83b5/edit?usp=drive_link&ouid=102712416489497756938&rtpof=true&sd=true)

---

## Screenshots

### External data import

<img width="1920" height="1080" alt="group" src="https://github.com/user-attachments/assets/7133541b-2b1f-44a9-946f-e1d6c1151d5a" />

### Append queries

<img width="520" height="224" alt="Appen" src="https://github.com/user-attachments/assets/fc4a076d-4f76-451f-a8a6-1ec2429bdcf4" />

### Merge queries

<img width="727" height="468" alt="Merg" src="https://github.com/user-attachments/assets/d85f4cba-2497-4b1e-883b-43dda0eb38b1" />

### Grouping
<img width="852" height="439" alt="Screenshot (349)" src="https://github.com/user-attachments/assets/00c50589-5c65-474c-9911-e93c7c20d67f" />


### Data types
<img width="952" height="521" alt="image" src="https://github.com/user-attachments/assets/8c6b7d15-646f-4cf7-a2b4-1c2f456e8797" />

<img width="652" height="399" alt="image" src="https://github.com/user-attachments/assets/a2efdb48-92c2-4045-a91c-37e5dcc60764" />

