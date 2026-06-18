# Gender Classification Using Machine Learning

## Project Overview

This project aims to develop a machine learning model capable of classifying an individual's gender based on three physical attributes:
- **Height (cm)**
- **Weight (kg)**
- **Age (years)**

The project follows a complete machine learning workflow, including data preprocessing, exploratory data analysis (EDA), feature engineering, model training, evaluation, and prediction.

## Models Evaluated

Several classification algorithms are tested to identify the most effective model for this problem:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- K-Nearest Neighbors (KNN)

## Libraries Used

- `pandas` for data manipulation
- `matplotlib` and `seaborn` for data visualization
- `scikit-learn` for machine learning model development and evaluation

## Workflow

1. **Load Data**: The dataset `Gender_Classification_Data.csv` is loaded and inspected.
2. **Exploratory Data Analysis (EDA)**: Understanding dataset dimensions, statistical summaries, and checking for missing values.
3. **Data Preprocessing**: Preparing the data for machine learning models (e.g., encoding categorical variables, scaling features).
4. **Model Training**: Training the four aforementioned classification algorithms.
5. **Model Evaluation**: Comparing models based on accuracy and classification reports to determine the best performing algorithm.

## How to Run

Open the `Gender_Classification.ipynb` Jupyter Notebook and run the cells sequentially. Make sure you have the required libraries installed and the dataset `Gender_Classification_Data.csv` in the appropriate directory as referenced in the notebook.

## Credits

Dataset provided by [Sameh Raouf on Kaggle](https://www.kaggle.com/datasets/samehraouf/gender-classification-dataset).