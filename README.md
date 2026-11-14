#  Titanic Survival Prediction Using Feature Engineering

##  Project Overview

This project focuses on predicting passenger survival on the Titanic using Machine Learning and Feature Engineering techniques.

The project uses Python, Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn to perform data cleaning, feature engineering, data preprocessing, model training, and performance evaluation.

A Random Forest Classifier is implemented to predict whether a passenger survived the Titanic disaster.

##  Project Objectives

- Load and explore the Titanic dataset.
- Perform data cleaning and preprocessing.
- Create meaningful features using Feature Engineering.
- Encode categorical variables.
- Scale numerical variables.
- Train a Random Forest Classification model.
- Evaluate model performance using accuracy and classification metrics.
- Analyze feature importance.
- Generate a project report.

##  Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

##  Project Structure

```text
Titanic-Survival-Prediction-Feature-Engineering/
│
├── Titanic_Survival_Feature_Engineering.ipynb
├── Titanic_Feature_Engineering_Report.txt
├── cleaned_titanic_dataset.csv
├── feature_importance.csv
├── titanic_survival_model.pkl
```

##  Dataset

The project uses the Titanic passenger training dataset.

Dataset source:
[Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic/data)

The training dataset contains passenger information such as:

- Passenger class
- Passenger age
- Gender
- Number of siblings and spouses
- Number of parents and children
- Ticket fare
- Cabin information
- Embarkation port
- Survival status

The target variable is `Survived`:

- `0` – Did not survive
- `1` – Survived

##  Project Implementation

### 1. Data Loading and Exploration

- Load the Titanic dataset using Pandas.
- Examine dataset dimensions and column information.
- Identify missing values and duplicate records.
- Analyze the target variable distribution.

### 2. Data Cleaning

- Remove duplicate records.
- Handle missing target values.
- Validate survival labels.
- Prepare the dataset for machine learning.

### 3. Feature Engineering

Three additional features are created:

**FamilySize**

Calculates the total family size of a passenger.

`FamilySize = SibSp + Parch + 1`

**CabinLetter**

Extracts the first letter of the passenger's cabin information. Missing cabin values are assigned `Unknown`.

**IsAlone**

Identifies whether a passenger travelled alone.

- `1` – Travelling alone
- `0` – Travelling with family

### 4. Data Preprocessing

Numerical features:
- Missing values handled using median imputation.
- Numerical variables scaled using StandardScaler.

Categorical features:
- Missing values handled using most-frequent imputation.
- Categorical variables encoded using One-Hot Encoding.

A Scikit-learn ColumnTransformer and Pipeline are used to organize preprocessing and model training.

### 5. Model Training

Algorithm: Random Forest Classifier

Model configuration:
- Number of estimators: 300
- Maximum depth: 8
- Minimum samples split: 5
- Minimum samples leaf: 2
- Random state: 42

Dataset splitting:
- 80% Training Data
- 20% Testing Data

### 6. Model Evaluation

The model is evaluated using:

- Accuracy Score
- Classification Report
- Confusion Matrix
- 5-Fold Cross-Validation

### 7. Feature Importance Analysis

Feature importance is extracted from the trained Random Forest model.

A visualization is generated to identify the most influential features used by the classifier.

### 8. Project Report

A text report is automatically generated containing:

- Project objective
- Data preprocessing details
- Feature engineering techniques
- Model configuration
- Model accuracy
- Cross-validation results
- Top five important features
- Project conclusion

##  How to Run the Project

### Step 1: Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Titanic-Survival-Prediction-Feature-Engineering.git
```

### Step 2: Open the project directory

```bash
cd Titanic-Survival-Prediction-Feature-Engineering
```

### Step 3: Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib jupyter
```

### Step 4: Download the dataset

Download `train.csv` from the Kaggle Titanic competition and place it in the project directory.

### Step 5: Launch Jupyter Notebook

```bash
jupyter notebook
```

### Step 6: Run the notebook

Open `Titanic_Survival_Feature_Engineering.ipynb` and execute the cells sequentially from beginning to end.

##  Expected Outputs

After successful execution, the project generates:

- Cleaned Titanic dataset
- Trained Random Forest model
- Model accuracy and classification report
- Confusion matrix visualization
- Cross-validation results
- Feature importance ranking
- Feature importance visualization
- Automated project report

Actual accuracy and feature importance values depend on the dataset and model execution.

##  Key Learning Outcomes

- Understanding data preprocessing techniques.
- Applying Feature Engineering to real-world datasets.
- Handling missing numerical and categorical values.
- Implementing One-Hot Encoding and Standard Scaling.
- Building machine learning pipelines.
- Training and evaluating Random Forest models.
- Understanding feature importance.
- Generating machine learning project reports.

##  Conclusion

This project demonstrates how Feature Engineering and Machine Learning can be combined to predict passenger survival using the Titanic dataset.

By creating meaningful features, preprocessing data, and implementing a Random Forest Classifier, the project provides a structured approach to binary classification.

The project also demonstrates model evaluation and feature importance analysis to understand the predictive performance of the trained model.

##  Author

**Purva Ghate**

GitHub: https://github.com/YOUR-USERNAME

---

⭐ If you find this project useful, consider giving the repository a star!
