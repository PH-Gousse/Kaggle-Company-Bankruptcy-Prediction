# Company Bankruptcy Prediction


## Non-technical explanation

This project aims to predict whether companies will go bankrupt based on financial data from the Taiwan Economic Journal, covering the years 1999-2009. Using various machine learning models, we analyse financial indicators to help identify potential bankruptcy risks, which can be crucial for investors, policymakers, and financial institutions.

## Data

The dataset comprises financial records of companies from the Taiwan Economic Journal for the years 1999-2009. It includes various financial ratios and metrics that serve as features to predict the likelihood of bankruptcy. The target variable is a binary indicator of bankruptcy status. The data was preprocessed to handle missing values, remove highly correlated features, and balance the class distribution using Synthetic Minority Over-sampling Technique (SMOTE).

## Model 

We evaluated three machine learning models: Logistic Regression, Decision Tree, and Neural Network. Each model was trained to identify patterns in the financial data that could indicate a company’s risk of bankruptcy. We chose these models to compare their performance in terms of accuracy, precision, recall, and F1-score.

## Hyperparameter Optimisation

For each model, we optimised hyperparameters to enhance performance.

- Logistic Regression: We used Grid Search to find the best combination of regularisation strength, penalty type, solver, and tolerance.
- Decision Tree: Randomised Search was employed to optimise criteria, maximum depth, minimum samples split, minimum samples leaf, maximum features, and maximum leaf nodes.
- Neural Network: Randomised Search was used to tune the hidden layer sises, activation functions, learning rates, maximum iterations, alpha (regularisation term), and solver.


## Results

After training and evaluating the models, the Neural Network with tuned hyperparameters emerged as the best performer based on precision and F1-score. It achieved a balanced performance in correctly predicting both bankrupt and non-bankrupt companies. Here are the detailed results:

- Logistic Regression:
  - Precision: 0.87
  - F1 Score: 0.88
  - ROC AUC: 0.99
- Decision Tree:
  - Precision: 0.91
  - F1 Score: 0.93
- Neural Network:
  - Precision: 0.96
  - F1 Score: 0.97
  - ROC AUC: 0.99

The results indicate that the **Neural Network model**, with its ability to capture complex patterns in the data, provides the most reliable predictions for bankruptcy risk.
