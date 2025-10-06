# Ttelco Customer Churn Prediction

This project aims to predict customer churn for a telecommunications company using a deep learning model.

## Project Steps

1.  **Data Loading and Initial Exploration:**
    - The dataset `WA_Fn-UseC_-Telco-Customer-Churn.csv` is loaded into a pandas DataFrame.
    - Initial inspection of the data using `df.head()` and `df.info()` is performed to understand the structure, data types, and presence of missing values.

2.  **Data Preprocessing:**
    - The `customerID` column is dropped as it is not relevant for model training.
    - Categorical columns are identified and their value counts are inspected.
    - Label Encoding is applied to all categorical columns to convert them into numerical representations.

3.  **Feature Scaling:**
    - The numerical columns `MonthlyCharges`, `TotalCharges`, and `tenure` are scaled using `MinMaxScaler` to normalize their values between 0 and 1.
    - 
4.  **Model Training:**
    - The data is split into training and testing sets using `train_test_split`.
    - A sequential Keras model is built with three dense layers and sigmoid activation functions.
    - The model is compiled with the Adam optimizer and binary cross-entropy loss.
    - The model is trained on the training data with a batch size of 50 and 100 epochs, using a 20% validation split.

5.  **Model Evaluation:**
    - Predictions are made on the test set using the trained model.
    - The accuracy of the model is calculated using `accuracy_score`.
    - The training and validation loss and accuracy are plotted to visualize the model's performance during training.

## Code Details

- Libraries used: `pandas`, `numpy`, `matplotlib.pyplot`, `seaborn`, `sklearn`, `tensorflow`, `keras`.
- Data is loaded from `/content/drive/MyDrive/datasets/WA_Fn-UseC_-Telco-Customer-Churn.csv`.
- LabelEncoder is used for categorical feature encoding.
- MinMaxScaler is used for numerical feature scaling.
- A simple sequential neural network is built with Keras.
- The model is trained for 100 epochs with a batch size of 50.
- Accuracy is used as the evaluation metric.
- Loss and accuracy plots are generated to visualize training progress.
