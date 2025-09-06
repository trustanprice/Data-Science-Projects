# Case Study: Halloween Candy Popularity Analysis

## Project Overview
This project analyzes the key qualities that make Halloween candies desirable based on their attributes. Using a dataset of candies with characteristics such as chocolate, fruity flavor, caramel, peanuts, nougat, and other ingredients, we apply multiple linear regression to explain candy desirability as measured by the percentage of votes each candy receives (`winpercent`).

The project explores:
- Exploratory data analysis and visualization of candy attributes
- Correlation analysis to identify relationships among predictors
- Multiple linear regression model development
- Model reduction and validation
- Interpretation of results and implications

## Dataset
The dataset (`candy-data.csv`) contains candy attributes and popularity measures. Each row represents a candy with the following features:
- Ingredient indicators (chocolate, fruity, caramel, peanutyalmondy, nougat, crispedricewafer, hard, bar, pluribus)
- Percent sugar and price values (`sugarpercent`, `pricepercent`)
- Response variable: `winpercent` (percentage of popularity votes)

## Methodology
1. **Exploratory Data Analysis**
   - Summary statistics and boxplots of `winpercent`
   - Attribute frequency visualization with stacked bar plots
   - Correlation matrix for predictor relationships

2. **Regression Modeling**
   - Full multiple linear regression model including all predictors
   - Reduced model selection focusing on significant predictors
   - Multicollinearity checks using Variance Inflation Factor (VIF)

3. **Model Evaluation**
   - Residual analysis and diagnostic plots
   - Prediction of selected candies (Reese’s Peanut Butter Cup, Snickers, Almond Joy, Candy Corn)
   - Comparison of predicted versus actual desirability

## Key Findings
- Chocolate, fruity flavors, and peanuts/almonds were statistically significant predictors of candy desirability.
- The reduced model simplified interpretation while retaining strong explanatory power.
- Predictions highlighted underestimation for certain popular candies (e.g., Reese’s Peanut Butter Cup).
- Multicollinearity was not a concern, with all VIF values below 5.

## Results
Example predictions compared to actual values:

| Candy                     | Predicted Win% | Actual Win% | Residual |
|----------------------------|----------------|-------------|----------|
| Almond Joy                 | 66.84          | 50.35       | 16.49    |
| Candy Corn                 | 35.79          | 38.01       | 2.22     |
| Reese’s Peanut Butter Cup  | 66.84          | 84.18       | 17.34    |
| Snickers                   | 66.84          | 76.67       | 9.84     |

## Tools and Technologies
- **Language**: R
- **Libraries**: `ggplot2`, `stats`, `car`
- **Techniques**: Exploratory data analysis, multiple linear regression, model selection, diagnostics

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/stat425-case-study1.git
   cd stat425-case-study1

## Author

Trustan Gabriel Price
University of Illinois Urbana-Champaign
Course: STAT 425 – Case Studies in Statistical Analysis
