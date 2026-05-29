# Projeto - Diabetes Engineering Pipeline

This project cleans and ingests the dirty Diabetes dataset from the course Final Project.

### Dataset

- Relative path: `Projeto/raw/uci-diabetes/dirty/diabetes-dirty.csv`
- Dataset: Diabetes

### Workflow

- Loaded the semicolon-separated dirty CSV
- Removed the accidentally saved index column (`Unnamed: 0`)
- Standardized column names (strip whitespace and lowercase)
- Dropped redundant columns (`index` and `bmi category`)
- Inspected unique values for categorical columns
- Converted inconsistent missing markers (`?`) to `NaN`
- Calculated the quantity of missing values per column
- Standardized categorical values such as 'Positive', 'Negative', 'North', 'South, 'Routine Follow-up', 'High-Risk', 'Urgent Monitoring', 'Adult', 'Senior', 'Mid-Age'
- Fixed column types by cleaning numeric fields polluted with text
- Imputed missing values (median for numeric, mode for categorical)
- Detected and removed duplicate rows
- Detected outliers in numerical columns using the IQR method
- Added a `source_file` column to track data origin
- Exported cleaned dataset to `raw/uci-diabetes/cleaned/diabetes-cleaned.csv`