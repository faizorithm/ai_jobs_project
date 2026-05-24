# Is Your Salary Safe from Artificial Intelligence?
### Predicting Job Loss and Growth in the Age of AI
**Faiza Sarker | CSCI 39542 Intro to Data Science | Spring 2026**

## To Run This Project
1. Install required libraries:
   pip install pandas numpy matplotlib scikit-learn mlxtend openpyxl
2. Download the datasets and place them in the same folder as the notebook:
   - postings.csv — LinkedIn Job Postings (Kaggle)
   - salaries.csv — LinkedIn Job Postings (Kaggle)
   - job_skills.csv — LinkedIn Job Postings (Kaggle)
   - national_M2025_dl.xlsx — BLS OEWS May 2025 (bls.gov)
   - ai_job_trends_dataset.csv — AI Job Trends Dataset (Kaggle)
3. Open main.ipynb
4. Run all cells from top to bottom

## Project Summary
Every LinkedIn post says the same thing: AI is taking over jobs. But what about the jobs 
it's creating? And does earning more actually protect you?

This project uses real data to find out — combining 124K+ LinkedIn job postings, Bureau of 
Labor Statistics wage data, and an AI job trends dataset covering 30,000 occupations to 
answer one question: **Is your salary saving you?**

### Exploratory Data Analysis (EDA)
- **Salary Distribution** *(Histogram)* — How pay is spread across the LinkedIn job market (spoiler: 87.9% earn under $150K)
- **Employment Type vs. Salary** *(Bar Chart)* — Full-time roles average $95K vs. $59K for part-time
- **Salary vs. Job Views** *(Scatter Plot)* — Does higher pay attract more applicants?
- **Automation Risk vs. Salary** *(Scatter Plot)* — The core visualization: are high earners actually safer?
- **Top 10 Highest Paying Job Titles** *(Horizontal Bar Chart)* — Which roles sit at the top of the salary distribution
- **Industry Automation Risk** *(Bar Chart)* — Finance and Healthcare both exceed the 50.2% average risk score
- **2024 vs. 2030 Job Projections** *(Grouped Bar Chart)* — Which industries AI is growing, not just shrinking

### Machine Learning
**K-Means Clustering (k=3)**
Groups LinkedIn job postings by salary and posting views to identify natural labor market segments — entry-level, professional, and executive roles.

**Logistic Regression Classifier**
Predicts whether an occupation is Increasing or Decreasing using:
- Automation Risk (%)
- Median Salary (USD)
- Job Openings (2024)

Model accuracy: ~51% ... barely above random. Which is itself the finding.

### Key Takeaway
The real dividing line isn't what you earn — it's what you *do*.
