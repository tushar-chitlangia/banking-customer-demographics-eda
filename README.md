# Exploratory Data Analysis Pipeline: Banking Data Analysis

## Project Overview
This repository contains a structured, production-grade Exploratory Data Analysis (EDA) and data engineering pipeline executed on a high-volume financial marketing dataset containing 45,216 customer records across 19 feature columns. The project isolates structural customer demographics, evaluates outlier financial distributions, and mathematically maps feature interactions back to a target conversion column to establish foundational patterns before downstream machine learning development.

---

## Technical Architecture & Analytical Workflow

The script builds a reproducible processing workflow leveraging standardized data science packages:

1. **Univariate Demographic Profiling:** Isolated structural client distributions using statistical aggregations (`.describe()`) and visual layouts. Successfully segmented core age profiles (Mean: ~41 years old), major employment variations (Blue-collar: 21.5%, Management: 20.9%), and marital variables via clean Matplotlib/Seaborn structures.
2. **Financial Outlier Detection:** Investigated heavily skewed customer account balances by mapping minimum/maximum limits (-8,019 to 102,127 Euros). Implemented explicit boxplot models (`sns.boxplot`) to isolate and display high-variance asset clusters on the upper economic spectrum.
3. **Temporal Marketing Analytics:** Implemented chronological index ordering across marketing outreach channels. Visualized organizational trends using Seaborn countplots to highlight historical workflow thresholds (e.g., peak contact loads exceeding 13,000 campaigns in May).
4. **Target Variable Binarization:** Mapped the raw text categorical subscription target indicator (`y`) into a computer-readable numeric framework (`df['target_numeric'] = df['y'].map({'yes': 1, 'no': 0})`).
5. **Multi-Variable Pearson Correlation:** Filtered numeric dimensions and executed an explicit `.corr()` function to measure directional feature associations. Constructed an annotated Seaborn Heatmap Matrix (`sns.heatmap`) to mathematically visually present exactly which factors drive conversion parameters.

---

## Verified Project Outcomes & Insights
* **Operational Performance:** Proved that direct conversation length (`duration`) shares the highest structural numeric correlation (0.39) with a successful customer term-deposit sign-up, whereas high-frequency repetitive calling (`campaign`) drops efficiency (-0.07).
* **Consumer Base Mapping:** Established that 60.2% of the bank's targeted consumer base is married, and 98.2% maintain a clean credit profile with zero history of default actions.

---

## Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
