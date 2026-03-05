# Titanic Survival Prediction

This notebook demonstrates a machine learning workflow to predict passenger survival on the Titanic using the Logistic Regression algorithm.

## Data Preprocessing

1.  **Loading Data**: The `train_titanic.csv` dataset was loaded into a Pandas DataFrame.
2.  **Initial Inspection**: The shape and info of the dataset were checked to understand the number of rows, columns, and data types.
3.  **Handling Missing Values**:
    *   The 'Cabin' column, which had a high number of missing values (687 out of 891), was dropped.
    *   Missing values in the 'Age' column were imputed with the mean age.
    *   Missing values in the 'Embarked' column were imputed with the mode (most frequent value).
4.  **Encoding Categorical Features**: The 'Sex' column ('male', 'female') and 'Embarked' column ('S', 'C', 'Q') were converted into numerical representations (0, 1, 2) using one-hot encoding.

## Exploratory Data Analysis (EDA)

Basic EDA was performed to understand the distribution of key features and their relationship with survival:

*   **Survival Count**: Visualized the number of survivors vs. non-survivors.
*   **Sex Distribution**: Analyzed the distribution of male and female passengers.
*   **Survival by Sex**: Explored the survival rates based on gender, showing that females had a higher survival rate.
*   **Survival by Pclass**: Investigated survival rates across different passenger classes, indicating that passengers in higher classes had better survival chances.

## Model Training

1.  **Feature Selection**: Features such as 'PassengerId', 'Name', and 'Ticket' were dropped as they were not considered relevant for the prediction model. The 'Survived' column was set as the target variable (Y), and the remaining columns formed the feature set (X).
2.  **Data Splitting**: The dataset was split into training (80%) and testing (20%) sets to evaluate model performance on unseen data.
3.  **Model Selection**: A Logistic Regression model was chosen for this binary classification task.
4.  **Model Training**: The Logistic Regression model was trained using the training data (`X_train`, `Y_train`).
5.  **Evaluation**: 
    *   Training data accuracy: 80.76%
    *   Test data accuracy: 78.21%

## Prediction

The trained model can predict survival for new input data. An example prediction was made with a sample input, demonstrating how to prepare input data and interpret the model's output.
"""

with open('README.md', 'w') as f:
    f.write(readme_content)

print('README.md has been generated.')
