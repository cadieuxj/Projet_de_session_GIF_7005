# Projet de Session GIF-7005: Fetal Health Classification

## 📋 Project Overview

This repository contains a comprehensive dataset and analysis project for fetal health classification, developed as part of the GIF-7005 course session project. The project focuses on classifying fetal health status using Cardiotocography (CTG) data to help prevent child and maternal mortality.

## 🎯 Objective

The main objective of this project is to analyze and classify fetal health outcomes based on cardiotocogram examinations. Cardiotocography is a technical means of recording the fetal heartbeat and uterine contractions during pregnancy, which is crucial for assessing fetal well-being.

## 📊 Dataset Description

### Data Source
The dataset (`fetal_health.csv`) contains CTG exam results with 2,126 records of fetal cardiotocograms, classified by expert obstetricians into three fetal health states.

### Target Variable
- **fetal_health**: Classification of fetal health state
  - `1.0` = Normal
  - `2.0` = Suspect
  - `3.0` = Pathological

### Features (21 variables)

#### Baseline Features
- **baseline value**: Baseline Fetal Heart Rate (FHR)
- **accelerations**: Number of accelerations per second
- **fetal_movement**: Number of fetal movements per second
- **uterine_contractions**: Number of uterine contractions per second
- **light_decelerations**: Number of light decelerations per second
- **severe_decelerations**: Number of severe decelerations per second
- **prolongued_decelerations**: Number of prolonged decelerations per second

#### Short-term Variability Features
- **abnormal_short_term_variability**: Percentage of time with abnormal short-term variability
- **mean_value_of_short_term_variability**: Mean value of short-term variability

#### Long-term Variability Features
- **percentage_of_time_with_abnormal_long_term_variability**: Percentage of time with abnormal long-term variability
- **mean_value_of_long_term_variability**: Mean value of long-term variability

#### Histogram Features
- **histogram_width**: Width of the FHR histogram
- **histogram_min**: Minimum value of the FHR histogram
- **histogram_max**: Maximum value of the FHR histogram
- **histogram_number_of_peaks**: Number of peaks in the FHR histogram
- **histogram_number_of_zeroes**: Number of zeros in the FHR histogram
- **histogram_mode**: Mode of the FHR histogram
- **histogram_mean**: Mean of the FHR histogram
- **histogram_median**: Median of the FHR histogram
- **histogram_variance**: Variance of the FHR histogram
- **histogram_tendency**: Tendency of the FHR histogram

## 📁 Repository Structure

```
Projet_de_session_GIF_7005/
│
├── Data/
│   └── fetal_health.csv          # Main dataset (2,126 records)
│
└── README.md                       # Project documentation (this file)
```

## 🚀 Getting Started

### Prerequisites
To work with this dataset, you may need:
- Python 3.x with libraries such as:
  - pandas (for data manipulation)
  - numpy (for numerical operations)
  - scikit-learn (for machine learning)
  - matplotlib/seaborn (for visualization)
- Or R with appropriate packages
- Or any data analysis tool that can read CSV files

### Loading the Data

#### Python Example
```python
import pandas as pd

# Load the dataset
df = pd.read_csv('Data/fetal_health.csv')

# Display basic information
print(df.head())
print(df.info())
print(df['fetal_health'].value_counts())
```

#### R Example
```r
# Load the dataset
fetal_data <- read.csv('Data/fetal_health.csv')

# Display basic information
head(fetal_data)
summary(fetal_data)
table(fetal_data$fetal_health)
```

## 📈 Potential Analyses

This dataset can be used for various machine learning and statistical analyses:

1. **Classification Models**: Build predictive models to classify fetal health status
   - Decision Trees
   - Random Forests
   - Support Vector Machines (SVM)
   - Neural Networks
   - Logistic Regression

2. **Exploratory Data Analysis (EDA)**:
   - Feature correlation analysis
   - Distribution analysis of variables
   - Class imbalance investigation
   - Feature importance evaluation

3. **Data Preprocessing**:
   - Feature scaling/normalization
   - Handling class imbalance (if present)
   - Feature selection
   - Dimensionality reduction (PCA, t-SNE)

4. **Model Evaluation**:
   - Cross-validation
   - Confusion matrix analysis
   - Precision, Recall, F1-Score
   - ROC curves and AUC

## 📚 Background Information

### Why is this Important?
Reduction of child mortality is reflected in several United Nations' Sustainable Development Goals and is a key indicator of human progress. Cardiotocography (CTG) is a simple and cost-effective option for assessing fetal health, allowing healthcare professionals to take action to prevent child and maternal mortality.

### Medical Context
CTG interpretation requires expert knowledge and experience. Automated systems that can accurately classify fetal health can:
- Assist medical professionals in decision-making
- Provide early warning systems
- Help in resource-limited settings
- Reduce human error in interpretation

## 🎓 Course Information

- **Course**: GIF-7005
- **Project Type**: Session Project
- **Focus**: Data Analysis and Machine Learning for Healthcare

## 📝 License and Attribution

Please ensure to properly cite and attribute the original data source when using this dataset for research or educational purposes.

## 🤝 Contributing

This is an academic project. If you have suggestions or improvements, feel free to open an issue or submit a pull request.

## 📧 Contact

For questions regarding this project, please contact the repository owner.

---

**Note**: This dataset is intended for educational and research purposes as part of the GIF-7005 course curriculum.