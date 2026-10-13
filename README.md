
# Student Performance Prediction Using Machine Learning

## Overview

This project focuses on predicting students' mathematics scores based on demographic information, reading scores, writing scores, and other educational factors using Machine Learning.

The project follows a modular Machine Learning pipeline that includes data ingestion, data transformation, model training, and prediction pipeline development.

## Tech Stack

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning:** Scikit-learn, CatBoost
- **Data Preprocessing:** SimpleImputer, StandardScaler, OneHotEncoder
- **Pipeline Management:** Pipeline, ColumnTransformer
- **Model Serialization:** Pickle, Dill
- **Version Control:** Git, GitHub

## Dataset

The project uses a student performance dataset containing the following features:

- Gender
- Race/Ethnicity
- Parental Level of Education
- Lunch Type
- Test Preparation Course
- Reading Score
- Writing Score

**Target Variable:** `math_score`

The objective is to predict students' mathematics scores using the available input features.

## Project Structure

```text
ML-Project1/
├── artifacts/
│   ├── data.csv
│   ├── train.csv
│   ├── test.csv
│   ├── model.pkl
│   └── proprocessor.pkl
├── catboost_info/
├── logs/
├── notebook/
│   └── data/
│       └── stud.csv
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   ├── pipeline/
│   │   ├── predict_pipeline.py
│   │   └── train_pipeline.py
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
├── .gitignore
└── README.md
```

## Project Workflow

### 1. Data Ingestion

- Loads the original dataset using Pandas.
- Saves a copy of the raw dataset.
- Splits the dataset into training and testing sets using an 80:20 ratio.
- Stores the generated datasets in the `artifacts` directory.

### 2. Data Transformation

- Handles missing numerical values using median imputation.
- Handles missing categorical values using most-frequent imputation.
- Applies StandardScaler to numerical features.
- Converts categorical features into numerical representations using OneHotEncoder.
- Uses ColumnTransformer and Pipeline to organize preprocessing steps.
- Saves the fitted preprocessing object for reuse during prediction.

### 3. Model Training

- Uses the transformed training data to train Machine Learning models.
- Evaluates model performance using the implemented model evaluation process.
- Saves the trained model as `model.pkl`.

### 4. Prediction Pipeline

- Loads the saved model and preprocessing object.
- Prepares input data using the same preprocessing steps used during training.
- Generates predictions for new student records.

## Installation and Setup

### Prerequisites

- Python 3.10 or a compatible Python version
- Git
- pip

### Step 1: Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd ML-Project1
```

Replace `<YOUR_GITHUB_REPOSITORY_URL>` with your actual GitHub repository URL.

### Step 2: Create a Virtual Environment

```bash
python -m venv venv
```

### Step 3: Activate the Virtual Environment

For Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

### Step 4: Install Dependencies

If the repository contains a `requirements.txt` file, run:

```bash
pip install -r requirements.txt
```

### Step 5: Run the ML Pipeline

From the project root directory, execute:

```bash
python src/components/data_ingestion.py
```

The script runs data ingestion, data transformation, and model training in sequence, according to the current implementation.

## Generated Artifacts

| File | Description |
|---|---|
| `data.csv` | Copy of the original dataset |
| `train.csv` | Training dataset |
| `test.csv` | Testing dataset |
| `proprocessor.pkl` | Serialized preprocessing pipeline |
| `model.pkl` | Serialized trained model |

## Key Learning Outcomes

- Understanding an end-to-end Machine Learning workflow.
- Implementing modular Python code for ML projects.
- Performing data cleaning and preprocessing.
- Handling numerical and categorical features.
- Building reusable Scikit-learn pipelines.
- Separating training and testing datasets.
- Saving and loading trained models and preprocessing objects.
- Managing project versions using Git and GitHub.

## Future Improvements

- Compare multiple Machine Learning algorithms.
- Add detailed evaluation metrics and visualizations.
- Improve automated testing and error handling.
- Develop a user interface for predictions.
- Deploy the model as a web application or API.

## Disclaimer

This project is developed for educational purposes to explore Machine Learning concepts and workflows. Predictions should not be used as the sole basis for consequential decisions about students.

# Student Performance Prediction Using Machine Learning

## Overview

This project focuses on predicting students' mathematics scores based on demographic information, reading scores, writing scores, and other educational factors using Machine Learning.

The project follows a modular Machine Learning pipeline that includes data ingestion, data transformation, model training, and prediction pipeline development.

## Tech Stack

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning:** Scikit-learn, CatBoost
- **Data Preprocessing:** SimpleImputer, StandardScaler, OneHotEncoder
- **Pipeline Management:** Pipeline, ColumnTransformer
- **Model Serialization:** Pickle, Dill
- **Version Control:** Git, GitHub

## Dataset

The project uses a student performance dataset containing the following features:

- Gender
- Race/Ethnicity
- Parental Level of Education
- Lunch Type
- Test Preparation Course
- Reading Score
- Writing Score

**Target Variable:** `math_score`

The objective is to predict students' mathematics scores using the available input features.

## Project Structure

```text
ML-Project1/
├── artifacts/
│   ├── data.csv
│   ├── train.csv
│   ├── test.csv
│   ├── model.pkl
│   └── proprocessor.pkl
├── catboost_info/
├── logs/
├── notebook/
│   └── data/
│       └── stud.csv
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   ├── pipeline/
│   │   ├── predict_pipeline.py
│   │   └── train_pipeline.py
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
├── .gitignore
└── README.md
```

## Project Workflow

### 1. Data Ingestion

- Loads the original dataset using Pandas.
- Saves a copy of the raw dataset.
- Splits the dataset into training and testing sets using an 80:20 ratio.
- Stores the generated datasets in the `artifacts` directory.

### 2. Data Transformation

- Handles missing numerical values using median imputation.
- Handles missing categorical values using most-frequent imputation.
- Applies StandardScaler to numerical features.
- Converts categorical features into numerical representations using OneHotEncoder.
- Uses ColumnTransformer and Pipeline to organize preprocessing steps.
- Saves the fitted preprocessing object for reuse during prediction.

### 3. Model Training

- Uses the transformed training data to train Machine Learning models.
- Evaluates model performance using the implemented model evaluation process.
- Saves the trained model as `model.pkl`.

### 4. Prediction Pipeline

- Loads the saved model and preprocessing object.
- Prepares input data using the same preprocessing steps used during training.
- Generates predictions for new student records.

## Installation and Setup

### Prerequisites

- Python 3.10 or a compatible Python version
- Git
- pip

### Step 1: Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd ML-Project1
```

Replace `<YOUR_GITHUB_REPOSITORY_URL>` with your actual GitHub repository URL.

### Step 2: Create a Virtual Environment

```bash
python -m venv venv
```

### Step 3: Activate the Virtual Environment

For Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

### Step 4: Install Dependencies

If the repository contains a `requirements.txt` file, run:

```bash
pip install -r requirements.txt
```

### Step 5: Run the ML Pipeline

From the project root directory, execute:

```bash
python src/components/data_ingestion.py
```

The script runs data ingestion, data transformation, and model training in sequence, according to the current implementation.

## Generated Artifacts

| File | Description |
|---|---|
| `data.csv` | Copy of the original dataset |
| `train.csv` | Training dataset |
| `test.csv` | Testing dataset |
| `proprocessor.pkl` | Serialized preprocessing pipeline |
| `model.pkl` | Serialized trained model |

## Key Learning Outcomes

- Understanding an end-to-end Machine Learning workflow.
- Implementing modular Python code for ML projects.
- Performing data cleaning and preprocessing.
- Handling numerical and categorical features.
- Building reusable Scikit-learn pipelines.
- Separating training and testing datasets.
- Saving and loading trained models and preprocessing objects.
- Managing project versions using Git and GitHub.

## Future Improvements

- Compare multiple Machine Learning algorithms.
- Add detailed evaluation metrics and visualizations.
- Improve automated testing and error handling.
- Develop a user interface for predictions.
- Deploy the model as a web application or API.

## Disclaimer

This project is developed for educational purposes to explore Machine Learning concepts and workflows. Predictions should not be used as the sole basis for consequential decisions about students.

