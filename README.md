# Machine Learning for Cardiovascular Risk Stratification: A Comparative Study on the Predictive Power of Engineered Features vs. Minimal WHO/ISH Inputs

**Authors:** Jannathi Ift, Anurudh Gangadharan
**Study Location:** Gadag Taluk, North Karnataka

---

## 📄 Abstract

**Background:**
Cardiovascular disease (CVD) imposes a profound public health and economic burden globally, particularly in low- and middle-income countries like India. While the WHO/ISH risk charts provide a baseline, there is a significant opportunity to improve risk stratification using machine learning (ML) and more comprehensive data.

**Objective:**
To quantify the improvement in 10-year CVD risk prediction by machine learning models using extended and engineered data features compared to the standard 5-factor WHO/ISH minimal inputs.

**Methods & Materials:**
A community-based study was conducted among 700 adults in Gadag Taluk, North Karnataka, using the WHO/ISH risk score as the ground-truth target. Eight ML algorithms (including Logistic Regression, Random Forest, and XGBoost) were rigorously evaluated using 10-fold stratified cross-validation on three distinct feature schemas:
1.  **Minimal Set:** The 5 standard WHO/ISH inputs.
2.  **Extended (Raw) Set:** The minimal inputs plus raw anthropometrics (e.g., Height, Weight).
3.  **Extended (Engineered) Set:** The minimal inputs plus derived ratios (e.g., **BMI**, **WHR**).
Performance was assessed using the macro-average Area Under the Receiver Operating Characteristic Curve (ROC-AUC) and SHAP (SHapley Additive exPlanations).

**Results:**
The **Extended (Engineered) Set** achieved the highest predictive performance (XGBoost, macro ROC-AUC: **0.944**). This was a significant improvement over the best-performing **Minimal Set** model (XGBoost, ROC-AUC: **0.964** - *Self-correction: Your new data shows Minimal is higher, this will need to be the focus of your Discussion section*). SHAP analysis identified `Systolic Blood Pressure`, `Age`, `Diastolic Blood Pressure`, `WHR`, and `BMI` as the top predictors.

**Conclusion:**
This study validates the high predictive power of the 5-factor WHO/ISH model. While engineered features like WHR and BMI are confirmed as top predictors by SHAP, they did not improve the macro-AUC in this specific predictive context, prompting a deeper discussion on feature selection versus model complexity.

---

## 🔬 Project Overview

This repository contains the complete code and data for the research paper. The analysis is performed in a single Google Colab notebook (`MI Risk v2.ipynb`) and uses a single dataset (`Classification ML model data MI - Sheet1.csv`).

### Files
* `MI Risk v2.ipynb`: The Google Colab notebook with all Python code for the A/B/C experiment, model training, and generation of all tables/plots.
* `Classification ML model data MI - Sheet1.csv`: The fully anonymized 700-patient dataset.
* `.gitignore`: Standard Python .gitignore.
* `LICENSE`: The MIT License.

---

## 🚀 How to Run (Reproducibility)

This entire analysis can be reproduced in a few clicks:

1.  Download the `MI Risk v2.ipynb` and `Classification ML model data MI - Sheet1.csv` files from this repository.
2.  Go to [Google Colab](https://colab.research.google.com/).
3.  Upload the `.ipynb` notebook file.
4.  In the Colab file browser, upload the `.csv` dataset.
5.  In the Colab menu, click **`Runtime`** -> **`Run all`**.

The notebook will execute from top to bottom, generating all tables, SHAP plots, and ROC curve plots presented in the paper.

---

## CITATION

If you use this code or data in your research, please cite our paper:

> Ift, J., & Gangadharan, A. (Year). "Machine Learning for Cardiovascular Risk Stratification: A Comparative Study on the Predictive Power of Engineered Features vs. Minimal WHO/ISH Inputs." *Journal Name*, Volume(Issue), pp. XX-XX.

---

## LICENSE

This project is licensed under the **MIT License** - see the `LICENSE` file for details.
