# 🤖 Predicting Monthly AI Tool Spending
### Multiple Linear Regression Model with Scikit-Learn
 
![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-MLR-orange?style=flat&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat&logo=pandas&logoColor=white)
![Colab](https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?style=flat&logo=googlecolab&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat)
 
---
 
## 📌 Overview
 
As AI tools become a growing part of everyday work and study, understanding what drives people to spend more on them is a relevant and practical question. This project builds a **Multiple Linear Regression (MLR)** model using Python and Scikit-Learn to predict how much a person spends monthly on AI tool subscriptions — based on four key factors.
 
---
 
## 🎯 Variables
 
| Type | Variable | Description | Unit |
|------|----------|-------------|------|
| Independent | `num_ai_tools` | Number of AI tool subscriptions | count (1–10) |
| Independent | `daily_usage_hours` | Average hours per day using AI tools | hours (0.5–8) |
| Independent | `monthly_income_usd` | Individual's monthly income | USD |
| Independent | `tech_experience_years` | Years of experience in a tech field | years (0–20) |
| **Dependent** | **`monthly_ai_spending_usd`** | **Monthly spending on AI subscriptions** | **USD** |
 
**Hypothesis:** People who subscribe to more AI tools, use them longer daily, earn higher incomes, and have more tech experience tend to spend more on AI tools each month.
 
---
 
## 📁 Files
 
```
mlr-ai-spending-sklearn/
├── ai_tool_spending_dataset.csv   # Dataset (60 rows, 5 columns)
├── MLR_AI_Tool_Spending.ipynb     # Google Colab notebook
└── README.md
```
 
---
 
## 🔬 Methodology
 
The notebook walks through the full MLR pipeline:
 
1. **Import Libraries & Load Dataset** — Load CSV directly from GitHub using `pd.read_csv()`
2. **Prepare Variables** — Define feature matrix X and target y, split 80/20 train-test
3. **Correlation Analysis** — Seaborn heatmap to visualize relationships between variables
4. **Fit the Model** — Train `LinearRegression()` from Scikit-Learn on the training set
5. **Interpret Coefficients** — Extract intercept and slopes to form the regression equation
6. **Evaluate Performance** — Compute MSE, RMSE, and R² Score on the test set
7. **Actual vs. Predicted Plot** — Scatter plot with perfect-fit reference line and R² annotation
8. **User Input Simulation** — Interactive predictor: enter your own values and get a spending estimate
---
 
## 📊 Results
 
| Metric | Value |
|--------|-------|
| R² Score | ~0.93 |
| RMSE | ~$11 USD |
 
The model explains approximately **93% of the variance** in monthly AI tool spending, with predictions accurate to within about $11 on average.
 
**Regression Equation:**
```
monthly_ai_spending = β₀ + β₁(num_ai_tools) + β₂(daily_usage_hours)
                         + β₃(monthly_income_usd) + β₄(tech_experience_years)
```
 
---
 
## 🚀 How to Run
 
1. Open the notebook in **Google Colab**
2. Run **Step 1** — paste the raw GitHub CSV URL when prompted:
   ```
   https://raw.githubusercontent.com/jeromenazario/mlr-ai-spending-sklearn/refs/heads/main/ai_tool_spending_dataset.csv
   ```
3. Run all remaining cells in order
4. In **Step 8**, enter your own values to get a personalized prediction
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jeromenazario/mlr-ai-spending-sklearn/blob/main/MLR_AI_Tool_Spending.ipynb)
 
---
 
## 🛠️ Tech Stack
 
- **Python 3.10+**
- **Pandas** — data loading and manipulation
- **NumPy** — numerical operations
- **Matplotlib & Seaborn** — data visualization
- **Scikit-Learn** — model training and evaluation
---
 
## 👤 Author
 
**Jerome Nazario**
- GitHub: [@jeromenazario](https://github.com/jeromenazario)
---
 
*Built as part of a Machine Learning course project.*
