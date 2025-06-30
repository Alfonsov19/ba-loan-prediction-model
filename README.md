# SBA 504 Loan Approval Analysis

## Project Summary
This project investigates the patterns behind funded and unfunded SBA 504  loans, using a public dataset. It includes extensive EDA, feature engineering, and predictive modeling using Linear, Polynomial, and Ridge Regression.

Business Problem
This project uses SBA 504 loan data to identify patterns among businesses whose loans were approved but never funded. By training a predictive model exclusively on this group, we can estimate what these businesses should have received — unlocking opportunities for alternative lenders to serve overlooked clients.

**Primary Goal**
Predict the GrossApproval amount a business would likely receive based on key features — for businesses whose SBA loans were approved but not funded.

This enables lenders (like Doriscar Capital) to:

Identify pre-qualified but unfunded businesses

Estimate how much they would likely need

Proactively offer alternative financing options

## Key Results
- Final model (Polynomial Regression, degree=2) achieved:
  - R²: 0.98
  - Cross-validated R²: 0.966
- Engineered features: Business age category, loan density, approval per job, NAICS sector encoding
- Developed with: Pandas, Scikit-learn, NumPy, Matplotlib

- ##  Results Summary

| Model                     | R² Score | Cross-validated R² | RMSE       | MAE        |
|--------------------------|----------|--------------------|------------|------------|
| Linear Regression         | 0.165    | -                  | ~1.15M     | ~834K      |
| Polynomial Regression (deg=2) | **0.987** | **0.966**        | ~143K      | ~97K       |
| Ridge Regression          | 0.165    | -                  | ~1.15M     | ~834K      |

##  Key Features Engineered

- `BusinessAge_num`: Numerical conversion of business age
- `NaicsSector_encoded`: Encoded 2-digit NAICS industry sectors
- `CollateralInd_encoded`: Encoded indicator for presence of collateral
- `ApprovalPerJob`: Funding efficiency per job created
- `LoanDensity`: Loan amount relative to loan term
- `IsStartup`: Flag for businesses with less than 2 years in operation
- `JobsPerMonth`: Job creation normalized over loan duration

## Why It Matters
This project demonstrates my ability to:
- Understand and clean complex financial data
- Engineer predictive features from real-world business variables
- Communicate findings clearly and apply modeling to support loan and investment decisions

