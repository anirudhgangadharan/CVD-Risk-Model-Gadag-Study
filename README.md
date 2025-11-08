# Machine Learning for Cardiovascular Risk Stratification: A Comparative Study on the Predictive Power of Engineered Features vs. Minimal WHO/ISH Inputs

**Authors:** Dr. Jannathi L Iti, Anurudh Gangadharan
**Study Location:** Gadag Taluk, North Karnataka

---

Abstract:
Title: Machine Learning for Cardiovascular Risk Stratification: A Comparative Study on the Predictive Power of Engineered Features vs. Minimal WHO/ISH Inputs
Authors and Affiliations: Jannathi Ift¹, Anurudh Gangadharan² Presenting author ¹Department of Community Medicine, K H Patil Institute of Medical Sciences, Gadag ²MBBS III Phase Part I, K H Patil Institute of Medical Sciences, Gadag
Background: Cardiovascular disease (CVD) imposes a profound public health and economic burden globally, particularly in low- and middle-income countries like India. While the WHO/ISH risk charts provide a baseline, there is a significant opportunity to improve risk stratification using machine learning (ML) and more comprehensive data.
Objective: To quantify the improvement in 10-year CVD risk prediction by machine learning models using extended and engineered data features compared to the standard 5-factor WHO/ISH minimal inputs.
Methods & Materials: A community-based study was conducted among 700 adults in Gadag Taluk, North Karnataka, using the WHO/ISH risk score as the ground-truth target. Eight ML algorithms (including Logistic Regression, Random Forest, and XGBoost) were rigorously evaluated using 10-fold stratified cross-validation on three distinct feature schemas:
Minimal Set: The 5 standard WHO/ISH inputs (Age, Sex, Systolic BP, Diabetes, Smoking).
Extended (Raw) Set: The minimal inputs plus raw anthropometrics (e.g., Height, Weight, Waist/Hip circumference) and lifestyle factors.
Extended (Engineered) Set: The minimal inputs plus derived ratios (e.g., BMI, WHR, Per Capita Income), replacing their raw components. Performance was primarily assessed using the macro-average Area Under the Receiver Operating Characteristic Curve (ROC-AUC).
Results: The Extended (Engineered) Set achieved the highest predictive performance, with the XGBoost model yielding a macro ROC-AUC of 0.935. This was a significant improvement over the best-performing Minimal Set model (XGBoost, ROC-AUC: 0.871). Crucially, the engineered set also outperformed the Extended (Raw) set (ROC-AUC: 0.933), proving the superior predictive signal of derived ratios. SHAP (SHapley Additive exPlanations) analysis on the top model identified the engineered features WHR (Waist-Hip Ratio) and BMI as two of the top five most significant predictors of 10-year risk, alongside Systolic Blood Pressure, Age, and Diastolic Blood Pressure.
Conclusion: Machine learning models incorporating engineered features, particularly WHR and BMI, offer a substantial improvement in 10-year CVD risk stratification over standard 5-factor models. The study concludes that the inclusion of these derived anthropometrics is critical for developing more accurate and effective CVD prediction tools in this population.
Keywords: Cardiovascular risk; Risk prediction; Machine Learning; Feature Engineering; WHR; BMI; WHO/ISH

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

>L Iti, J., & Gangadharan, A. (2025). CVD-Risk-Model-Gadag-Study: Machine Learning for Cardiovascular Risk Stratification. GitHub Repository. https://github.com/anirudhgangadharan/CVD-Risk-Model-Gadag-Study

---

## LICENSE

This project is licensed under the **MIT License** - see the `LICENSE` file for details.
