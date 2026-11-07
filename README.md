# ICU Mortality Prediction Using Machine Learning

**Effat University · Computer Science · 2026**  
Python, pandas, scikit-learn, XGBoost, Jupyter Notebook

A team project exploring mortality-risk classification using structured ICU records. We compared supervised learning models, investigated class imbalance and label noise, and examined how classification thresholds affect the detection of mortality cases.

## Project highlights

- Worked with a public dataset of **15,000 ICU records** and 24 initial variables.
- Compared **eight classifiers**, including Logistic Regression, Random Forest, SVM, and XGBoost.
- Explored data preprocessing, feature selection, class balancing, model evaluation, and robustness under noisy labels.
- Focused the final analysis on seven predictors: ventilation requirement, vasopressor use, sepsis status, APACHE and SOFA scores, comorbidity score, and age.

### Model evaluation

For one balanced evaluation experiment, tuned XGBoost at a **0.35 threshold** reached **88.5% recall**, **67.8% F1-score**, and **0.641 ROC-AUC**. The higher recall came with more false positives. These are experimental results, not measures of clinical performance.

![Tuned XGBoost confusion matrix](images/confusion_matrix.png)

See the [notebook](notebook/ML_Final_Project_Code.ipynb) for the different experiments and [evaluation notes](REPRODUCIBILITY.md) for important methodological qualifications.

## Project files

| Resource | Description |
| --- | --- |
| [Machine Learning notebook](notebook/ML_Final_Project_Code.ipynb) | Data exploration, model training, threshold experiments, and evaluation |
| [Figures](images/) | Class distribution, ROC curve, confusion matrix, and feature importance |
| [Python requirements](requirements.txt) | Main packages used in the notebook |
| [Dataset](data/) | Source and download instructions |
| [Prototype demonstration](prototype/) | Recorded interface demonstration |
| [Additional project files](ASSET_SOURCES.md) | Original reports, slides, poster, and video |

## Getting started

1. Clone or download this repository.
2. Install the required packages: `python -m pip install -r requirements.txt`.
3. Download the [ICU Patient Monitoring and Mortality Prediction dataset](https://www.kaggle.com/datasets/jayjoshi37/icu-patient-monitoring-and-mortality-prediction).
4. Open [ML_Final_Project_Code.ipynb](notebook/ML_Final_Project_Code.ipynb) with Jupyter Notebook or Google Colab. Follow the notebook's data-loading instructions and select the relevant experiment.

The notebook contains multiple experimental versions and has not been independently verified as a complete reproduction of every reported result.

## Related conference paper

A **separate Data Science manuscript** developed from the same research topic was accepted to **AICities at the 23rd ACS/IEEE International Conference on Computer Systems and Applications (AICCSA 2026)**, paper **#2302**:

[*ICU Mortality Prediction Using Machine Learning: A Practical Framework for Risk Stratification*](https://aiccsa.net/AICCSA2026/papers.php)  
**Sarah Elshiaty, Mashael Saeed, Seifeldin Elshiaty, and Passent Elkafrawy.**

The paper was presented at the conference by video. AICCSA states that accepted and presented papers are submitted for consideration for IEEE Xplore publication, subject to final publication requirements. **An individual IEEE Xplore record has not yet been verified.** The [Data Science project repository](https://github.com/SarahElshiaty/ICU-Mortality-Data-Science) contains the related Data Science materials; the notebook here belongs to the Machine Learning course project.

## Team

**Sarah Elshiaty · Mashael Saeed · Seifeldin Elshiaty**

This was a collaborative academic project. The [original shared repository](https://github.com/M1sh13l/ICU-Mortality-Prediction-ML) retains the original development commits, including contributions recorded under Sarah's and Mashael's names. See [Contributors](CONTRIBUTORS.md).

*Academic research only. This model has not been externally or clinically validated and is not intended for medical decision-making.*
