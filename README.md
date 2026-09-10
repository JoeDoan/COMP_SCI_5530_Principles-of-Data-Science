# COMP-SCI 5530: Principles of Data Science - Assignment 1

**Author:** Du Doan  
**Course:** COMP-SCI 5530 - Principles of Data Science (UMKC)  

This repository contains the complete implementation for **Assignment 1**, structured into two self-contained projects adhering to reproducible data science workflows (Ingest → Process → Analyze).

---

## Repository Structure

```text
.
├── README.md
├── .gitignore
├── Frailty_study/
│   ├── data_raw/
│   │   └── Frailty_Study.csv           # Stage 1: Raw participant data
│   ├── cleaned_data/
│   │   └── cleaned_data.csv            # Stage 2: Standardized & feature engineered data
│   ├── src/
│   │   └── Frailty_study.ipynb         # Workflow implementation notebook
│   └── reports/
│       └── findings.md                 # Stage 3: Summary table & correlation findings
└── Data_visualization/
    ├── raw_data/
    │   └── StudentsPerformance.csv     # Stage 1: Raw student performance dataset
    ├── cleaned_data/
    │   └── cleaned_data.csv            # Stage 2: Preprocessed student dataset
    ├── src/
    │   └── Data_Visualization.ipynb    # Visualizations & analysis notebook
    ├── results/                        # Stage 3: Exported figures (800x600 px, 300 DPI)
    │   ├── V1_Gender_boxplots.png
    │   ├── V2_Test_prep_impact_on_math.png
    │   ├── V3_Lunch_type_and_average_performance.png
    │   ├── V4_Subject_correlations.png
    │   └── V5_Math_vs_reading_with_trend_lines_by_test_prep.png
    └── reports/
        └── report.md                   # Stage 3: Visual report with 5-8 sentence interpretations
```

---

## 1. Frailty Study (`Frailty_study/`)

Implements a reproducible three-stage workflow analyzing physical frailty and hand grip strength among 10 female participants:
- **Unit Standardization:** Height converted to meters (`Height_m`), weight converted to kilograms (`Weight_kg`).
- **Feature Engineering:** Body Mass Index (`BMI`) calculated and rounded to 2 decimals; categorical age groups (`AgeGroup`) binned into `<30`, `30–45`, `46–60`, and `>60`.
- **Encoding:** Binary encoding for frailty indicator (`Frailty_binary`, `1` for Yes, `0` for No, stored as `int8`); one-hot encoding for all age categories.
- **Analysis & Findings:** Numeric summary table (mean, median, standard deviation) and Pearson correlation coefficient ($r = -0.4759$) quantifying the relationship between grip strength and frailty, documented in [findings.md](Frailty_study/reports/findings.md).

---

## 2. Student Performance Data Visualization (`Data_visualization/`)

Performs data ingestion, preprocessing (verification of 0 missing values), and five core visualization tasks on the Student Performance dataset:
- **V1 (Gender Boxplots):** Side-by-side boxplots comparing math and reading scores across male and female students.
- **V2 (Test Prep Impact):** Kernel density estimation (KDE) plot evaluating math scores by course completion status.
- **V3 (Lunch Type & Performance):** Bar chart assessing academic performance differences across standard vs. free/reduced lunch recipients.
- **V4 (Subject Correlations):** Annotated correlation matrix heatmap illustrating strong linear associations between math, reading, and writing.
- **V5 (Math vs. Reading Trend Lines):** Scatter plot with linear regression best-fit lines comparing slopes and intercepts between test preparation cohorts.

All visual figures are exported at 300 DPI resolution, and comprehensive 5–8 sentence interpretations addressing each specific research question are available in [report.md](Data_visualization/reports/report.md).
