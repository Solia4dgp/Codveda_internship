## Objective 
* Remove duplicates and blank values.
* Use TRIM, CLEAN, SUBSTITUTE to standardize text.
* Apply TEXT-TO-COLUMNS & Flash Fill for data transformation.
* Implement Find & Replace for mass updates.

## Data Preparation & Excel Techniques
* Used **Remove Duplicates** from the Data tab to identify and eliminate duplicate records and improve data integrity.
* Created a dedicated **staging sheet** to clean selected columns using a combination of **TRIM, CLEAN, and SUBSTITUTE** functions.
* Used **Text to Columns with delimiters** to separate the combined timestamp into distinct **Date** and **Time** columns.
* Derived the **Year** from the Date column and used **Flash Fill** to automatically populate the remaining values based on the established pattern.

## Excel Functions Applied
```excel
 =TRIM(CLEAN(Table1[@Column_name]))
```
It was used to clean the text, platform, sentiment, country and user column 
```excel
=SUBSTITUTE(TRIM(CLEAN(Table1[@Hashtags]))," #",", #")
```
It was used to clean and substitute the hashtag column


## Dataset
To view the [dataset](https://docs.google.com/spreadsheets/d/18Bs1UUJZBMIhIHGMsE7C_kT5wNTlJRvV/edit?usp=drive_link&ouid=102712416489497756938&rtpof=true&sd=true)

### Key Learning
I learned that structured references behave differently depending on whether the `@` symbol is used. The `@` operator refers to the value in the **current row**, while the column reference without `@` refers to the **entire table column**.

## Screenshot
<img width="793" height="379" alt="Screenshot (337)" src="https://github.com/user-attachments/assets/caff691f-eedf-470c-871a-a021dc199f04" />


## Linkedin Post
For a closer look at my approach and learning experience, check out the accompanying [LinkedIn post](https://www.linkedin.com/posts/aileru-solia-471407285_datacleaning-excel-codvedainternship-activity-7497274091045830656-JNv9?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEVLMdUBDlhp6fhuqXMKrvomaXej1w4FXQI).

