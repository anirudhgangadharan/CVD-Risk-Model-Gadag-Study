# World Health Organization Cardiovascular Risk Assessment Using Machine Learning: A Comparative Study of Minimal vs. Extended Feature Models

[![Language](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Authors:** Jannathi Ift¹, Anurudh Gangadharan²
**Affiliations:** ¹K H Patil Institute of Medical Sciences, Gadag; ²MBBS III Phase Part I, K H Patil Institute of Medical Sciences, Gadag

---

##  Abstract

**Objective:**
To compare the cardiovascular risk prediction of a Minimal machine learning model (based on 5 WHO/ISH factors) with an Extended Feature Model (including anthropometrics, lifestyle factors, etc.) in estimating 10-year risk of major cardiovascular events.

**Methods:**
A community-based study was conducted among 700 adults in Gadag Taluk, North Karnataka, using the WHO/ISH risk score as the ground-truth target. Eight ML algorithms (including XGBoost, Random Forest, and SVM) were rigorously evaluated using 10-fold stratified cross-validation on three distinct feature schemas:
1.  **Minimal Set:** The 5 standard WHO/ISH inputs (Age, Sex, SBP, Diabetes, Smoking).
2.  **Extended (Raw) Set:** The Minimal Set plus raw data (e.g., Height, Weight, Income).
3.  **Extended (Engineered) Set:** The Minimal Set plus derived ratios (e.g., BMI, WHR).
Performance was primarily assessed using the macro-average Area Under the Receiver Operating Characteristic Curve (ROC-AUC).

**Results:**
The study produced a clear and counter-intuitive finding. The **`Minimal Set`** (5 WHO/ISH inputs) achieved the highest predictive performance, with the **XGBoost** model yielding a macro ROC-AUC of **0.9641**. This significantly outperformed the best models from the **`Extended (Raw) Set`** (XGBoost, AUC: 0.9473) and the **`Extended (Engineered) Set`** (XGBoost, AUC: 0.9443).

**Conclusion:**
Our initial hypothesis that an extended-feature model would be superior was disproven. For the specific task of predicting the WHO/ISH score (which is itself derived from the 5 minimal features), the 5-factor model represents the pure, optimal signal. Adding extra features, even clinically relevant ones like BMI and WHR, acted as statistical noise and degraded model performance. This study validates the parsimony and robustness of the 5-factor WHO/ISH framework.

---

##  Key Findings

* **"Less is More"**: The 5-factor `Minimal Set` (AUC **0.9641**) was statistically superior to the `Extended (Engineered)` set (AUC **0.9443**).
* **Signal vs. Noise**: Adding features not used to create the target variable (the WHO/ISH score) confused the model and worsened its performance.
* **Champion Model**: The best-performing model for this task is **XGBoost** trained *only* on the **5 minimal features**.

---

##  Repository Contents

* `MI Risk v2.ipynb`: The Google Colab notebook with all Python code for the A/B/C experiment, model training, and generation of all tables/plots.
* `Classification ML model data MI - Sheet1.csv`: The fully anonymized 700-patient dataset.
* `cv_risk_minimal_app.joblib`: The saved, deployable "champion" model (XGBoost-Minimal).
* `app.py`: (Optional) A Python file to deploy the Gradio web app.
* `.gitignore`: Standard Python gitignore.
* `LICENSE`: The MIT License.

---

##  How to Run (Reproducibility)

This entire analysis can be reproduced in a few clicks:

1.  Clone or download this repository.
2.  Go to [Google Colab](https://colab.research.google.com/).
3.  Upload the `MI Risk v2.ipynb` notebook and the `Classification ML model data MI - Sheet1.csv` dataset.
4.  In the Colab menu, click **`Runtime`** -> **`Run all`**.

The notebook will execute from top to bottom, training all 24 models (8 algorithms x 3 sets) and regenerating all tables, SHAP plots, and ROC curve plots presented in the paper.

---

## CITATION

This repository and its contents are the basis for a research paper currently in preparation:

> Ift, J., & Gangadharan, A. (2024). "World Health Organization Cardiovascular Risk Assessment Using Machine Learning: A Comparative Study of Minimal vs. Extended Feature Models." *Unpublished manuscript*.

If you use this code or data, **please cite this GitHub repository directly** until the final paper is published:

> Dr. Jannathi L Iti, & Anirudh Gangadharan. (2024). *CVD-Risk-Model-Gadag-Study: Machine Learning for Cardiovascular Risk Stratification*. GitHub Repository. https://github.com/anirudhgangadharan/CVD-Risk-Model-Gadag-Study

---

## LICENSE

This project is licensed under the **MIT License** - see the `LICENSE` file for details.
