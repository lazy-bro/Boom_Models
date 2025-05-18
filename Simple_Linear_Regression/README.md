📊 Salary Prediction using Linear Regression
This project demonstrates how to use Linear Regression to predict salary based on years of experience using Python libraries such as pandas, matplotlib, seaborn, and scikit-learn.

📁 Dataset
The dataset used is Salary_Data.csv, which contains the following columns:
YearsExperience: Number of years of professional experience.
Salary: Annual salary in dollars.

🧪 Objective
To build a simple linear regression model that predicts salary based on years of experience.

📌 Libraries Used
pandas for data manipulation
matplotlib.pyplot & seaborn for data visualization
scikit-learn for machine learning model building and evaluation

🔍 Exploratory Data Analysis (EDA)
Viewed first 10 rows using df.head(10)
Checked correlation with df.corr()
Created visualizations:
Scatter plot of YearsExperience vs Salary
Heatmap of correlation matrix
Histogram of years of experience
Line plot showing the trend of salary with experience
Pair plot to visualize all numerical features
Checked for missing values using df.isnull().sum()

🧠 Model Building
Feature Selection
Input: YearsExperience
Output: Salary
Train-Test Split
Training size: 67%
Testing size: 33%
random_state=42 for reproducibility
Model Training
Used LinearRegression() from sklearn.linear_model
Trained model on training data
Prediction & Evaluation
Made predictions on test set
Evaluated model using R² Score

✅ Results
The R² score indicates how well the model fits the test data.
Visualization confirms a linear relationship between years of experience and salary.
