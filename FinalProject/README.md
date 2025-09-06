# Diagnosing Diabetes with Machine Learning

## Project Overview
This project investigates the use of machine learning techniques to predict diabetes and prediabetes using health indicators from the **Behavioral Risk Factor Surveillance System (BRFSS) 2015 dataset**. The dataset contains over 250,000 observations with 21 health-related features, making it well-suited for modeling chronic health conditions.

The original outcome variable had three classes:  
- 0 = No Diabetes  
- 1 = Prediabetes  
- 2 = Diabetes  

For practical purposes and to reduce misclassification risk, classes 1 and 2 were merged into a binary outcome:  
- 0 = No Diabetes  
- 1 = Diabetes or Prediabetes  

This binary setup emphasizes **recall for the diabetic class**, minimizing false negatives, which are especially costly in medical applications where undiagnosed cases may lead to severe health complications.

## Dataset
- Source: Behavioral Risk Factor Surveillance System (BRFSS) 2015  
- Observations: 253,680  
- Features: 22 health and demographic indicators  
- Target: Binary diabetes status (0 or 1)

Key predictors include:
- Demographics: Age, Sex, Education, Income  
- Health metrics: BMI, Blood Pressure, Cholesterol  
- Lifestyle factors: Smoking, Physical Activity, Alcohol Consumption  
- General and mental health indicators

## Models Implemented
1. **Decision Tree Classifier (Model 0)**  
   - Initial attempt with the three-class outcome  
   - Poor recall for prediabetes (3.4%) and diabetes (30.9%)  
   - Led to reformulation as a binary classification task  

2. **Logistic Regression (Model 1)**  
   - Reduced model by removing weaker predictors  
   - Accuracy ~82%, recall ~48% (threshold tuned to 0.3)  
   - Interpretable, but still struggled with false negatives  

3. **K-Nearest Neighbors (Model 2)**  
   - Applied PCA (17 components capturing 90% variance)  
   - k = 37 chosen via cross-validation  
   - Accuracy ~91%, recall ~88% for diabetic class  
   - Strongest model overall  

4. **Neural Network (MLP Classifier, Model 3)**  
   - Grid search for hyperparameter tuning  
   - Best recall for diabetic class achieved by lowering threshold to 0.3  
   - Accuracy ~82%, recall ~55% for diabetic class  

## Results Summary

| Model                  | Accuracy | Recall (Diabetic Class) | Precision | F1-Score | Balanced Accuracy |
|-------------------------|----------|--------------------------|-----------|----------|-------------------|
| Decision Tree (3-class) | 77%      | 30.9%                   | 38.1%     | 33.8%    | —                 |
| Logistic Regression     | 82.1%    | 48.4%                   | 43.6%     | 45.9%    | 68.4%             |
| KNN (k=37, PCA)         | 91.4%    | 88.0%                   | 91.8%     | 89.9%    | 76.0%             |
| MLP (threshold=0.3)     | 82.0%    | 55.0%                   | 43.0%     | 48.2%    | 69.0%             |

## Key Findings
- The KNN model emerged as the top performer, achieving high accuracy and strong recall, aligning with the medical priority of minimizing false negatives.  
- Logistic Regression offered interpretability but struggled with sensitivity.  
- The MLP classifier provided a balance between flexibility and recall, though requiring more tuning.  
- Decision Trees failed in the original multiclass setting, highlighting the importance of reframing the classification task.  

## Improvements for Future Work
- Apply **SMOTE resampling** or class-weighting to further address imbalance.  
- Explore **Voting Classifier ensembles** to combine model strengths.  
- Expand hyperparameter tuning for MLP and KNN.  
- Add interpretability methods such as **SHAP values** for clinical decision support.  

## Tools and Technologies
- **Languages**: Python, R  
- **Libraries**: scikit-learn, NumPy, Pandas, Matplotlib, Seaborn, caret, ROSE  
- **Techniques**: Logistic Regression, Decision Trees, KNN, MLP Neural Networks, PCA, threshold tuning, model diagnostics  

## How to Run
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/data-science-projects.git
   cd data-science-projects/diabetes-prediction
2. Open the Jupyter Notebook or R scripts in the project folder.
3. Run the analysis to reproduce preprocessing, modeling, and evaluation steps.\

## Authors and Contributions

Marta Przybylska (martap4@illinois.edu) 
– Wrote the introduction section.

Nate White (nathanw7@illinois.edu) 
– Implemented the KNN code.

**Trustan Gabriel Price (tpric5@illinois.edu) **
– Developed all other code and analyses, wrote discussions, and compiled the final project report for submission.

University of Illinois Urbana-Champaign
