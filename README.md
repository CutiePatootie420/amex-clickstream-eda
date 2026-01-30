# AmEx Clickstream EDA

Exploratory Data Analysis (EDA) on the AmEx dataset to understand data quality, missingness, and duplication patterns.

## Dataset
- The dataset `amex_data.csv` is **not included** in this repo.
- Download the dataset from(https://www.kaggle.com/datasets/pratsharma7/the-american-express-campus-challenge-dataset).
- Place the dataset in `data/raw/` before running the notebook.

## Project Structure
```text
eda
├── data
│   └── amex_data.csv
├── notebooks
│   └── DataAudit.ipynb
├── .gitignore
└── README.md
```
## Current Progress
- Column-wise missing value analysis
- Row-wise missingness distribution and extreme row detection
- Duplicate row detection (full-row duplicates)
- Preliminary analysis of information loss vs column removal thresholds
- Basic data faultiness exploration

## Observations & Preliminary Conclusions
- 12 columns have significant missing values (>50%), 7 with very high ones (>90%).
- Information loss ~4% if we drop columns with significant missing values, <1% for ones with high number of missing values.
- Row-level analysis shows that the majority of rows have ~25-30% missing values. We will thus try to avoid deleting rows in order to clean.
- Only ~3% of rows are duplicates or full duplicates.
- Analysis till now shows that cleaning may be column-heavy.

## Notes
- No cleaning, dropping, or imputation has been applied yet
- This notebook focuses on understanding the data, not modifying it
- Decisions on thresholding or cleaning will be made after further analysis

## Next Steps
- Analyze structured missingness across columns
- Investigate duplicate rows using candidate key columns
- Optional: time-based analysis and visualizations


