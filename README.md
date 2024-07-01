# Credit-Card-Fraud-Detection

This repository contains code for detecting credit card fraud using a machine learning model. The dataset used is highly imbalanced, with a majority of the transactions being legitimate (class 0) and a small fraction being fraudulent (class 1). The key steps in the process include data preprocessing, balancing the dataset, splitting the data into training and testing sets, scaling the features, and evaluating the model's performance.

Steps Involved

1. Data Preprocessing:

- Grouping the data by the Class column and calculating the mean for each class.
- Sampling a subset of legitimate transactions to balance the dataset.
- Combining the sampled legitimate transactions with all the fraudulent transactions to create a new balanced dataset.

2. Splitting the Data:
- Dropping the Class column to create feature set X.
- Keeping the Class column as the target variable Y.
- Splitting the data into training and testing sets using an 80-20 split while ensuring the class distribution is maintained using stratification.

3. Feature Scaling:
- Scaling the features using StandardScaler to standardize the feature values.

4. Model Training and Evaluation:
- Training the model on the scaled training data.
- Predicting the labels for the training data and calculating the training accuracy.
- Predicting the labels for the test data and calculating the test accuracy.

5. Key Functions and Methods
- pd.concat(): Combines the sampled legitimate transactions and fraudulent transactions.
- train_test_split(): Splits the data into training and testing sets with stratification to maintain class distribution.
- StandardScaler(): Scales the features to have a mean of 0 and a standard deviation of 1.
- accuracy_score(): Calculates the accuracy of the model by comparing the predicted labels with the true labels.
