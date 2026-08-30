# Task 3: Array Formulas & Dynamic Array

## Objective
- Use SEQUENCE, UNIQUE, SORT, FILTER for data automation.
- Apply TRANSPOSE to rearrange datasets.
- Utilize SUMPRODUCT for advanced data aggregation.
- Understand Array Formulas (CSE Formulas) in older Excel versions

The dataset contains measurements of sepal and petal length and width across three species of iris flowers.

---

## Data Preparation & Excel Techniques

- Before applying the functions, I reviewed the dataset structure and identified how each function could be used to make data manipulation more efficient.
- I created an automated ID column using the SEQUENCE function rather than manually numbering each record.
- I also prepared sections of the worksheet to demonstrate how dynamic arrays can return and update multiple values automatically.

---

## Excel Functions Applied

### SEQUENCE
```excel
=SEQUENCE(ROWS(Table1))
```

SEQUENCE was used to automatically generate record numbers based on the number of rows in the dataset.

Unlike manually entering IDs, the sequence automatically adjusts when the number of records changes.

**Purpose:** Automate record numbering and reduce manual data entry.

---

### UNIQUE

```excel
=UNIQUE(Table1[Species])
```

UNIQUE was used to return the distinct iris species contained in the dataset.

**Purpose:** Quickly identify unique categorical values without manually searching or removing duplicates.

---

### SORT

```excel
=SORT(Table1[[Sepal_length]:[Petal_length]],3,1)
```

SORT was used to organize the selected measurement columns based on the third column in ascending order.

**Purpose:** Dynamically arrange records without manually sorting the original dataset.

---

### FILTER

```excel
=FILTER(Table1[[#All],[Sepal_length]:[Petal_length]],Table1[[#All],[Sepal_length]]>=5)
```

FILTER was used to return records where the sepal length was **5 or greater**.

**Purpose:** Extract specific records based on a condition while leaving the original dataset unchanged.

---

### TRANSPOSE

```excel
=TRANSPOSE(B5:F8)
```

TRANSPOSE was used to change the orientation of a selected range from rows to columns.

**Purpose:** Rearrange data when a different layout is more suitable for analysis or presentation.

---

### SUMPRODUCT
``` excel
=SUMPRODUCT(Table1[Petal_length])
=SUMPRODUCT(--(Table1[Petal_length]>1.5))
=SUMPRODUCT((Table1[Sepal_length]>=5)*Table1[Petal_length])
```

SUMPRODUCT was used to perform calculations across multiple conditions and ranges.

**Purpose:** Perform advanced aggregation without relying on several separate calculations.

It is particularly useful when calculations need to consider multiple criteria simultaneously.

---

## Array Formulas & CSE
``` excel
=AVERAGE(IF(Table1[Sepal_length]>=5,Table1[Petal_length]))
```
I also explored how array formulas work in older versions of Excel.

In older versions of Excel, certain array formulas required **Ctrl + Shift + Enter (CSE)** to return results.

Newer versions of Excel support **Dynamic Arrays**, allowing formulas to automatically spill results into multiple cells without requiring CSE.

This demonstrated the difference between traditional array formulas and the newer dynamic-array approach.

---

## Interactive Features

The workbook demonstrates how Dynamic Array Functions can make Excel analysis more automated.

The functions dynamically return, organize and manipulate data without requiring the user to manually copy, sort, filter, or number records.

This makes the workbook easier to update when the underlying dataset changes.

---

## Key Outcome

This task demonstrated how Excel functions can be used to move beyond manual data manipulation.

Instead of manually:

* Numbering records
* Identifying unique values
* Sorting data
* Searching for specific records
* Rearranging data

I used dynamic and array-based functions to automate these processes.

The result is a more efficient approach to working with structured datasets and a better understanding of how modern Excel handles dynamic results.

---

## Skills Demonstrated

* Dynamic array functions
* Sequence
* Unique
* Sort
* Filter
* Transpose
* Sumproduct
* Array formulas
* CSE formulas
* Data manipulation
* Conditional data extraction
* Automated record numbering
* Excel data analysis

---

## To View the Dataset

To view the [dataset](https://docs.google.com/spreadsheets/d/1XyJ98G8JUDCNF-mUSjYORxV2mO0j-tpC/edit?usp=drive_link&ouid=102712416489497756938&rtpof=true&sd=true).

---

## Screenshots
<img width="789" height="277" alt="Screenshot (335)" src="https://github.com/user-attachments/assets/0abe0835-b7f4-4a1f-a6bc-718ff5508bbd" />



## Linkedin Post
Check out my [LinkedIn post](https://www.linkedin.com/posts/aileru-solia-471407285_dataautomation-internship-learninginpublic-activity-7496940651171840000-5RsR?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEVLMdUBDlhp6fhuqXMKrvomaXej1w4FXQI) for a detailed overview of this task, the techniques I applied, and my key takeaways.

