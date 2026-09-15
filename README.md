# COMP-SCI 5530: Principles of Data Science

**Author:** Du Doan  
**Course:** COMP-SCI 5530 - Principles of Data Science (UMKC)  

This repository contains coursework and assignments for COMP-SCI 5530.

---

## Repository Structure

```text
.
├── README.md
├── ICP1/                                       # In-Class Practice 1
│   ├── raw_data/
│   │   └── hepatitis.csv                       # Raw hepatitis dataset
│   ├── cleaned_data/
│   │   └── hepatitis_cleaned.csv               # Cleaned dataset
│   └── Doan_Joe_Week1_Checkpoint.ipynb         # Week 1 checkpoint notebook
├── Data_visualization/                         # Assignment 1 - Part 2
│   ├── raw_data/
│   │   └── StudentsPerformance.csv             # Stage 1: Raw student performance dataset
│   ├── cleaned_data/
│   │   └── cleaned_data.csv                    # Stage 2: Preprocessed student dataset
│   ├── src/
│   │   └── Data_Visualization.ipynb            # Visualizations & analysis notebook
│   ├── results/                                # Stage 3: Exported figures (800x600 px, 300 DPI)
│   │   ├── V1_Gender_boxplots.png
│   │   ├── V2_Test_prep_impact_on_math.png
│   │   ├── V3_Lunch_type_and_average_performance.png
│   │   ├── V4_Subject_correlations.png
│   │   └── V5_Math_vs_reading_with_trend_lines_by_test_prep.png
│   └── reports/
│       └── report.md                           # Stage 3: Visual report with interpretations
└── Frailty_study/                              # Assignment 1 - Part 1
    ├── data_raw/
    │   └── Frailty_Study.csv                   # Stage 1: Raw participant data
    ├── cleaned_data/
    │   └── cleaned_data.csv                    # Stage 2: Standardized & feature engineered data
    ├── src/
    │   └── Frailty_study.ipynb                 # Workflow implementation notebook
    └── reports/
        └── findings.md                         # Stage 3: Summary table & correlation findings
```

---

## ICP1 — Week 1 Checkpoint (`ICP1/`)

Introductory in-class checkpoint working with the Hepatitis dataset:
- Data loading and initial inspection
- Basic data cleaning and export of cleaned CSV

---

## Assignment 1

### 1. Frailty Study (`Frailty_study/`)

Implements a reproducible three-stage workflow analyzing physical frailty and hand grip strength among 10 female participants:
- **Unit Standardization:** Height converted to meters (`Height_m`), weight converted to kilograms (`Weight_kg`).
- **Feature Engineering:** Body Mass Index (`BMI`) calculated and rounded to 2 decimals; categorical age groups (`AgeGroup`) binned into `<30`, `30–45`, `46–60`, and `>60`.
- **Encoding:** Binary encoding for frailty indicator (`Frailty_binary`); one-hot encoding for all age categories.
- **Analysis & Findings:** Numeric summary table and Pearson correlation coefficient ($r = -0.4759$) documented in [findings.md](Frailty_study/reports/findings.md).

### 2. Student Performance Data Visualization (`Data_visualization/`)

Performs data ingestion, preprocessing, and five core visualization tasks on the Student Performance dataset:
- **V1 (Gender Boxplots):** Side-by-side boxplots comparing math and reading scores across male and female students.
- **V2 (Test Prep Impact):** KDE plot evaluating math scores by course completion status.
- **V3 (Lunch Type & Performance):** Bar chart assessing academic performance differences across lunch types.
- **V4 (Subject Correlations):** Annotated correlation matrix heatmap.
- **V5 (Math vs. Reading Trend Lines):** Scatter plot with linear regression best-fit lines by test prep cohort.

All figures exported at 300 DPI. Interpretations available in [report.md](Data_visualization/reports/report.md).
