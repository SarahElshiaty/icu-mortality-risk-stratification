# Experiments and reproducibility

The [notebook](notebook/ML_Final_Project_Code.ipynb) contains several stages of the Machine Learning course project: data exploration, preprocessing, comparison of eight classifiers, threshold experiments, and robustness analysis.

## Dataset and dependencies

- Dataset: [ICU Patient Monitoring and Mortality Prediction](https://www.kaggle.com/datasets/jayjoshi37/icu-patient-monitoring-and-mortality-prediction), 15,000 records.
- Core libraries: pandas, NumPy, scikit-learn, XGBoost, matplotlib, seaborn. See [requirements.txt](requirements.txt). Some notebook cells also use SciPy and interactive Jupyter tools.
- Original CSV: [team repository](https://github.com/M1sh13l/ICU-Mortality-Prediction-ML/tree/main/data).

## Interpreting the results

The accepted **Data Science conference manuscript** reports tuned XGBoost at threshold **0.35** with recall **0.885**, F1 **0.678**, and ROC-AUC **0.641** on a balanced evaluation sample. The related **Machine Learning notebook** includes additional experiments and a threshold value of **0.413** in one intermediate section. These results should not be conflated.

The repository has not been independently rerun end to end to verify numerical agreement with the conference manuscript.

## Limitations

- The dataset is public secondary data, not a hospital deployment.
- The paper reports results on a balanced evaluation sample, which differs from the original class distribution.
- Threshold selection and evaluation in the paper were performed on the same evaluation split; further validation would be needed.
- No external clinical validation was performed.
- Features may include information recorded during the ICU stay, so the model should not be described as an admission-time early warning tool.

The work is an academic retrospective risk-stratification study, not a diagnostic system.
