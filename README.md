# Data Science and Machine Learning Portfolio

## Overview
This repository contains a collection of data science and machine learning projects I have completed across coursework, research, and personal study. Each project includes a detailed README, code, and analysis. Together, these projects demonstrate my abilities in **statistical modeling, data preprocessing, machine learning, exploratory data analysis, and interpretation of results for real-world insights**.

---

## Projects

### [Halloween Candy Popularity Analysis](./Case%20Study%201)
Explores the factors that make Halloween candy desirable.  

- **Skills Utilized**: Multiple Linear Regression, Model Reduction, Correlation Analysis, Exploratory Data Analysis (EDA)  
- **Tools**: R (`ggplot2`, `car`)  
- **Key Takeaway**: Chocolate and nut-based candies were significantly more desirable than fruity or sugar-only candies.  
- **Skills Learned**: Interpreting regression outputs, diagnosing model assumptions, and applying statistical methods to categorical predictors.  

---

### [Wine Alcohol Content Prediction](./Case%20Study%202)
Predicts alcohol content of wines from chemical attributes.  

- **Skills Utilized**: Subset Selection, Weighted Least Squares (WLS), Ridge Regression, Lasso Regression, Principal Component Regression (PCR), Model Diagnostics  
- **Tools**: R (`leaps`, `MASS`, `pls`)  
- **Key Takeaway**: Weighted Least Squares corrected heteroscedasticity and achieved the strongest model fit.  
- **Skills Learned**: Handling heteroscedasticity, comparing regularization techniques, and reducing dimensionality with PCR.  

---

### [Diagnosing Diabetes with Machine Learning](./FinalProject)
Predicts diabetes/prediabetes using BRFSS 2015 dataset.  

- **Skills Utilized**: Logistic Regression, Decision Trees, K-Nearest Neighbors (KNN), Neural Networks, PCA, Threshold Tuning, Model Evaluation (Recall, Precision, F1-Score, AUC)  
- **Tools**: Python (`scikit-learn`, `pandas`, `matplotlib`, `seaborn`)  
- **Key Takeaway**: KNN achieved ~91% accuracy and 88% recall, outperforming all other models.  
- **Skills Learned**: Balancing accuracy and recall in imbalanced datasets, implementing multiple ML models, and evaluating models with medical relevance.  
- **Grade**: 95%  

---

### [Spotify Song Popularity Analysis](./project_01)
Investigates whether tempo and explicit content predict song popularity.  

- **Skills Utilized**: Correlation Analysis, Simple Linear Regression, Data Cleaning, Visualization  
- **Tools**: Python (`pandas`, `numpy`, `seaborn`, `matplotlib`)  
- **Key Takeaway**: Neither tempo nor explicit content were strong predictors — popularity is influenced by cultural and external factors.  
- **Skills Learned**: Testing weak predictors, interpreting regression coefficients, and identifying limitations of simple models.  

---

### [Data Science Salary Differences](./project_02)
Compares salaries between **pure data science roles** and **business-oriented roles**, and across **Europe vs. North America** post-pandemic.  

- **Skills Utilized**: Hypothesis Testing, Bootstrap Confidence Intervals, Simulation Methods, Data Sampling, EDA  
- **Tools**: Python (`scipy`, `numpy`, `matplotlib`, `seaborn`)  
- **Key Takeaway**: Pure data science roles earn \$25K–\$57K more than business roles. No statistically significant salary difference was found between Europe and North America.  
- **Skills Learned**: Building confidence intervals, running simulation-based hypothesis tests, and interpreting regional salary trends.  

---

### [Global Salary Trends in Data Science](./project_03)
Analyzes global data science salary growth and employment patterns.  

- **Skills Utilized**: Linear Regression, Logistic Regression, Forward Selection, ROC/AUC Analysis, Residual Diagnostics  
- **Tools**: Python (`statsmodels`, `scikit-learn`, `pandas`, `seaborn`, `matplotlib`)  
- **Key Takeaway**: Salary increases ~\$9,387 per year on average. Logistic regression predicted U.S. residence with 91% accuracy (AUC = 0.92).  
- **Skills Learned**: Performing regression model selection, interpreting coefficients, and applying classification metrics to evaluate binary outcomes.  

---

## Skills Summary

### Programming & Tools
- **Python**: scikit-learn, Pandas, NumPy, Matplotlib, Seaborn, Statsmodels, SciPy  
- **R**: ggplot2, car, leaps, MASS, pls  
- **Jupyter Notebook, R Markdown, Git/GitHub**  

### Data Science Techniques
- Exploratory Data Analysis (EDA) and Visualization  
- Statistical Modeling: Linear Regression, Logistic Regression, Model Selection (AIC, BIC, Cp)  
- Regularization: Ridge Regression, Lasso Regression  
- Dimensionality Reduction: Principal Component Regression (PCR), PCA  
- Machine Learning: Decision Trees, KNN, Neural Networks  
- Model Diagnostics: Residual Analysis, Multicollinearity (VIF), ROC/AUC, Threshold Tuning  
- Resampling & Inference: Bootstrap Confidence Intervals, Hypothesis Testing with Simulation  

---

## How to Explore
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Data-Science-Projects.git
   cd Data-Science-Projects
2. Open any project folder (Case Study 1, FinalProject, project_02, etc.).
3. Each project folder contains its own README with details, methods, and results.

## Author

Trustan Gabriel Price

University of Illinois Urbana-Champaign

B.S. in Statistics | Minors in Computer Science and Data Science
