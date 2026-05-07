# student-performance-prediction

A regression study comparing **student academic performance in online vs. offline learning modes** during the COVID-19 transition. Done as part of an MSc project in 2022.

> **Status:** archived academic project (2022). Dataset is a one-time survey snapshot.

## Question

Did the shift to online learning measurably affect academic performance, and which factors (study hours, internet quality, attendance, prior grades, etc.) predict performance under each mode?

## Approach

1. **Data collection** — survey-based dataset (`Dataset/msc2019b.csv`) covering students who experienced both in-person and online instruction.
2. **EDA** — distribution plots, correlation heatmaps, missing-value handling (pandas / seaborn / matplotlib).
3. **Modelling** — two regressors compared:
   - Linear Regression (baseline, interpretable)
   - Random Forest Regressor (non-linear interactions)
4. **Evaluation** — train/test split, error metrics, feature-importance comparison between online and offline regimes.

The notebook is the artifact — 66 cells walking through the full pipeline from raw CSV to model comparison.

## Tech stack

- Python · pandas · numpy
- scikit-learn (LinearRegression, RandomForestRegressor, train_test_split)
- seaborn · matplotlib for visualization
- Jupyter Notebook

## Project layout

```
Code/
└── Student_Performance.ipynb     full analysis notebook (66 cells)
Dataset/
└── msc2019b.csv                   survey data
```

## Reproducing

```bash
pip install pandas numpy scikit-learn seaborn matplotlib jupyter
jupyter notebook Code/Student_Performance.ipynb
```

Run all cells top to bottom.

## Caveats

- **Sample size is small** — survey-driven, single cohort. Results are descriptive of this dataset, not generalizable.
- No hyperparameter search; defaults used for both regressors.
- Class-imbalance / sampling-bias diagnostics are not run.

Treat this as a methodology demo, not a study fit for publication.
