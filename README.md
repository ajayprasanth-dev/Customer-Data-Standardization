# Customer Data Standardization Project

## Project Overview

This project presents an **end-to-end data cleaning and standardization workflow** designed to transform a raw, inconsistent customer call list into a clean, analysis-ready dataset.

All transformations were performed using **Python** and the **Pandas** library, showcasing strong proficiency in real-world data wrangling and preprocessing.

---

## Project Context

In most organizations, customer datasets are collected from multiple sources, often resulting in **inconsistent formats, missing values, and redundant information**.

The objective of this project was to build a **reliable and reproducible data cleaning pipeline** capable of converting messy real-world data into a structured format ready for analytics or CRM integration.

---

## Data Quality Challenges and Solutions

### 1. Inconsistent Contact Formatting

* **Issue:** Phone numbers included mixed separators (-, /, |), scientific notation, and invalid text entries such as “N/a.”
* **Solution:** Used **Regular Expressions (RegEx)** with `str.replace()` to remove all non-numeric characters and cast results as strings to maintain a 10-digit format. Missing values were replaced with "MISSING".

### 2. Boolean Field Standardization

* **Issue:** Boolean columns (Paying Customer, Do\_Not\_Contact) contained inconsistent representations such as Yes, Y, No, N, and blanks.
* **Solution:** Applied targeted `.replace()` mappings to standardize all variants into **"Yes" or "No"**.

### 3. Text and Structural Cleanliness

* **Issue:** Text fields like customer names and addresses contained inconsistent capitalization, extra spaces, and unwanted symbols (/, ").
* **Solution:**
    * Removed leading and trailing whitespace using `.str.strip()`
    * Standardized capitalization with `.str.capitalize()`
    * Cleaned unwanted symbols using `.str.replace()`
    * Replaced invalid placeholders (No/a, N/a, nan) with **"UNKNOWN"**

### 4. Structural Integrity

* **Issue:** The dataset contained duplicate rows and irrelevant columns.
* **Solution:**
    * Ensured unique records using `df.drop_duplicates()`
    * Removed unnecessary fields such as `Not_Useful_Column` to improve dataset clarity

---

## Key Technical Deliverables

* **Core Library:** **Pandas** for all data manipulation and transformation
* **String Operations:** Chained string methods (`.str.strip().str.capitalize()`) for efficient text processing
* **Data Integrity:** Reliable duplicate removal using `df.drop_duplicates()`
* **Missing Data Handling:** Combined use of `.fillna()` and `.replace()` for accurate imputation

---

## Outcome

The final dataset achieved:

* **Fully standardized** contact and text formatting
* **Clean, validated entries** for names, addresses, and boolean fields
* **Duplicate-free structure** with only relevant columns retained
* **Ready-to-use data** for sales analytics, CRM systems, and BI dashboards

---

## Skills Demonstrated

* Data Cleaning & Preprocessing
* Regular Expressions (RegEx)
* Data Wrangling with Pandas
* Text Normalization & Standardization
* Data Quality Validation
* Python for Data Analytics
