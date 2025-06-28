# insurance-charges-regression-modeling

**📊 Insurance Cost Prediction (First End-to-End ML Workflow)**
This project is my first attempt to build a complete machine learning pipeline from scratch for regression.
The main goal was not only to predict insurance charges but to learn how a professional modeling workflow is structured—from raw data to evaluation.

**📂 Project Overview**
Problem:
Predict insurance claim amounts (charges) based on customer demographics and health-related information.

**Dataset:**

~1,300 rows
Columns:
age
sex
bmi
children
smoker
region
charges (target variable)

**🛠️ Workflow Steps**
I tried to follow a structured, step-by-step process similar to how it’s done in the industry:

**1️⃣ Exploratory Data Analysis**
Checked the distribution of charges (found it to be heavily skewed).

Reviewed correlations between numeric variables and the target.

**2️⃣ Data Preprocessing**
One-hot encoding of categorical variables (sex, smoker, region).

Verified multicollinearity using Variance Inflation Factor (VIF).

Decided not to scale features initially because tree-based models don’t require scaling.

**3️⃣ Baseline Models**
> Linear Regression to establish a reference performance.

> Applied Ridge and Lasso Regression to see if regularization improved results.

-In this case, regularization did not lead to significant improvements.

**4️⃣ Nonlinear Models**
> Decision Tree Regressor
- Helped capture interactions and non-linear relationships.

> Random Forest Regressor
-Reduced variance and improved RMSE.

> Gradient Boosting Regressor
- Delivered the best overall performance.

**5️⃣ Hyperparameter Tuning**
> Used GridSearchCV to find the best parameters for Gradient Boosting.

> Tried different learning rates, max depths, and subsampling rates.

**6️⃣ Evaluation**
> Measured RMSE and R² for all models.

> Compared models side by side.

> Visualized actual vs. predicted charges to check model accuracy.

**🚀 Results Summary**
**Model          	RMSE	 R²**
Linear Regression	~5794	0.78
Ridge Regression	~5794	0.78
Lasso Regression	~5794	0.78
Decision Tree	    ~5042	0.83
Random Forest	    ~4499	0.87
Gradient Boosting	~4349	0.88
Best Gradient Boosting	~4381	0.88

**✅ Gradient Boosting achieved the lowest RMSE and explained ~88% of the variance.**

**💡 What I Learned**
> Building a pipeline step by step is crucial. It helps you understand why each step is needed.

> Linear models are often not enough when the target variable is skewed or has nonlinear relationships.

> Tree-based ensembles like Random Forest and Gradient Boosting can substantially improve accuracy without requiring feature scaling.

> Grid search is useful to fine-tune hyperparameters and find better-performing models.

> Model evaluation should combine metrics and visual checks, such as residual plots or predicted vs. actual comparisons.

> This project gave me confidence to tackle more complex modeling workflows in the future.

**🤝 Acknowledgments
Thanks to the open-source Python community for tools like:**
Pandas
Scikit-Learn
Matplotlib and Seaborn

**🙌 About This Project:**
This was my first attempt at learning and practicing a full modeling workflow, and I’m sharing it to help others who are starting their journey in machine learning.
Feel free to connect if you’d like to discuss or collaborate!
