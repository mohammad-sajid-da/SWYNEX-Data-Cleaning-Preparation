# SWYNEX - Task 1: Data Cleaning & Preparation

## Overview
This repository contains the data cleaning workflow for Task 1 of the Data Analytics Internship at Swynex Technologies. The objective is to identify and resolve data quality issues in a raw customer transactions dataset using Python (Pandas).

## Identified Data Quality Issues
- **Duplicate Records:** 16 duplicate entries detected across the dataset.
- **Missing Values:** Identified null entries across Name, Age, Gender, City, JoinDate, PurchaseAmount, ProductCategory, and Rating.
- **Inconsistent Categorical Entries:** 
  - Gender: Unstandardized entries (female, f, M, MALE, Female).
  - City: Mixed casing and historical names (Bombay vs Mumbai, Madras vs Chennai, Banaras vs Varanasi).
  - ProductCategory: Plural and singular variants (Book vs BOOKS, Grocery vs Groceries).
- **Data Type & Format Inconsistencies:**
  - Age: String formatting containing "yrs" text and negative values (-5 yrs).
  - PurchaseAmount: Text values containing currency symbols (₹) and thousand commas.
  - JoinDate: Mixed date formatting (DD/MM/YYYY, YYYY/MM/DD, DD-Mon-YYYY).

## Cleaning Steps Executed
1. **Deduplication:** Dropped 16 duplicate rows using .drop_duplicates().
2. **Imputation:** Imputed missing values for Age, PurchaseAmount, and Rating using median values, and categorical blanks with "Unknown" or "Other".
3. **Normalization:** Mapped and standardized City, Gender, and ProductCategory into unified standard categories.
4. **Data Type Casting:** Stripped string artifacts from Age and PurchaseAmount and converted them to integer and float respectively. Standardized JoinDate to YYYY-MM-DD ISO format.

## Repository Structure
- raw_data.csv: Original uncleaned dataset.
- cleaned_data.csv: Final prepared dataset ready for analysis.
- SWYNEX_Task1_Data_Cleaning.ipynb: Step-by-step cleaning execution code.
