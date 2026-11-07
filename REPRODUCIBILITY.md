# Reproducibility and research limitations

## What's actually available

- [Original research notebook](notebook/ML_Final_Project_Code.ipynb): multiple experiments and analysis stages, rather than a minimal independently verified production pipeline.
- [Requirements](requirements.txt): pandas, numpy, scikit-learn, xgboost, matplotlib, seaborn. The notebook also imports other packages (including SciPy and interactive notebook tools), which may require installing them separately.
- [Public dataset source](https://www.kaggle.com/datasets/jayjoshi37/icu-patient-monitoring-and-mortality-prediction): 15,000 structured ICU records. The CSV is hosted in the [original team repository](https://github.com/M1sh13l/ICU-Mortality-Prediction-ML/tree/main/data).
- Visualizations are in [images](images/). Large paper/poster/presentation and video files remain linked from the original team repository.

## How to run

1. Clone/download the repository.
2. Install `python -m pip install -r requirements.txt`.
3. Open `notebook/ML_Final_Project_Code.ipynb` in Jupyter or Google Colab.
4. Download the original dataset and follow the notebook's upload/path instructions.
5. Select the experimental stage deliberately; the notebook contains several independent model comparisons and exploratory variants.

**Unverified:** a fully clean, end-to-end rerun that exactly reproduces all the accepted manuscript's reported results.

## Published-study configuration vs. notebook experiments

The accepted manuscript reports tuned XGBoost with **threshold 0.35**, reaching recall **0.885**, F1 **0.678**, and ROC-AUC **0.641** on a balanced experimental evaluation set. The notebook contains intermediate work with a different threshold (including **0.413** in one code cell). Do not treat all notebook cells as if they refer to the paper's final run.

The correct technical improvement would be to isolate the final configuration, rerun it, record the dataset checksum and environment versions, and distinguish validation-based threshold selection from untouched test-set evaluation.

## Interpretation limits

- Data are from a public secondary dataset, **not a hospital deployment**.
- The reported metrics come from a **balanced study distribution**, unlike the original prevalence.
- No external cohort was used for clinical validation.
- The available features may have been recorded during the ICU stay; this is **not demonstrated to be an admission-time early-warning model**.
- The accepted manuscript acknowledges that threshold selection and performance reporting used the same evaluation set.
- A high recall came with substantial false-positive predictions; it should not be presented as clinically validated screening effectiveness.

These results support an **academic retrospective risk-stratification experiment** only.
