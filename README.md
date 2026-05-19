# Automated Python Data Pipeline — AI Jobs Market 2025–2026

## Project Overview
An automated data pipeline built in Python that takes raw AI job posting data and transforms it into a clean, validated, business-ready dataset — eliminating manual Excel-based processes entirely.

This project is the technical implementation of the data workflow re-engineering case study mapped in Miro (Week 2), applied to the same AI Jobs dataset analysed in SQL and Power BI (Week 1).

## Pipeline Architecture
```
Raw CSV (ai_jobs.csv — 1,500 rows, 25 columns)
    ↓
Step 1: Data Loading (pandas)
    ↓
Step 2: Data Exploration (columns, types, missing values)
    ↓
Step 3: Data Cleaning (duplicates, whitespace standardisation)
    ↓
Step 4: Data Transformation (3 new business-ready columns)
    ↓
Step 5: Data Validation (4 automated quality checks)
    ↓
Step 6: Clean Export (ai_jobs_cleaned.csv — 1,500 rows, 28 columns)
```

## What the Pipeline Does

### Data Cleaning
- Removes duplicate records
- Strips whitespace from all text columns
- Standardises formatting across 7 text fields

### Data Transformation
- **salary_range**: Calculates the gap between max and min salary for each role
- **salary_band**: Groups salaries into 5 business-friendly bands (Under 100K, 100K-150K, 150K-200K, 200K-250K, 250K+)
- **experience_rank**: Converts text experience levels into numeric rankings for sorting and analysis

### Data Validation
- Check 1: Min salary should never exceed max salary
- Check 2: Annual salary must be positive
- Check 3: Years of experience must not be negative
- Check 4: Demand score must fall within 0-100 range

**Result: 0 validation errors — all checks passed**

## Key Findings from the Data
- 430 roles (29%) fall in the 150K-200K salary band — the most common range
- Only 67 roles (4%) pay under 100K — the AI job market pays well across the board
- 300 roles (20%) pay above 250K — significant high-end opportunity
- AI Solutions Architects command the highest average salary at $251K

## Tools Used
- **Python 3.14** — core programming language
- **pandas** — data manipulation and transformation
- **numpy** — numerical operations
- **Jupyter Notebook** — interactive development environment
- **VS Code** — code editor

## Files in This Repository
- `ai_jobs_pipeline.ipynb` — complete Jupyter Notebook with all pipeline code
- `ai_jobs.csv` — raw input dataset (1,500 rows, 25 columns)
- `ai_jobs_cleaned.csv` — clean output dataset (1,500 rows, 28 columns)
- `README.md` — project documentation

## How to Run
1. Install Python 3.11+
2. Install dependencies: `pip install pandas numpy`
3. Open `ai_jobs_pipeline.ipynb` in VS Code or Jupyter
4. Run all cells in order
5. Clean dataset exports automatically to `ai_jobs_cleaned.csv`

## Part of a 4-Week LinkedIn Project Series
| Week | Project | Tools |
|------|---------|-------|
| Week 1 | AI Jobs Market Dashboard | SQL + Power BI |
| Week 2 | Data Workflow Re-Engineering Case Study | Miro |
| **Week 3** | **Automated Python Data Pipeline** | **Python + pandas** |
| Week 4 | Executive KPI Dashboard | Power BI + DAX |

## Author
**Uzair Baugwala**
Business Data Analyst
