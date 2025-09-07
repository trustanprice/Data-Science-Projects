# Data Science Salary Analysis

## Project Overview
This project explores salary trends within the global data science profession. Using a dataset of job titles, locations, experience levels, and salaries updated through 2024, we investigated two main questions:  
1. What is the salary difference between **pure data science roles** and **business-oriented data roles**?  
2. Do **European data science professionals** earn significantly less than their **North American counterparts** post-pandemic?  

By applying confidence intervals and hypothesis testing, we aimed to quantify salary differences and examine regional patterns in compensation.

## Dataset
- **Source**: [Data Science Salaries Dataset](https://www.kaggle.com/datasets)  
- **Size**: 5,736 rows × 11 columns  
- **Features**:
  - Job Title, Employment Type, Experience Level, Expertise Level  
  - Salary, Salary Currency, Salary in USD  
  - Company Location, Employee Residence  
  - Company Size, Year  
- **Timeframe**: 2020–2024  
- **Population**: Global data science professionals  

## Research Questions
1. **Confidence Interval**  
   - What proportion of employees hold purely data science roles vs. business data roles?  
   - What is the 95% confidence interval for the average salary difference between these two groups in 2024?  

2. **Hypothesis Test**  
   - Post-pandemic (2022+), are salaries for data science professionals in Europe significantly lower than those in North America?  

## Methodology
1. **Data Cleaning**
   - Verified no missing values.  
   - Split job titles into “pure data science” vs. “business/BI/marketing” categories.  
   - Filtered for 2024 and for post-pandemic years (≥2022).  

2. **Analysis**
   - Calculated descriptive statistics (mean, median, standard deviation).  
   - Constructed a **bootstrap-based 95% confidence interval** for salary differences.  
   - Performed a **hypothesis test** with simulation to compare regional salaries while avoiding assumptions of normality or equal variance.  

3. **Visualization**
   - Boxplots comparing salary distributions.  
   - Histograms of simulated sampling distributions.  
   - Confidence interval and p-value interpretation.  

## Results
- **Salary Roles Comparison (2024)**  
  - Pure Data Science roles (n=142): Mean = \$137,118 | Median = \$131,600  
  - Business Data roles (n=14): Mean = \$95,805 | Median = \$88,900  
  - **95% CI for salary difference**: (\$24,531, \$57,193)  
  - Conclusion: Pure data science roles earn significantly more on average.  

- **Regional Comparison (Post-2022)**  
  - Europe (n=644): Mean = \$91,352 | Median = \$74,961  
  - North America (n=4,653): Mean = \$156,550 | Median = \$147,800  
  - Hypothesis Test: p-value = 0.8122 → fail to reject null hypothesis.  
  - Conclusion: Despite large differences in summary statistics, the simulation found insufficient evidence to claim significant regional salary differences at α = 0.01.  

## Key Insights
- Pure data science roles pay **~\$25K–\$57K more** than business-oriented roles in 2024.  
- North America shows **higher average salaries** and a wider range of high-paying roles, but statistical evidence was insufficient to confirm a significant post-pandemic difference vs. Europe.  
- Salary distributions are **skewed and influenced by outliers**, making median a more reliable measure of center than mean.  

## Tools and Technologies
- **Languages**: Python  
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, SciPy  
- **Techniques**: Bootstrap confidence intervals, simulation-based hypothesis testing, descriptive statistics, visualization  

## How to Run
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/data-science-projects.git
   cd data-science-projects/data-science-salary-analysis
2. Install required packages:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy
   ```
3. Open the Jupyter Notebook or HTML file and run through the analysis.

## Authors and Contributions

Quinn Crockling (qdc2) – Completed part 4 analysis.

**Trustan Gabriel Price (tpric5)** – Completed parts 1–3, performed coding and statistical analysis, and finalized the project for submission.

University of Illinois Urbana-Champaign
