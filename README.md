# ICU Mortality Prediction — Machine Learning

**Research project | Effat University | 2026**  
Python · scikit-learn · XGBoost · exploratory data analysis · classification

An academic machine-learning study of **retrospective ICU mortality-risk classification** using a public structured dataset. The team compared eight classifiers, examined class imbalance and decision thresholds, and reported interpretable model-evaluation results. This repository is a **maintained standalone presentation of collaborative work**, not a claim of solo authorship.

> **Conference recognition:** [*ICU Mortality Prediction Using Machine Learning: A Practical Framework for Risk Stratification*](https://aiccsa.net/AICCSA2026/papers.php) — accepted to the **AICities track, ACS/IEEE AICCSA 2026**, paper **#2302**. Acceptance is confirmed; IEEE Xplore publication/indexing is **not claimed**.

## Project at a glance

| | |
|---|---|
| **Task** | Binary retrospective ICU mortality classification |
| **Data** | Public Kaggle dataset: 15,000 patient records, 24 initial variables |
| **Approach** | Data exploration, preprocessing, feature selection, class-imbalance analysis, eight classifier comparisons, threshold evaluation |
| **Final study features** | 7: ventilation, vasopressor use, sepsis, APACHE, SOFA, comorbidity, age |
| **Status** | Completed academic experiments and prototype; **not deployed or clinically validated** |

## Results reported in the accepted manuscript

The reported tuned XGBoost model at **threshold 0.35** was evaluated on a **balanced experimental set**.

| Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---:|---:|---:|---:|---:|
| 0.580 | 0.550 | **0.885** | 0.678 | 0.641 |

**Interpretation:** Higher recall meant more mortality cases were flagged in this experiment, accompanied by substantial false positives. These numbers do **not** establish real-world hospital performance. The study also acknowledges limitations in evaluation design and external validity. See [Reproducibility notes](REPRODUCIBILITY.md).

## Explore the project

| Material | Open |
|---|---|
| Analysis and experiments | [Jupyter notebook](notebook/ML_Final_Project_Code.ipynb) |
| Dataset and source | [Dataset folder](data/) · [original Kaggle source](https://www.kaggle.com/datasets/jayjoshi37/icu-patient-monitoring-and-mortality-prediction) |
| Evaluation charts | [Images](images/) |
| Research manuscript | [Paper](paper/) |
| Poster and slides | [Poster](poster/) · [Presentation](presentation/) |
| Recorded interface demo | [Prototype](prototype/) |
| Team contribution details | [Contributors](CONTRIBUTORS.md) |
| Reproduction and limitations | [Reproducibility notes](REPRODUCIBILITY.md) |

## Run the notebook

The deliverable is a research **Jupyter/Colab notebook**, not a production-ready API.

1. Download or clone this repository.
2. Install Python 3, then run `python -m pip install -r requirements.txt`.
3. Open `notebook/ML_Final_Project_Code.ipynb` in Jupyter or Google Colab.
4. Follow its data-loading cells. If prompted to upload data, supply `data/ICU_Patient_Monitoring_Mortality_Prediction_15000.csv`.
5. Run the desired experiment and read its outputs. The notebook includes exploratory stages; **not every stage corresponds to the accepted manuscript's final experiment**.

A clean, end-to-end reproduction of the final manuscript results has **not** been independently verified for this repository. We do not present these figures as a passing automated test.

## Team and provenance

This work was developed collaboratively by **Sarah Elshiaty, Mashael Saeed, and Seifeldin Elshiaty**. The conference manuscript additionally lists **Passent Elkafrawy** as co-author.

- [Original team repository — Mashael Saeed](https://github.com/M1sh13l/ICU-Mortality-Prediction-ML)
- [Sarah's retained fork](https://github.com/SarahElshiaty/ICU-Mortality-Prediction-ML)
- [Original Git commit history](https://github.com/M1sh13l/ICU-Mortality-Prediction-ML/commits/main)

The original commit log includes changes authored under **Sarah Elshiaty** and **Mashael Saeed**. This standalone repository preserves source-file credit and links to that history; its own commits for copying/organizing the files **must not be interpreted as the complete original development history**. See [CONTRIBUTORS.md](CONTRIBUTORS.md).

## Responsible use and licensing

This is a retrospective **academic research project**, not a diagnosis, triage, or clinical-decision tool. No external clinical validation or production deployment is claimed. The dataset is attributed to its public Kaggle source; downstream reuse remains subject to the dataset's terms. **No open-source license is asserted for team code** without the collaborators' agreement.
