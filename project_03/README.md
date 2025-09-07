# Salary Trends and Employment Patterns in Data Science Professions

## Project Overview
This project analyzes global salary and employment trends in data science–related roles using regression modeling. We apply **linear regression** to predict salary growth across expertise levels and **logistic regression** to estimate the likelihood that an employee resides in the United States. The analysis helps uncover key drivers of salary growth and employment location patterns for professionals in the data science field.

## Dataset
- **Source**: Data Science Salaries Dataset (2020–2024)  
- **Size**: 5,736 rows × 11 columns  
- **Key Features**:  
  - Job Title, Employment Type, Experience Level, Expertise Level  
  - Salary, Salary Currency, Salary in USD  
  - Company Location, Employee Residence  
  - Company Size, Year  

- **Response Variables**:  
  - *Linear Regression*: `Salary_in_USD` (continuous)  
  - *Logistic Regression*: `USA_Residence` (binary: 1 = U.S., 0 = non-U.S.)  

## Research Questions
1. **Linear Regression**:  
   How do expertise levels, company size, and other factors influence salary trends, and how can we predict future salaries across different expertise levels?  

2. **Logistic Regression**:  
   What are the key factors influencing the likelihood of an employee’s residence being in the United States, and how accurately can we predict residence?  

## Methodology
### Linear Regression
- Categorical encoding and forward selection for predictor choice.  
- Model refinement by removing non-significant predictors and multicollinearity.  
- Interpretation of coefficients and 95% confidence intervals.  
- Diagnostic checks with residual plots and Q-Q plots.  

### Logistic Regression
- Label encoding and creation of binary outcome (`USA_Residence`).  
- Full and reduced models tested.  
- Evaluation with confusion matrix, accuracy, sensitivity/specificity, ROC curve, and AUC.  

## Results
### Linear Regression
- **Key predictors**: Expertise Level, Employee Residence, Year.  
- Salary is predicted to increase **~$9,387 per year** on average.  
- 95% CI: $6,488 to $12,301.  
- Adjusted R² = 0.205 → model explains 20.5% of salary variability.  
- RMSE ≈ $70,753 → relatively high error for salary prediction.  

### Logistic Regression
- **Significant predictors**: Salary in USD, Company Location.  
- Reduced model achieved:  
  - **Accuracy**: 91%  
  - **AUC**: 0.92  
  - **Sensitivity**: 0.999  
  - **Specificity**: 0.578  
- Conclusion: Salary and location strongly predict U.S. residence for data science roles.  

## Key Insights
- Salary increases are more strongly linked to **expertise level** and **U.S. residence** than company size or employment type.  
- U.S.-based professionals consistently earn more than non-U.S. professionals.  
- Logistic regression is highly effective in predicting U.S. residency, suggesting clear geographic salary and employment patterns.  
- Linear regression shows moderate predictive power, highlighting the complexity and variability of salary trends.  

## Tools and Technologies
- **Languages**: Python  
- **Libraries**: Pandas, NumPy, Seaborn, Matplotlib, Scikit-learn, Statsmodels, SciPy  
- **Techniques**: Linear regression, logistic regression, forward selection, residual diagnostics, ROC/AUC evaluation  

## How to Run
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/data-science-projects.git
   cd data-science-projects/salary-trends
  2. Install dependencies:
     ```bash
     pip install pandas numpy matplotlib seaborn scikit-learn statsmodels scipy
     ```
  3. Open the Jupyter Notebook/HTML file and run all cells to reproduce results.

## Authors and Contributions

Quinn Crockling (qdc2) – Completed Parts 3 & 4 analysis.

**Trustan Gabriel Price**– Completed Parts 1–3, coding, statistical analysis, and final project submission.

University of Illinois Urbana-Champaign
