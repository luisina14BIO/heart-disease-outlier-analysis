# Heart Disease – Exploratory Data Analysis

## Project Overview

This project presents an Exploratory Data Analysis (EDA) of the **Heart Disease – Cleveland dataset**, obtained from the UCI Machine Learning Repository.

The analysis focuses on exploring categorical and numerical variables, understanding their distributions, calculating descriptive statistics, and identifying potential outliers using the Interquartile Range (IQR) method.

The main objective is to characterize the dataset through statistical analysis and visualization, while evaluating the presence and treatment of extreme observations.

## Dataset

**Source:** [UCI Machine Learning Repository – Heart Disease](https://archive.ics.uci.edu/dataset/45/heart+disease)

**Dataset:** Cleveland subset (`processed.cleveland.data`)

The dataset contains:
- 303 patient records.
- 14 original variables.
- Demographic and clinical information related to cardiovascular disease.

### Main variables

| Variable | Description |
|---|---|
| `age` | Age of the patient |
| `sex` | Sex |
| `cp` | Chest pain type |
| `trestbps` | Resting blood pressure |
| `chol` | Serum cholesterol |
| `fbs` | Fasting blood sugar |
| `restecg` | Resting electrocardiographic results |
| `thalach` | Maximum heart rate achieved |
| `exang` | Exercise-induced angina |
| `oldpeak` | ST depression induced by exercise |
| `slope` | Slope of the peak exercise ST segment |
| `ca` | Number of major vessels |
| `thal` | Thalassemia |
| `num` | Heart disease diagnosis (0–4) |

The original target variable `num` was also used to create a binary classification indicating the presence or absence of heart disease.

## Project Objectives

- Explore categorical and numerical variables.
- Analyze categorical distributions through barplots.
- Calculate descriptive statistics, skewness and kurtosis.
- Visualize numerical distributions using boxplots and violin plots.
- Identify potential outliers using the IQR method.
- Evaluate and document the treatment of detected outliers.

## Methodology

The analysis was developed using Python and the following stages:

1. **Data loading and exploration:** inspection of dataset dimensions, variable types, missing values and duplicate records.
2. **Data preparation:** interpretation of missing values and creation of descriptive labels for categorical variables.
3. **Categorical analysis:** visualization of patient distributions by sex, chest pain type and heart disease status.
4. **Numerical analysis:** calculation of descriptive statistics, skewness and kurtosis for five numerical variables.
5. **Data visualization:** construction of boxplots and violin plots to examine distributions and potential extreme values.
6. **Outlier detection:** application of the Interquartile Range (IQR) method to identify observations outside the defined limits.
7. **Interpretation:** evaluation of detected outliers and documentation of the decision regarding their treatment.

## Main Findings

The analysis identified several relevant patterns:

- The dataset contains 303 records and 14 original variables.
- Six missing values were identified: four in `ca` and two in `thal`.
- No duplicate records were found.
- `chol` and `oldpeak` showed the strongest positive skewness.
- The IQR method identified 20 outlier observations across four numerical variables, corresponding to 19 distinct records.

### Outlier detection results

| Variable | Outliers detected |
|---|---:|
| `age` | 0 |
| `trestbps` | 9 |
| `chol` | 5 |
| `thalach` | 1 |
| `oldpeak` | 5 |
| **Total detections** | **20** |

### Outlier treatment

All detected outliers were retained.

Since the dataset contains clinical observations, extreme values may represent valid patient measurements rather than data entry errors. No sufficient evidence was found to justify removing or transforming these observations.

Missing values were also retained without imputation or deletion, given their low proportion in the dataset.

## Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Structure

```text
heart-disease-outlier-analysis/
│
├── data/
│   └── raw/
│       └── processed.cleveland.data
│
├── notebooks/
│   └── heart_disease_analysis.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/heart-disease-outlier-analysis.git
```

### 2. Install the dependencies

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

Open Jupyter Notebook or JupyterLab from the project's `notebooks` directory and run:

`heart_disease_analysis.ipynb`

The notebook uses relative paths to access the dataset stored in `data/raw/`.

Run the notebook cells sequentially to reproduce the analysis.

## Author

**Luisina Schwab**

Data Science | Biology | Bioinformatics
