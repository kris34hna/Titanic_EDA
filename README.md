# Titanic Survival - Exploratory Data Analysis

Exploring passenger demographics and travel details from the Titanic disaster to uncover what factors influenced survival.

---

# Brief Summary

An exploratory data analysis (EDA) on the classic Titanic dataset (891 passengers), examining how gender, passenger class, age, family size, and embarkation point relate to survival outcomes using Pandas, Matplotlib, and Seaborn.

---

# Overview

This project investigates the famous Titanic dataset to understand the demographic and socio-economic patterns behind passenger survival. The analysis covers survival distribution, gender-based survival rates, embarkation patterns, family size effects (siblings/spouses & parents/children), age distributions, and a custom-engineered "Life Stage" feature, all tied together with correlation analysis.

---

# Dataset

Key Columns:

|Column | Description |
|-------|-------------|
|PassengerId | Unique passenger ID (no predictive value) |
|Survived | Target — 1 = Survived, 0 = Did not survive |
|Pclass | Passenger class — 1 Upper, 2 Middle, 3 Lower |
|Name | Passenger name |
|Sex | Gender |
|Age | Age in years |
|SibSp | # of siblings/spouses aboard |
|Parch | # of parents/children aboard |
|Ticket | Ticket number |
|Fare | Ticket fare paid |
|Cabin | Cabin number |
|Embarked | Port of embarkation — C Cherbourg, Q Queenstown, S Southampton |

---

# Tools & Technologies

|Tool | Purpose |
|-----|---------|
|Python | Core language |
|Pandas / NumPy | Data manipulation & cleaning |
|Matplotlib / Seaborn | Visualizations (countplots, pie charts, pairplots, heatmaps, displots) |
|Jupyter Notebook | Development environment |

---

# Methods

-1.  Initial Inspection — Checked shape, data types, unique value counts, duplicates, missing value percentages, and descriptive statistics (numeric & categorical).
-2.  Categorical & Numerical Split — Separated columns into cat_cols (Survived, Pclass, Sex, SibSp, Parch, Embarked) and num_cols (Age, Fare) for targeted analysis.
-3.  Survival Overview — Countplot and grouped aggregation to determine overall survival counts and rate.
-4.  Gender-Based Survival — Pie charts comparing survival proportions between male and female passengers.
-5.  Pairplot Analysis — Full pairwise relationships across numeric variables, colored by gender.
-6.  Embarkation Analysis — Multi-panel plots examining passenger counts and survival by embarkation port.
-7.  Family Size Analysis (SibSp & Parch) — Bar plots of survival rate against number of siblings/spouses and parents/children aboard.
-8.  Correlation Matrix — Heatmap of all numeric variables to identify relationships with survival.
-9.  Age Distribution — Displot (histogram + KDE + rug) split by gender and survival status.
-10. Feature Engineering — Life Stage — Created a new LifeStage column bucketing passengers into Infant, Toddler, Child, Teen, and other age groups for deeper survival analysis.



💡 Key Insights


🛟 The dataset shows a clear survival imbalance — fewer passengers survived than perished, consistent with the historical death toll.
👩‍🦰👨 Gender was a major survival factor — the pie chart breakdown shows a stark contrast between male and female survival proportions, reflecting the "women and children first" evacuation protocol.
⚓ Embarkation port shows uneven passenger distribution, with Southampton (S) contributing the largest share of passengers.
👨‍👩‍👧 Family size mattered — survival rate trends differ across SibSp and Parch values, suggesting passengers with small families had different survival odds than those traveling alone or in large groups.
📈 The correlation heatmap highlights relationships between Pclass, Fare, and Survived — passenger class and fare are meaningful numeric predictors of survival.
👶 The Age distribution split by survival and gender reveals different age profiles among survivors vs. non-survivors.
🧒 The custom LifeStage feature (Infant, Toddler, Child, Teen, etc.) enables a more granular look at how survival varied not just by raw age, but by life-stage category.



📊 Dashboard / Output

This project's output is the Jupyter Notebook (Titanic.ipynb) containing:


Survival count plots & grouped survival rate
Gender-based survival pie charts
Full pairplot colored by gender
Embarkation port analysis (4-panel visualization)
Family size (SibSp/Parch) vs. survival bar plots
Correlation matrix heatmap
Age distribution displot (by gender & survival)
Life Stage feature engineering & analysis



▶️ How to Run This Project

bash# 1. Clone the repository
git clone <your-repo-url>
cd titanic-eda

# 2. Install dependencies
pip install numpy pandas matplotlib seaborn jupyter

# 3. Launch the notebook
jupyter notebook Titanic.ipynb

# 4. Ensure train.csv is in the same directory before running


✅ Results & Conclusion

This EDA confirms several well-known patterns from the Titanic disaster — survival was strongly influenced by gender, passenger class, and family configuration, with women, higher-class passengers, and those in small family groups generally faring better. Age and life-stage analysis further reveals that children had different survival dynamics compared to adults. These insights lay a strong foundation for predictive modeling on survival outcomes.


🔮 Future Work


🤖 Build a survival prediction model (Logistic Regression, Random Forest, XGBoost)
🧹 Handle missing values in Age, Cabin, and Embarked with imputation strategies
🔤 Engineer new features from Name (titles like Mr./Mrs./Master) and Cabin (deck level)
📊 Perform feature importance analysis to rank top survival predictors
🌐 Deploy the model as an interactive "Would I have survived?" web app



👤 Author & Contact

Name(Your Name)LinkedIn(your-linkedin-url)GitHub(your-github-username)Email(your-email@example.com)


⭐ If you found this project helpful, consider giving it a star!
