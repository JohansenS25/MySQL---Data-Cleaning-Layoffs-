# Layoffs Data Cleaning Project (MySQL)

**Summary:**  
This project involved cleaning a real-world dataset of global layoffs using SQL in MySQL Workbench. It showcases essential data wrangling techniques such as deduplication, data standardization, and handling missing values to prepare the dataset for analysis and visualization.

## Objectives

- Apply data cleaning best practices using SQL.
- Prepare a raw dataset for accurate business insights.
- Demonstrate use of window functions, joins, and data transformations.

## Data Cleaning Process

1. **Created a Staging Table**
   - Copied the raw dataset into a staging table to preserve the original data.

2. **Removed Duplicates**
   - Used `ROW_NUMBER()` to identify duplicates based on key columns.
   - Deleted duplicate entries after verification.

3. **Standardized Data**
   - Trimmed whitespace, unified industry categories, and corrected country names.
   - Converted date values from strings to `DATE` format.

4. **Handled Null and Blank Values**
   - Replaced blanks with `NULL`, then filled in missing values using self-joins.
   - Removed entries lacking key layoff information.

5. **Dropped Temporary Columns**
   - Removed helper columns (like `row_num`) after completing deduplication.

## Tools and Techniques Used

- MySQL Workbench
- SQL: CTEs, `ROW_NUMBER()`, `JOIN`, `UPDATE`, `DELETE`, `TRIM`, `STR_TO_DATE()`
- Data cleaning workflow development

## File

- `MySQL - Data Cleaning (Layoffs).sql`: All SQL queries with in-line documentation.

## Key Skills Demonstrated

- SQL scripting and data cleaning
- Analytical thinking and attention to detail
- Data normalization and preparation
- Real-world problem solving with staging workflows

