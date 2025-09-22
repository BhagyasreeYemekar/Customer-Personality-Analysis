# 🧹 Marketing Campaign Dataset Cleaning

This project cleans and prepares the **Marketing Campaign dataset** for analysis or modeling.

## 📌 Steps Performed in the Notebook
1. **Import libraries**  
   - `pandas`, `numpy`, `datetime`, `pathlib2. **Load dataset**  

2. **Load dataset**  
   - Supports `.xls`, `.xlsx`, and `.csv`  
   - Handles errors if `xlrd` is missing for `.xls`

3. **Initial exploration**  
   - Shape, column names, dtypes, missing values, duplicates
   - 
4. **Column name standardization**  
   - Lowercased, spaces → `_`, removed special characters

5. **Data type fixes**  
   - Trimmed string columns  
   - Converted numeric-like strings → numbers  
   - Parsed date-like columns → `datetime`

6. **Handling missing values & duplicates**  
   - Dropped duplicate rows  
   - Filled numeric missing with **median**  
   - Filled categorical missing with **mode**

7. **Feature engineering**  
   - `age` from `year_birth`  
   - `total_spent` from `Mnt*` columns  
   - `total_purchases` from purchase columns  
   - `family_size` = `kidhome + teenhome + 1`

8. **Outlier treatment**  
   - Capped values using the **IQR method**

9. **Categorical encoding**  
   - Converted low-cardinality categorical variables to dummy variables (one-hot encoding)

10. **Save cleaned dataset**  
    - Saved as `marketing_campaign_cleaned.csv`


## 📂 Outputs

- `marketing_campaign_cleaned.csv`

These cleaned files are ready for **EDA, visualization, or ML modeling**.

