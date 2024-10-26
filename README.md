
# Titanic Survival Prediction Project

This project uses the Titanic dataset to predict passenger survival based on various features. Following the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** methodology, this project emphasizes a structured, iterative approach from understanding the business problem to data preparation, modeling, evaluation, and deployment.

## Project Outline

### 1. **Business Understanding**
   - **Goal**: Predict which passengers survived the Titanic disaster based on passenger details.
   - **Objective**: Use machine learning (specifically logistic regression and ensemble methods) to achieve high accuracy in predicting survival.
   - **Evaluation Metric**: Primary metric is **accuracy**, supplemented with confusion matrix, precision, recall, and ROC-AUC for a comprehensive evaluation.

### 2. **Data Understanding**
   - **Dataset**: The project uses Kaggle's Titanic dataset (`train.csv` for training and `test.csv` for submission).
   - **Feature Analysis**: Key features like `Pclass`, `Sex`, `Age`, `Fare`, etc., were explored to understand correlations with survival.

### 3. **Data Preparation**
   - **Handling Missing Values**: Imputed missing values in `Age`, `Cabin`, and `Embarked` based on data patterns.
   - **Feature Engineering**: Created new features such as `FamilySize` (from `SibSp` and `Parch`), `IsAlone`, and extracted titles from `Name`.
   - **Encoding and Scaling**: Applied one-hot encoding for categorical variables and scaled continuous variables for model optimization.

### 4. **Modeling**
   - **Initial Model**: Built a logistic regression model to establish a baseline accuracy.
   - **Feature Selection**: Used **Recursive Feature Elimination (RFE)**, **SelectKBest**, and **Optuna** to select top features.
   - **Advanced Model**: Implemented a Random Forest model, followed by hyperparameter tuning, to improve performance on the test set.

### 5. **Evaluation**
   - **Metrics**: Evaluated the model using accuracy, confusion matrix, precision, recall, F1 score, and ROC-AUC.
   - **Champion Solution Analysis**: Compared the approach with top-ranking Kaggle solutions, identifying potential improvements through advanced feature engineering and additional ensemble methods.

### 6. **Deployment (Submission)**
   - **Submission File**: Created a CSV file with `PassengerId` and `Survived` columns, as required by Kaggle.
   - **Submission Process**: Provided instructions for submitting the predictions on Kaggle and tracking performance on the leaderboard.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/titanic-survival-prediction.git
   cd titanic-survival-prediction
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Train the Model**: Run the `train_model.py` file to train and evaluate the model on the Titanic dataset.
2. **Feature Selection**: Adjust the parameters in `feature_selection.py` to experiment with different feature selection techniques.
3. **Predict and Submit**: Use `submit.py` to generate predictions for the test set and prepare the final submission file.

## Project Structure

- `data/` - Folder containing the Titanic dataset (`train.csv` and `test.csv`).
- `notebooks/` - Jupyter notebooks for data exploration and feature engineering.
- `src/` - Source code for data processing, model training, and evaluation.
- `output/` - Directory for saving submission files and model artifacts.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue for major changes.

## License

This project is licensed under the MIT License. See `LICENSE` for details.
