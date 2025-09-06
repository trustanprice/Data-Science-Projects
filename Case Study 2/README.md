# Case Study: Wine Alcohol Content Prediction

## Project Overview
This project focuses on building predictive models to estimate the alcohol content of wines using various chemical properties and measurements. Multiple modeling approaches were explored, including subset selection, Weighted Least Squares (WLS), Ridge, Lasso, and Principal Component Regression (PCR). The analysis addressed challenges such as heteroscedasticity, multicollinearity, and influential points to ensure valid model assumptions and robust predictions.

The study demonstrates the importance of diagnostic testing, model selection, and remedial measures in developing reliable regression models.

## Dataset
The dataset (`wines.csv`) contains chemical measurements and type classification for red and white wines. Key features include:

- Fixed acidity, volatile acidity, citric acid  
- Residual sugar, chlorides, sulphates  
- Free and total sulfur dioxide  
- Density, pH  
- Alcohol content (response variable)  
- Type (red or white)

## Methodology
1. **Exploratory Data Analysis**
   - Correlation matrix to assess variable relationships and multicollinearity  
   - Boxplots comparing alcohol by wine type  
   - Histograms and density plots for alcohol distribution  

2. **Model Development**
   - **Full Model**: Regression with all predictors  
   - **Subset Selection**: Stepwise regression (AIC, BIC, adjusted R², Mallows’ Cp)  
   - **Principal Component Regression (PCR)**: Dimensionality reduction and RMSE evaluation  
   - **Ridge and Lasso Regression**: Regularization to handle collinearity and improve generalization  
   - **Weighted Least Squares (WLS)**: Corrected for heteroscedasticity  

3. **Diagnostics and Validation**
   - Residual analysis and Q–Q plots  
   - Breusch-Pagan test for heteroscedasticity  
   - Kolmogorov-Smirnov test for normality of residuals  
   - Cook’s distance and leverage analysis for influential points  
   - ANOVA comparison of models  

## Key Findings
- The **full model** achieved an R² of 82%, showing strong predictive power.  
- **Subset selection** produced simpler models but left some heteroscedasticity unresolved.  
- **WLS** provided the best fit (Adjusted R² ≈ 99.98%), correcting for heteroscedasticity and improving explanatory power.  
- **Regularization (Ridge, Lasso)** and **PCR** showed competitive performance with lower RMSE values on test data, confirming generalizability.  
- High-leverage points were identified and addressed to improve model stability.  

## Results
- WLS explained nearly all variance in alcohol content while passing key diagnostic tests.  
- Lasso regression achieved low RMSE (~0.38) on the test set, balancing sparsity and predictive accuracy.  
- PCR indicated that ~3 principal components captured most variance in predictors, though with diminishing returns beyond that.  

## Tools and Technologies
- **Language**: R  
- **Libraries**: `stats`, `leaps`, `car`, `MASS`, `pls`, `lars`  
- **Techniques**: Regression modeling, model selection, Ridge/Lasso regularization, PCR, ANOVA, WLS  

## How to Run
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/data-science-projects.git
   cd data-science-projects/wine-alcohol-prediction
2. Open the R scripts or R Markdown file.
3. Run the analysis to reproduce data cleaning, model fitting, and diagnostics.

## Author

Trustan Gabriel Price

University of Illinois Urbana-Champaign

B.S. in Statistics, Minors in Computer Science and Data Science
