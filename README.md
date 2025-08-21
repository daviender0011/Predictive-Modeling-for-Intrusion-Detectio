# Predictive-Modeling-for-Intrusion-Detection

This project aims to detect intrusions in a Software-Defined Networking (SDN) environment using various machine learning models. The project utilizes a dataset containing network traffic features to classify connections as either benign or malicious.

## Dataset

The dataset used in this project is `SDN_Intrusion.csv`, which contains network flow data with various features and a 'Class' column indicating whether the flow is benign or an intrusion.

## Project Steps

1.  **Data Loading and Preprocessing**: The data is loaded into a pandas DataFrame. Column names are cleaned, and missing values are handled by filling them with the median of the respective columns. The target variable 'Class' is encoded and remapped to two classes: 'BENIGN' and 'Malicious' to handle class imbalance.

2.  **Data Visualization**: Various plots are generated to understand the distribution of key features and their relationship with the target variable. This includes count plots for the class distribution, histograms for flow duration and packet length mean, and bar plots for the total forward and backward packets by class.

3.  **Feature Engineering**: The data is split into features (X) and the target variable (y). Infinite values in the feature set are replaced with the median of each column. The features are then scaled using `StandardScaler`.

4.  **Model Training**: Five different machine learning models are trained on the preprocessed data:
    *   Logistic Regression
    *   Decision Tree
    *   Random Forest
    *   XGBoost
    *   MLP Classifier

5.  **Model Evaluation**: Each trained model is evaluated using various metrics, including Accuracy, F1 Score, Precision, and Recall. Classification reports and Confusion Matrices are generated to provide a detailed view of the model's performance.

6.  **Model Comparison**: The performance metrics of all models are compiled into a table and visualized using a bar plot for easy comparison.

7.  **Prediction Example**: A sample of 20 random instances from the test set is selected to demonstrate the actual vs. predicted class values for one of the models (XGBoost in this case).

## Dependencies

The project requires the following libraries:

*   pandas
*   numpy
*   matplotlib
*   seaborn
*   scikit-learn
*   xgboost

You can install these dependencies using pip:
