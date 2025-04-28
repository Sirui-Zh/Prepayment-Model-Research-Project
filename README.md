# Prepayment-Model-Research-Project
# Understanding Mortgage Prepayment Timing and Its Drivers: A Comparative Machine Learning Approach

This repository contains the code and report for analyzing the timing of mortgage prepayment using machine learning models, comparing linear and nonlinear approaches.

## Project Overview
Traditional studies often focus on whether a mortgage loan is prepaid, but few investigate *when* prepayment occurs.  
This project models prepayment timing—measured as the number of months from origination to prepayment—as a continuous variable.

We apply three regression models to predict prepayment timing based on borrower, loan, and property characteristics:
- Linear Regression
- Random Forest Regression
- Multilayer Perceptron (MLP)

## Files Included
- `mortgage_prepayment_analysis.ipynb`: Code for data preprocessing, model training, evaluation, and visualization. *(Replace with your real notebook name if different!)*
- `Understanding_Mortgage_Prepayment_Timing_and_Its_Drivers.pdf`: Full project report including methods, model performance, and feature importance analysis.

## Dataset
- Source: Kaggle Loan Prepayment Dataset (public dataset)
- Records: U.S. residential mortgage loans originated in 1991, tracked monthly over 192 months.
- Key features: Borrower credit score, loan-to-value ratio (LTV), debt-to-income ratio (DTI), mortgage interest rate, property characteristics.

## Methods
- Preprocessing: Excluded full-term and very early prepayments, normalized features, and created the refinancing incentive variable `RateSpread`.
- Modeling:
  - Linear Regression: Baseline model to capture linear relationships.
  - Random Forest Regression: Captures nonlinear feature interactions.
  - MLP: Neural network model for capturing complex patterns.

## Results
- **Random Forest** achieved the best performance:
  - **MAE**: 3.01 months
  - **R²**: 0.953
- **Linear Regression** showed moderate performance but suffered from heteroscedasticity and non-normal residuals.
- **MLP** performed better than linear regression but worse than random forest.

### Key Findings
- Mortgage interest rate (RateSpread) is the dominant driver of prepayment timing.
- Original loan balance (OrigUPB) and borrower credit score also play important roles.
- Nonlinear models significantly outperform linear approaches in capturing prepayment behavior.

## Conclusion
This study reframes mortgage prepayment analysis by focusing on *timing* rather than occurrence, and demonstrates the effectiveness of machine learning models in predicting loan prepayment dynamics.

The findings provide practical tools for mortgage lenders, investors, and risk managers seeking to better forecast cash flows and manage portfolio risks.

## Future Work
- Incorporating time-varying macroeconomic variables.
- Fine-tuning MLP architectures.
- Exploring survival analysis frameworks for time-to-event modeling.
