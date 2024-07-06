# Neural Network Challenge 2

## Background
This project aims to create a neural network to assist the HR department in predicting employee attrition and optimal department placement. HR needs a tool to determine if employees are likely to leave the company and to identify which department suits each employee best. To achieve this, we will develop a neural network with a branched architecture to handle these dual predictions simultaneously.

## Implementation Steps
The implementation process is divided into three main parts: preprocessing, model creation and training, and summarizing the results.

## Preprocessing
Begin by importing the dataset and viewing its first five rows to get an initial understanding. Assess the uniqueness of values in each column to help identify potential features and targets. Construct a DataFrame y_df containing the attrition and department columns, which are the target variables. Select at least ten other columns to use as features for your X_df, excluding the attrition and department columns. Inspect the data types of X_df to ensure they are appropriate for model training. Split the data into training and testing sets, then convert the features in X_df to numeric data types as needed. This may involve fitting encoders to the training data and subsequently transforming both the training and testing data. Apply a StandardScaler to standardize the features, fitting it to the training data first. For the target columns, use OneHotEncoder to encode the department and attrition columns, fitting the encoders to the training data and transforming both training and testing sets accordingly.

## Model Creation, Compilation, and Training
To build the neural network, first determine the number of input features from the training data. The model should not be sequential since it requires branched output layers. Instead, start by creating the input layer followed by at least two shared hidden layers. For the branch predicting the department, add one hidden layer and an output layer. Similarly, create a branch for predicting attrition with its own hidden and output layers. Compile the model to prepare it for training, and provide a summary to verify its structure. Train the model using the preprocessed data and then evaluate its performance on the testing data. The evaluation should include the accuracy for both department and attrition predictions.

## Summary and Analysis
After training and evaluating the model, reflect on the results by answering a few critical questions. Consider whether accuracy is the best metric for this data and explain your reasoning. Discuss the activation functions chosen for the output layers and justify your choices. Finally, suggest potential improvements for the model, considering aspects like architecture adjustments, additional data preprocessing, or alternative evaluation metrics.
