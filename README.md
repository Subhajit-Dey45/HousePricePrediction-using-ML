# 🏠 House Price Prediction using Machine Learning
Contributor: Subhajit Dey


# Open in colab to view interactive plots

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1pufx1DPK2rKysDjfK7XXJyIo2z0cUPtu?usp=sharing)

📌 Introduction
This project focuses on predicting housing prices in California using machine learning techniques. The dataset contains key features related to housing characteristics, demographics, and location.

Accurate house price prediction can provide valuable insights for real estate professionals, homeowners, investors, and policymakers, enabling better decision-making in property valuation and urban planning.

🎯 Problem Statement
The goal is to predict median house values using various features of California districts.

Dataset size: 20,640 entries

Features: 10 housing, location & demographic attributes

Challenge: Estimate median_house_value with robust machine learning models

📚 Libraries & Tools Used
Data Handling: NumPy, Pandas

Visualization: Matplotlib, Seaborn, Plotly, Folium

Machine Learning: Scikit-learn, XGBoost

Dataset Source: California Housing Dataset (Kaggle)

📊 Dataset Overview
Feature	Description
longitude, latitude	Geographic location (California districts)
housing_median_age	Median age of the houses in the district
total_rooms	Total rooms in the district
total_bedrooms	Total bedrooms in the district
population	Population of the district
households	Number of households in the district
median_income	Median income of households
median_house_value	Target variable (House Price)
ocean_proximity	Proximity to ocean (‘INLAND’, ‘NEAR BAY’, etc.)
Entries: 20,640

Missing Values: Only in total_bedrooms (≈207) → handled by median imputation

🔎 Exploratory Data Analysis (EDA)
Key Insights from EDA:

Median Income shows the strongest correlation with house prices.

Location factor (longitude & latitude) highly influences prices → coastal houses are more expensive.

House values are right-skewed with an artificial cap at $500,000.

Outliers exist in population, rooms, income, etc.

New engineered features:

rooms_per_house, bedrooms_ratio, people_per_house

⚙️ Feature Engineering
Income-based categories for stratified sampling.

House value bins for classification.

One-hot encoding applied to categorical data (ocean_proximity).

🧮 Model Building
Models Trained & Compared:
Logistic Regression

Decision Tree

Random Forest

Gradient Boosting

Performance Summary:
Model	Accuracy	RMSE ↓	MAE ↓	R² ↑
Logistic Regression	67.7%	0.59	0.33	0.35
Decision Tree	74.1%	0.53	0.26	0.48
Random Forest	82.0%	0.43	0.18	0.65
Gradient Boosting	80.5%	0.45	0.20	0.62
✅ Random Forest emerged as the best performer with highest accuracy, lowest errors, and best generalization.

📈 Model Evaluation
Random Forest Final Accuracy: 82.3%

Robust across all 3 house value categories (F1-score ~0.82).

Confusion matrix shows minimal misclassification between distinct classes.

Key Takeaways:

Most errors occur when predicting Class 1 vs Class 2 (moderate vs higher house values).

Model distinguishes low-value (Class 0) and high-value (Class 2) homes quite well.

🗝️ Insights
Median income is the single most important predictor of house value.

Geography matters – close-to-coast homes are significantly more expensive.

Ensemble models (Random Forest & Gradient Boosting) outperform traditional regression.

Stratified sampling ensures balanced representation across income groups.

✅ Conclusion
Machine learning, especially Random Forest, can reliably predict California house prices with robust accuracy.

Location & income dominate pricing patterns, confirming well-known real estate principles.

The project shows the power of ensemble methods in handling skewed, high-variance datasets.

🚀 Future Work
Include external factors such as:

Crime rates

School quality

Local economic conditions

Infrastructure development

Extend analysis to regression modeling instead of categorical prediction.

Experiment with Deep Learning (Neural Networks) for further accuracy boost.
