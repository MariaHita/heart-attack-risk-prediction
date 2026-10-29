# ❤️ Heart Attack Risk Prediction

<p align="center">
  <img src="https://img.shields.io/badge/Project-Data%20Mining-243B64?style=for-the-badge" alt="Data Mining"/>
  <img src="https://img.shields.io/badge/Machine%20Learning-Classification-E9AD35?style=for-the-badge" alt="Classification"/>
  <img src="https://img.shields.io/badge/Dashboard-R%20Shiny-75AADB?style=for-the-badge&logo=r" alt="R Shiny"/>
</p>

<p align="center">
  <b>Exploring machine learning techniques to identify patterns associated with heart attack risk.</b>
</p>

<p align="center">
  <a href="https://ruthwahyu5.shinyapps.io/DashboardDatmin/"><b>🚀 Live R Shiny Dashboard</b></a>
  &nbsp; | &nbsp;
  <a href="https://drive.google.com/file/d/1_2qtpHNsamCPgEZ41XusPTYOuFt6KPfZ/view?usp=drive_link"><b>▶️ Watch Demo</b></a>
</p>

---

## 📌 Project Overview

Heart disease is a major global health concern, making the identification of potential risk factors an important area of data analysis. Machine learning can help uncover patterns in clinical data and support the exploration of factors associated with heart attack risk.

This project applies **data mining and machine learning techniques** to analyze clinical attributes and classify patient conditions. Three approaches are compared: Random Forest, Logistic Regression, and K-Means Clustering.

The project also includes an interactive **R Shiny dashboard** to present the analysis and model results in an accessible visual format.

> **Disclaimer:** This project is intended for academic and educational purposes. Its models are not a substitute for professional medical advice, diagnosis, or clinical assessment.

## 📑 Table of Contents

- [Project Objectives](#-project-objectives)
- [Dataset](#-dataset)
- [Data Preprocessing](#-data-preprocessing)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Feature Selection](#-feature-selection)
- [Modeling Approaches](#-modeling-approaches)
- [Model Evaluation](#-model-evaluation)
- [Key Findings](#-key-findings)
- [Interactive Dashboard](#-interactive-dashboard)
- [Tools and Technologies](#-tools-and-technologies)
- [Team Members](#-team-members)
- [Academic Information](#-academic-information)

## 🎯 Project Objectives

The main objectives of this project are to:

- Explore clinical characteristics associated with heart attack risk.
- Perform data preprocessing and exploratory data analysis.
- Identify relevant features for classification.
- Compare supervised learning models with an unsupervised clustering approach.
- Evaluate model performance using classification metrics and validation techniques.
- Present the analysis through an interactive R Shiny dashboard.

## 📂 Dataset

The project uses the **Heart Attack Analysis and Prediction Dataset**, sourced from Kaggle.

🔗 [Access the dataset on Kaggle](https://www.kaggle.com/datasets/sonialikhan/heart-attack-analysis-and-prediction-dataset)

The dataset contains clinical and demographic attributes, including age, sex, chest pain type, resting blood pressure, cholesterol, maximum heart rate, exercise-induced angina, and other cardiovascular indicators.

### Dataset Features

| Feature | Description |
|---|---|
| `age` | Patient age |
| `sex` | Sex category, encoded as 1 and 0 |
| `cp` | Chest pain type |
| `trtbps` | Resting blood pressure |
| `chol` | Cholesterol level |
| `fbs` | Fasting blood sugar indicator |
| `rest_ecg` | Resting electrocardiographic results |
| `thalach` | Maximum heart rate achieved |
| `exang` | Exercise-induced angina indicator |
| `oldpeak` | ST depression induced by exercise |
| `slp` | Slope of the ST segment |
| `caa` | Number of major vessels |
| `thall` | Thalassemia-related category |
| `output` | Target class in the dataset |

*Note: Feature names follow the naming conventions shown in the project presentation and may differ slightly from other versions of the dataset.*

## 🧹 Data Preprocessing

The preprocessing stage prepares the dataset for statistical exploration and machine learning.

The steps presented in the project include:

1. **Missing Value Checking** — examining the dataset for missing observations.
2. **Data Type Inspection** — checking and adjusting numerical and categorical variable types.
3. **Outlier Checking** — inspecting extreme observations in numerical features.
4. **Categorical Encoding** — converting categorical attributes into model-compatible representations.
5. **Normalization** — scaling numerical features.
6. **Train–Test Split** — separating training and testing data to evaluate predictive performance.

## 📊 Exploratory Data Analysis

Exploratory Data Analysis (EDA) is conducted to understand the distribution of clinical variables and their relationships with the target variable.

The project includes:

- Descriptive statistics and summary indicators.
- Histograms of numerical variables.
- Distribution comparisons across patient outcome groups.
- Categorical feature visualizations.
- A correlation matrix to explore relationships among variables.

The presentation highlights several observations:

- Variables such as age, cholesterol, and maximum heart rate show relatively regular distributions.
- `oldpeak` is strongly right-skewed, with many observations concentrated at lower values.
- Some categories of chest pain, ST-segment slope, and thalassemia appear more frequently in one outcome group than the other.
- The correlation analysis highlights `thall`, `caa`, `slp`, `oldpeak`, and `exng` as variables associated with the target in the reported analysis.

These observations describe patterns in the dataset and should not be interpreted as evidence of causal relationships.

## 🔎 Feature Selection

Feature selection is used to identify variables considered relevant to the classification analysis.

According to the presentation, statistical significance was assessed using a p-value threshold of 0.05. Features meeting the project's selection criteria were retained for subsequent analysis.

This step aims to simplify the model inputs and focus the analysis on variables that show statistical evidence of association under the selected procedure.

## 🤖 Modeling Approaches

Three modeling approaches were evaluated.

### 1. Random Forest

Random Forest is an ensemble learning method that combines multiple decision trees to generate predictions.

In this project, it serves as a supervised classification model for distinguishing patient outcome categories.

### 2. Logistic Regression

Logistic Regression estimates the probability of a categorical outcome based on explanatory variables.

It was evaluated as a classification model and achieved the strongest overall performance among the approaches compared in the project presentation.

### 3. K-Means Clustering

K-Means is an unsupervised learning algorithm that groups observations based on their similarity.

Unlike Random Forest and Logistic Regression, K-Means does not directly learn from labeled outcomes. Its results were evaluated separately to explore the potential of clustering for identifying patterns in the data.

## 📈 Model Evaluation

The project evaluates the models using classification metrics and validation procedures.

### Classification Metrics

- **Accuracy:** The proportion of correctly classified observations.
- **Precision:** The proportion of predicted positive cases that are actually positive.
- **Recall / Sensitivity:** The proportion of actual positive cases correctly identified.
- **Specificity:** The proportion of actual negative cases correctly identified.
- **AUC:** The area under the Receiver Operating Characteristic (ROC) curve.

### Validation Techniques

The presentation reports the use of:

- Repeated Holdout
- K-Fold Cross-Validation
- Silhouette Score for K-Means clustering

These techniques provide additional information about model performance and stability beyond a single evaluation.

## 🏆 Key Findings

### Model Performance Comparison

The presentation reports the following comparison:

| Model | Accuracy | Sensitivity | Specificity | AUC |
|---|---:|---:|---:|---:|
| Random Forest | 73.77% | 84.85% | 60.71% | 88.31% |
| Logistic Regression | 83.61% | 87.88% | 78.57% | 88.85% |
| K-Means (Cluster-to-Class) | 73.77% | 75.76% | 71.43% | 73.59% |

### Logistic Regression as the Preferred Model

Based on the reported model comparison, Logistic Regression achieved the highest accuracy, sensitivity, specificity, and AUC among the three approaches.

The presentation also reports the following validation results:

| Validation Method | Random Forest | Logistic Regression |
|---|---:|---:|
| Repeated Holdout Mean Accuracy | 76.23% | 81.15% |
| K-Fold CV Mean Accuracy | 81.17% | 85.79% |

For K-Means, the reported mean Silhouette Score was approximately **0.1775**, suggesting that the resulting clusters were not clearly separated.

Overall, the results indicate that Logistic Regression performed more consistently than Random Forest in the reported evaluation, while K-Means was more suitable for exploratory grouping than direct individual-level classification.

*Results are reproduced from the group presentation. Performance can vary with data splitting, preprocessing, validation design, and model configuration.*

## 🖥️ Interactive Dashboard

Explore the project through the deployed R Shiny application.

<p align="center">
  <a href="https://ruthwahyu5.shinyapps.io/DashboardDatmin/">
    <img src="https://img.shields.io/badge/Open-Live%20R%20Shiny%20Dashboard-276DC3?style=for-the-badge&logo=r" alt="Open R Shiny Dashboard"/>
  </a>
</p>

The dashboard complements the project presentation by providing an interactive way to explore the heart attack risk analysis.

🎬 **Demo video:** [Watch the R Shiny demonstration on Google Drive](https://drive.google.com/file/d/1_2qtpHNsamCPgEZ41XusPTYOuFt6KPfZ/view?usp=drive_link)

## 🛠️ Tools and Technologies

| Category | Tools / Techniques |
|---|---|
| Programming and dashboard | R Shiny |
| Data preparation | Missing-value checks, encoding, normalization |
| Exploratory analysis | Descriptive statistics, histograms, correlation matrix |
| Supervised learning | Logistic Regression, Random Forest |
| Unsupervised learning | K-Means Clustering |
| Model evaluation | Accuracy, precision, recall, specificity, AUC |
| Validation | Repeated Holdout, K-Fold Cross-Validation |
| Clustering evaluation | Silhouette Score |

## 👩‍💻 Team Members

This project was developed by Group 7:

- **Danella Citra Aldarena**
- **Maria Immaculata Dyah Hita Widowati**
- **Ruth Wahyu Sedjati Priyambodo**

## 🎓 Academic Information

| Detail | Information |
|---|---|
| Course | Data Mining A |
| Program | Undergraduate Statistics |
| Department | Department of Statistics |
| Institution | Institut Teknologi Sepuluh Nopember (ITS) |
| Location | Surabaya, Indonesia |

---

<p align="center">
  <i>Turning clinical data into insights through data mining and machine learning.</i>
</p>
