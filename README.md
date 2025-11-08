# Machine Learning for Cardiovascular Risk Stratification: A Comparative Study on the Predictive Power of Engineered Features vs. Minimal WHO/ISH Inputs

**Authors:** Dr. Jannathi L Iti, Anurudh Gangadharan
**Study Location:** Gadag Taluk, North Karnataka

---

Abstract

Title: Machine Learning for Cardiovascular Risk Stratification: A Comparative Study on the Predictive Power of Engineered Features vs. Minimal WHO/ISH Inputs
Authors and Affiliations: Dr. Jannathi L. Iti¹, Anirudh Gangadharan² (Presenting Author)
¹Department of Community Medicine, K.H. Patil Institute of Medical Sciences, Gadag
²MBBS III Phase Part I, K.H. Patil Institute of Medical Sciences, Gadag
Study Location: Gadag Taluk, North Karnataka

Background: Cardiovascular disease (CVD) represents a leading cause of global morbidity and mortality, especially in low- and middle-income countries like India. While the WHO/ISH risk charts provide a minimal-input framework for population-level screening, there exists substantial potential to enhance predictive accuracy using machine learning (ML) and richer feature engineering.

Objective: To quantify the improvement in 10-year CVD risk prediction achieved by ML models utilizing extended and engineered data features compared to the standard 5-factor WHO/ISH minimal inputs.

Methods & Materials: A community-based study was conducted among 700 adults in Gadag Taluk, North Karnataka, using the WHO/ISH risk score as the reference standard. Eight ML algorithms—including Logistic Regression, Random Forest, and XGBoost—were evaluated via 10-fold stratified cross-validation across three feature schemas:

Minimal Set: The 5 standard WHO/ISH inputs (Age, Sex, Systolic BP, Diabetes, Smoking).

Extended (Raw) Set: The Minimal Set plus raw anthropometric and lifestyle variables (e.g., Height, Weight, Waist/Hip circumference).

Extended (Engineered) Set: The Minimal Set plus derived ratios (e.g., BMI, WHR, Per Capita Income).

Performance was measured using the macro-average Area Under the Receiver Operating Characteristic Curve (ROC-AUC).

Results: The Extended (Engineered) Set achieved the highest predictive performance, with XGBoost yielding a macro ROC-AUC of 0.935, outperforming both the Minimal Set (0.871) and the Extended (Raw) Set (0.933). SHAP (SHapley Additive exPlanations) analysis identified Waist-Hip Ratio (WHR) and Body Mass Index (BMI) as two of the top five predictors of 10-year CVD risk, alongside Systolic Blood Pressure, Age, and Diastolic Blood Pressure.

Conclusion: Machine learning models that incorporate engineered features—particularly WHR and BMI—offer a substantial enhancement in 10-year CVD risk stratification compared to the standard 5-factor WHO/ISH approach. The inclusion of these derived anthropometric indicators is critical for developing accurate, population-specific predictive tools in low-resource settings.

Keywords: Cardiovascular Risk; Machine Learning; Feature Engineering; WHO/ISH; WHR; BMI

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
