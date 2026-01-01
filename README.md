# Predictive Modeling of Breast Cancer Metastasis using Clinical Genomics

## 📌 Project Overview
Metastasis is the primary cause of cancer-related mortality. This project leverages the **MSK-Impact (2018)** clinical dataset to develop a robust machine learning pipeline capable of predicting whether a breast cancer sample is **Primary** or **Metastastic** based on clinical and biological features.

The core focus of this work was to maintain **scientific integrity** by identifying and removing "data leakage" features, ensuring the model learns from biological predictors rather than administrative or post-event data.

## 📊 Dataset Specifications
- **Source:** Memorial Sloan Kettering Cancer Center (MSK), via cBioPortal.
- **Samples:** 1,918 unique clinical records.
- **Features:** 50+ variables including ER/PR/HER2 status, Mutation Count, Diagnosis Age, and Tumor Grade.
- **Class Distribution:** - Metastasis (Target: 1): 1,000 samples
  - Primary (Target: 0): 918 samples

## 🛠 Project Structure
The repository is organized into a modular pipeline:

1.  **`01_load_and_parse_msk_breast_cancer_cell`**: Loading raw TSV data and initial parsing.
2.  **`02_preprocessing_and_feature_engineering`**: Handling missing values (Median/Mode imputation), standardizing feature names, and Label Encoding (**Metastasis=1, Primary=0**).
3.  **`03_model_training_and_evaluation`**: Visualizing feature distributions and identifying class imbalances.
4.  **`04_final_model_and_insights`**: Addressing **Data Leakage**. Features like 'Site of Sample' and 'Survival Months' were removed to ensure a realistic predictive scenario.
5.  **`05_visualizations_and_reporting`**: Final training using **Random Forest** and performance visualization.
6.  **`06_prediction_demo`**: A script for predicting metastasis risk for new, hypothetical patient profiles.

## 📈 Model Performance
The final model achieved high reliability after rigorous feature selection:
- **Accuracy:** 85%
- **ROC-AUC Score:** 0.93
- **Recall (Metastasis):** 0.93 (Crucial for clinical screening to minimize False Negatives).



## 🧬 Key Findings (Feature Importance)
The model identified the following features as the strongest biological predictors of metastasis:
1.  **Invasive Carcinoma Diagnosis Age**
2.  **Mutation Count** (Tumor Mutational Burden)
3.  **Overall Patient Receptor Status**
4.  **Primary Tumor Grade**



## 🚀 How to Run
1. Clone the repository.
2. Install requirements: `pip install pandas scikit-learn seaborn matplotlib`.
3. Run the notebooks in sequential order.

## 🎓 Author
**[Mobin Zamani]**
*Aspiring Data Scientist / Researcher in Bioinformatics*
