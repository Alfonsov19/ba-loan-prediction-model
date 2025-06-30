# SBA 504 Loan Approval Analysis

## Project Summary
This project investigates the patterns behind funded and unfunded SBA 504  loans, using a public dataset. It includes extensive EDA, feature engineering, and predictive modeling using Linear, Polynomial, and Ridge Regression.

 Business Problem
**How can we predict the gross amount approved for a commercial real estate loan based on business characteristics, job creation, and collateral?**

Financial institutions often struggle to proactively assess approval trends, gauge funding risks, and identify businesses likely to require alternative or follow-up financing. This project aims to support smarter lending strategies and partnership targeting (e.g., brokers, CRE agents).

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

