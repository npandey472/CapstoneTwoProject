\# Housing Price Prediction – Capstone Two



\## Project Overview



This project demonstrates a complete end-to-end machine learning workflow for predicting housing sale prices. Using a dataset of ~2,900 housing records, multiple regression models were built, evaluated, and compared to select the most effective model.



\*\*Objective:\*\* Predict `SalePrice` using numerical and categorical housing features.



\*\*Outcome:\*\* A Random Forest Regressor was identified as the best-performing model based on MAPE and R² metrics.



---



\## Table of Contents



1\. \[Dataset](#dataset)

2\. \[Data Preprocessing](#data-preprocessing)

3\. \[Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)

4\. \[Models Implemented](#models-implemented)

5\. \[Model Evaluation](#model-evaluation)

6\. \[Final Model](#final-model)

7\. \[Visualizations](#visualizations)

8\. \[Usage](#usage)

9\. \[Future Work](#future-work)

10\. \[References](#references)



---



\## Dataset



\- Source: https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fmedia.geeksforgeeks.org%2Fwp-content%2Fuploads%2F20240905183434%2FHousePricePrediction.xlsx\&wdOrigin=BROWSELINK

\- Records: ~2,900

\- Features: Mix of numerical (LotArea, HouseAge, OverallCond) and categorical (MSZoning, BldgType, Exterior1st)

\- Target: `SalePrice`



\*\*Note:\*\* Dataset preprocessing includes handling missing values, one-hot encoding for categorical variables, and feature scaling for certain models (e.g., SVR).



---



\## Data Preprocessing



\- \*\*Missing values:\*\* Imputed using mean for numeric columns

\- \*\*Feature engineering:\*\* Created `HouseAge` and other derived features

\- \*\*Encoding:\*\* One-hot encoding for categorical variables

\- \*\*Scaling:\*\* StandardScaler applied to SVR features

\- \*\*Train/Test split:\*\* 80% train / 20% test



---



\## Exploratory Data Analysis (EDA)



\*\*Key Findings:\*\*



\- Sale prices are right-skewed with high-value outliers

\- Weak linear correlations with the target variable

\- Supports use of tree-based models over linear regression



📊 Visualizations included in the report:

\- Distribution of Sale Prices

\- Correlation Heatmap



---



\## Models Implemented



| Model | Description |

|-------|-------------|

| Linear Regression | Baseline linear model |

| Support Vector Regression (SVR) | Tuned with RBF kernel |

| Random Forest Regressor | Handles non-linear relationships, provides feature importance |

| Random Forest (Log-Transformed Target) | Attempts to normalize skew |

| CatBoost Regressor | Gradient boosting with native categorical handling |



---



\## Model Evaluation



| Model | R² | MAPE |

|-------|----|------|

| Linear Regression | — | 20% |

| SVR | ~0.00 | ~18% |

| Random Forest | \*\*~0.30\*\* | ~20% |

| RF (Log) | ~0.26 | ~20% |

| CatBoost | ~0.23 | ~22% |



\*\*Observation:\*\* Random Forest provides the best combination of performance and interpretability.



---



\## Final Model



\- \*\*Selected Model:\*\* Random Forest Regressor

\- \*\*Reason:\*\* Highest R², interpretable feature importance, robust performance

\- \*\*Top Features:\*\* LotArea, HouseAge, OverallCond, MSSubClass



\*\*Limitation:\*\* ~70% of variance remains unexplained due to missing critical predictors.



---



\## Visualizations



\- \*\*Figure 1:\*\* Distribution of Sale Prices (skewed, high-value outliers)

\- \*\*Figure 2:\*\* Correlation heatmap (weak linear relationships)

\- \*\*Figure 3:\*\* Actual vs Predicted prices (Random Forest)

\- \*\*Figure 4:\*\* Feature importance (Random Forest)



> Figures are referenced in the final report PDF using APA/IEEE-compliant captions.



---



\## Usage



To run this project:



1\. Clone the repository:



```bash

git clone https://github.com/npandey472/CapstoneTwoProject.git

cd CapstoneTwoProject

Install required packages:



bash

pip install -r requirements.txt

Run Jupyter Notebooks:



bash

jupyter notebook

Access results:



Capstone\\\_Final\\\_Report.pdf → Final report with figures and analysis



model\\\_metrics.csv → All model evaluation metrics



Future Work

Include additional features like neighborhood data, total rooms, and quality metrics



Test Gradient Boosting (XGBoost, LightGBM)



Deploy model as a web application or API for predictions



References

Scikit-learn documentation: https://scikit-learn.org



Géron, A. (2019). Hands-On Machine Learning with Scikit-Learn, Keras \\\& TensorFlow.



APA/IEEE Style Guidelines for Figures and References



Repository Structure:



markdown

CapstoneTwoProject/

│

├── notebooks/

│   ├── data\\\_preprocessing.ipynb

│   ├── eda.ipynb

│   ├── model\\\_building.ipynb

│

├── Capstone\\\_Final\\\_Report.pdf

├── model\\\_metrics.csv

├── README.md

├── requirements.txt

└── figures/

\&nbsp;   ├── figure1\\\_distribution.png

\&nbsp;   ├── figure2\\\_correlation.png

\&nbsp;   ├── figure3\\\_rf\\\_predictions.png

\&nbsp;   └── figure4\\\_rf\\\_feature\\\_importance.png

GitHub Repository:

https://github.com/npandey472/CapstoneTwoProject


