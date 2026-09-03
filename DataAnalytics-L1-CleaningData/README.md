# Titanic Dataset - Data Cleaning

## Project Overview
This project focuses on identifying and correcting data quality issues in the Titanic dataset to produce a clean, consistent, and analysis-ready dataset.

---

## Data Cleaning Workflow
The pipeline was implemented using Python (`pandas`, `matplotlib`, `seaborn`) in a Jupyter Notebook:

1. **Initial Inspection & Exploration:**
   * Analyzed dimensions (891 rows, 12 columns), column datatypes, and summary statistics.
   * Visualized missing data distribution using heatmaps.

2. **Data Standardization & Formatting:**
   * Removed leading and trailing whitespaces from all text columns (`Name`, `Sex`, `Ticket`, `Embarked`).
   * Standardized categorical values in `Sex` to lowercase and `Embarked` to uppercase.

3. **Handling Missing Values:**
   * **`Age` (177 missing):** Imputed with the median age (~28.0) to avoid skewness from extreme values.
   * **`Embarked` (2 missing):** Imputed with the mode (`'S'`).
   * **`Cabin` (687 missing, ~77.1%):** Dropped the entire column due to excessive missingness.

4. **Duplicate Record Detection:**
   * Verified that the dataset contains 0 duplicate rows across all columns.

5. **Type Validation & Range Checks:**
   * Verified numeric types for identifiers, ticket classes, passenger counts, and fares.
   * Validated domain constraints (no negative ages/fares, valid binary values for `Survived`, valid classes 1–3).

6. **Outlier Analysis (IQR Method):**
   * Identified potential outliers using the Interquartile Range ($Q1 - 1.5 \times IQR$ to $Q3 + 1.5 \times IQR$):
     * **`Fare`:** 116 statistical outliers.
     * **`Age`:** 66 statistical outliers.

---

## Dataset Summary: Before vs. After

| Metric | Before Cleaning | After Cleaning |
| :--- | :--- | :--- |
| **Rows** | 891 | 891 |
| **Columns** | 12 | 11 |
| **Missing Values** | 866 | 0 |
| **Duplicate Rows** | 0 | 0 |

---

## Repository Contents
* `Untitled.ipynb`: Jupyter Notebook detailing the data cleaning pipeline.
* `cleaned_titanic_dataset.csv`: Cleaned output dataset.
* `train.csv`: Raw input data.
