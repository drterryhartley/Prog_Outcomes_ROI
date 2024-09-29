# Prog_Outcomes_ROI
Predicted savings (ROI) based on forecasted program outcomes and membership changes

Objective
The goal is to develop a model that predicts Return on Investment (ROI) based on forecasted provider quality outcomes, membership trends, and other healthcare program metrics. Additionally, the project involves validating whether the dataset meets the assumptions for running a linear regression model and generating a report comparing the predicted savings (ROI) with actual program expenditures.
Key Steps

1. Data Preparation
 We generated sample data representing the healthcare program’s quality measures and financial outcomes. The key variables include:
 •	Provider Quality Outcomes: How well healthcare providers perform on a scale of 0-100.
 •	Membership Trending: Predicted changes in membership (growth or decline).
 •	Program Expenditures: The actual expenditure on the program.
 •	Additional Quality Measures:
  o	Time Between Intake and Contact: Days between first contact and care delivery.
  o	Sessions per Member per Diagnosis: The number of sessions members attend for each diagnosis.
  o	Referrals In and Out: The number of external and internal referrals.
  o	Member Experience Survey Scores: Scores from the CAHPS Mental Health Surveys, such as timely appointments, provider communication, shared decision-making, customer service, and overall provider rating.
 We also generated a target variable, Predicted Savings (ROI), based on provider quality outcomes, membership trends, sessions per diagnosis, and other factors.

2. Assumptions Checks for Linear Regression
 Before running a linear regression model, it’s crucial to verify that the dataset meets the assumptions required for accurate modeling. The following assumptions were checked:
 •	Linearity: We used pair plots to visually inspect if there was a linear relationship between the independent variables and the dependent variable (Predicted Savings).
 •	Multicollinearity: We calculated the Variance Inflation Factor (VIF) to ensure that the independent variables were not highly correlated with one another (VIF < 10 for all variables).
 •	Homoscedasticity: We plotted the residuals (difference between the predicted and actual values) against the fitted values to confirm that the variance of residuals was constant.
 •	Normality of Residuals: We used a Q-Q plot and the Shapiro-Wilk test to check if the residuals were normally distributed. If the p-value of the Shapiro-Wilk test was greater than 0.05, it indicated that the residuals were normally distributed.

3. Model Development
 We split the dataset into training and testing sets and then developed a linear regression model to predict savings (ROI) based on the provided features. The features used in the model include provider quality outcomes, membership trending, program expenditures, 
 session counts, referral data, and survey scores.
 After training the model, we used it to predict the savings on the test set. The performance of the model was evaluated using the Mean Absolute Error (MAE), which measured the average magnitude of the errors between the predicted and actual savings.

4. Output and Visualization
 •	Comparison Report: After obtaining the predicted savings (ROI), we compared them to the program expenditures. A new column, Savings_vs_Expenditures, was added to represent the difference between predicted savings and actual expenditures.
 •	Visualization: A scatter plot was generated to visually compare the predicted savings (ROI) against actual program expenditures. A diagonal line represented the ideal case where savings match expenditures, and the spread of points gave an insight into how well the 
 model was performing.
 •	Summary Report: A statistical summary of the comparison between predicted savings and actual expenditures was generated to give an overview of the results.

5. Evaluation Summary
 •	Model Performance: The model was evaluated using Mean Absolute Error (MAE). A low MAE indicates that the model is performing well in predicting savings based on the given quality measures and financial inputs.
 •	Assumption Checks:
  o	Linearity: Visual inspection through pair plots confirmed that the relationship between variables was approximately linear.
  o	Multicollinearity: The VIF scores for all variables were below 10, indicating no multicollinearity issues.
  o	Homoscedasticity: The residuals plot showed that the residuals were evenly scattered around zero, indicating constant variance.
  o	Normality of Residuals: The Q-Q plot and the Shapiro-Wilk test indicated that the residuals were normally distributed.

Conclusion
The model developed in this project successfully predicts the Return on Investment (ROI) based on key healthcare quality measures and financial data. After validating the assumptions of linear regression, the model was fitted and evaluated, and the results were presented in both a comparison report and a visualization that compares predicted savings against program expenditures.
This project provides an effective approach for understanding how provider performance, membership trends, and other quality measures impact financial outcomes, allowing for better decision-making regarding healthcare program management and financial optimization.
