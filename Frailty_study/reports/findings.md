# Frailty Study - Statistical Summary & Findings

## 1. Summary Statistics Table
The table below reports the mean, median, and standard deviation for all standardized and engineered numeric variables across the 10 participants:

| Variable | Mean | Median | Std Dev |
|:---|---:|---:|---:|
| **Height_m** | 1.7424 | 1.7386 | 0.0424 |
| **Weight_kg** | 59.8288 | 61.6886 | 6.4554 |
| **Age** | 32.5000 | 29.5000 | 12.8604 |
| **Grip strength (Grip_kg)** | 26.0000 | 27.0000 | 4.5216 |
| **Frailty (Frailty_binary)** | 0.4000 | 0.0000 | 0.5164 |
| **BMI** | 19.6820 | 19.1850 | 1.7810 |
| **AgeGroup_<30** | 0.5000 | 0.5000 | 0.5270 |
| **AgeGroup_30-45** | 0.3000 | 0.0000 | 0.4830 |
| **AgeGroup_46-60** | 0.2000 | 0.0000 | 0.4216 |
| **AgeGroup_>60** | 0.0000 | 0.0000 | 0.0000 |

---

## 2. Correlation Analysis: Grip Strength vs. Frailty

- **Correlation Coefficient ($r$):** **`-0.4759`** (computed between `Grip_kg` and `Frailty_binary`).
- **Interpretation:**
  - The Pearson correlation coefficient of **`-0.4759`** indicates a **moderate negative association** between grip strength and frailty.
  - This clinical finding demonstrates that female participants with lower hand grip strength are substantially more likely to exhibit symptoms of frailty (`Frailty_binary = 1`), whereas those with higher static grip force exhibit lower frailty incidence (`Frailty_binary = 0`).
  - This empirical result aligns directly with established clinical literature indicating that dynamometer-measured grip strength serves as a key functional biomarker for physical frailty and weakness in adults.