# Layoffs Data Cleaning Project (MySQL)

This project focuses on cleaning a global layoffs dataset using SQL in MySQL Workbench. The dataset includes company, industry, and layoff details from various countries. The goal was to prepare the data for accurate analysis by removing duplicates, standardizing entries, handling null values, and formatting data types.

## 🧼 Data Cleaning Steps

1. **Created a Staging Table**  
   - Duplicated the raw `layoffs` table into `layoffs_staging` for safe modification.

2. **Removed Duplicates**  
   - Used `ROW_NUMBER()` window function to identify and delete exact duplicates based on multiple columns.

3. **Standardized the Data**  
   - Trimmed white spaces in company and country names.
   - Standardized industry names (e.g., consolidated "Crypto", removed inconsistencies).
   - Converted the `date` column from text to proper `DATE` format.

4. **Handled Null and Blank Values**  
   - Replaced blank industries with `NULL`.
   - Filled missing industry values using self-join logic based on company and location.
   - Removed rows where both `total_laid_off` and `percentage_laid_off` were missing.

5. **Dropped Unnecessary Columns**  
   - Removed the temporary `row_num` column used for deduplication.

## 💡 Tools & Concepts Used

- MySQL Workbench
- Window Functions (`ROW_NUMBER()`)
- Common Table Expressions (CTEs)
- Self Joins
- Data Type Conversion (`STR_TO_DATE`)
- `TRIM()` and string cleaning functions

## 📁 File

- `MySQL - Data Cleaning (Layoffs).sql` — complete SQL script with step-by-step cleaning operations.

## 🔍 Purpose

This project demonstrates best practices in data cleaning for analytics and reporting. Clean, structured data ensures more reliable visualizations and data-driven decisions.

---
