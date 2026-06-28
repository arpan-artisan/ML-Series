# Understanding Linear Regression: From Equation to Prediction

This project is the practical coding companion for a beginner-friendly Medium article on **Simple Linear Regression**.

The goal is to predict one numerical value using one input feature. In this example, we use a salary prediction dataset where the usual idea is to predict salary from years of experience. The notebook does not jump straight into training. It first shows how to inspect and understand the dataset before building a model.

This project stays focused only on **Simple Linear Regression**. It does not cover Multiple Linear Regression.

## Dataset

Dataset source:

[Salary Dataset - Simple Linear Regression on Kaggle](https://www.kaggle.com/datasets/abhishek14398/salary-dataset-simple-linear-regression)

Because Kaggle downloads often require authentication, the dataset is not included in this repository.

Download the CSV manually from Kaggle and place it here:

```text
linear-regression-practical/data/Salary_dataset.csv
```

The notebook is written to inspect the actual column names after loading the CSV. It does not assume column names before checking the dataset.

## Project Structure

```text
linear-regression-practical/
|
├── data/
│   └── Salary_dataset.csv
|
├── notebooks/
│   └── linear_regression_salary_prediction.ipynb
|
├── models/
│   └── linear_regression_model.pkl
|
├── requirements.txt
├── README.md
└── .gitignore
```

Note: `models/linear_regression_model.pkl` is created when you run the notebook. The `.gitignore` file excludes `.pkl` files because trained model files are generated outputs.

## Workflow

The notebook follows a simple Machine Learning workflow:

1. Load the dataset.
2. Inspect rows, shape, columns, data types, and summary statistics.
3. Understand which column should be the input feature and which should be the target.
4. Check and handle missing values.
5. Check and remove duplicate rows if needed.
6. Visualize the relationship between the feature and target.
7. Split the data into training and testing sets.
8. Train a Simple Linear Regression model.
9. Make predictions.
10. Evaluate the model.
11. Visualize the regression line, actual vs predicted values, and residuals.
12. Save and load the trained model.

## Setup

Open a terminal inside the `linear-regression-practical` folder.

### Windows PowerShell

```powershell
python -m venv venv
venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

### macOS/Linux

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Windows Long Path Note

If `pip install -r requirements.txt` fails on Windows with a long-path error while installing Jupyter, move the project closer to the drive root, for example `C:\ML-Series\linear-regression-practical`, or enable Windows Long Path support.

## How to Run the Notebook

After installing the dependencies and placing the Kaggle CSV at `data/Salary_dataset.csv`, start Jupyter from inside the `linear-regression-practical` folder:

```bash
jupyter notebook
```

Then open:

```text
notebooks/linear_regression_salary_prediction.ipynb
```

The notebook loads the dataset from this exact path:

```text
data/Salary_dataset.csv
```

## Libraries Used

- pandas
- numpy
- matplotlib
- scikit-learn
- jupyter
- joblib

## What the Notebook Covers

- Why we study the dataset before training a model
- Loading a real CSV dataset
- Inspecting rows, shape, column names, data types, and descriptive statistics
- Checking missing values and duplicate rows
- Selecting one input feature and one target variable
- Creating clean visualizations with matplotlib
- Training a Simple Linear Regression model with scikit-learn
- Understanding coefficient and intercept
- Making predictions
- Evaluating predictions with MAE, MSE, RMSE, and R2 Score
- Visualizing the regression line
- Comparing actual and predicted values
- Understanding residuals
- Saving and loading the trained model with joblib

## Saved Model File

When the notebook reaches the model-saving step, it writes the trained model to:

```text
models/linear_regression_model.pkl
```

Saving the model is useful because it lets you reuse the trained model later without retraining it from scratch. This is an early step toward understanding how trained models are used in real applications.

## Learning Goal

This project is designed for beginners learning Simple Linear Regression. The main lesson is not just how to call `model.fit()`, but how to approach a dataset carefully before training a Machine Learning model.
