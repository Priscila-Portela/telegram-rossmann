# SALES PREDICTION

!(img/rossmann.png)

# DESCRIPTION
This an end-to-end data science project to predict daily sales for Rossmann stores across multiple locations. The primary focus is on developing a robust machine learning model to accurately forecast sales and assist the management in making data-driven decisions.
# TECHNOLOGIES AND TOOLS
The technologies and tools used were: Python (Pandas, Nump, Seaborn, MatPlotLib, Scikit-learn and Flask), Jupyter Notebook, Git, GitHub, Machine Learning Regression Algorithms, PyEnv, Linux Terminal, Render.com, Telegram, Visual Studio Code.

# BUSINESS PROBLEM AND PROJECT OBJECTIVE 
* Rossmann operates over 3,000 drug stores across seven European countries. Store managers are tasked with predicting the daily sales for the upcoming weeks.

* The goal of this project is to create a model that can predict daily sales for Rossmann stores and help in inventory management, staffing, and marketing strategies.

# SOLUTION PIPELINE
1. Understand and define the business problem
2. Collect data
3. Obtain a general understanding of the dataset
4. Cleaning and pre-processing of data
5. Descriptive statistics
6. Creation of exploratory hypotheses (empirical)
7. Feature Engineering
8. Features Filter
9. Exploratory Data Analysis (EDA), through validation or not of the hypotheses created
10. Data preparation (rescaling, encoding and transformation)
11. Split into training and test dataset
12. Feature selection (Boruta)
13. Machine Learning Modeling (average, linear regression, linear regression regularized, random forest and XGboost)
14. Compare model’s performance
15. Hyperparameters fine tuning (Random search)
16. Training the final model and predicting (XGBoost)
17. Translate and interpret the error creating best and worst case scenarios of predictions based on the error (MAE)
18. Deploy the model to production

# Main business insights


* Stores with larger assortment tend to have higher average daily sales.
(img/graph1.png)
(img/graph1.1.png)
(img/graph1.2.png)
(img/graph1.3.png)

* Stores with the "extra" assortment have higher average daily sales. However, due to the smaller number of stores in this segment, the total contribution to sales is minimal. On the other hand, "basic" and "extended" stores dominate in terms of number and total sales volume, being the main contributors to the company's overall revenue.

(img/graph2.png)

* The average daily sales on holidays, as expected, are higher than on normal days.

(img/graph3.png)

* In all years (2013, 2014 and 2015), there is a significant spike in sales in December. This increase is likely driven by holiday shopping, suggesting that December is the most profitable month.

* January and February show a decline in sales compared to December, but sales are still relatively strong. In 2015, sales increase in February, reaching a higher peak than in January.

* In 2014, sales dropped sharply in August, which may indicate a specific event that negatively impacted sales that year. In other years, August shows a recovery after the decline in previous months.

* December is clearly a key month for sales, and additional marketing and inventory efforts may be warranted to maximize profits in this month.


# Modeling
* Preprocessing: The preprocessing steps for this project involved encoding categorical variables to prepare the data for modeling.
* Feature Selection: We utilized the Boruta algorithm for initial feature selection. Following this, features were manually selected to ensure optimal model performance.
* Model Selection: Various regression models were trained and evaluated. Although XGBoost did not deliver the best performance compared to Random Forest Regressor, for exemple, it was chosen due to its lightweight nature. This characteristic facilitated easier deployment and integration into the project.
(img/model_performance.png)

# Business Performance and Financial Reports
* Sales Prediction Scenarios: Sales were predicted for both the best-case and worst-case scenarios as anticipated by the algorithm.
*Prediction Accuracy: The algorithm effectively identified and predicted the major sales peaks and troughs with high clarity.
* Investment Planning: Daily sales forecasts for each Rossmann store enable more secure investment planning. These results are accessible via the Telegram messaging app for convenience.
  
# Web Application
## Overview
After developing the model, a Flask API was created and integrated into a Telegram bot. Users can interact with the bot to retrieve sales forecasts by sending the store number (ID) via chat.
## Telegram Bot Usage

### Run This Project Locally
Requirements:
A mobile device with iOS or Android updated to the latest version.
The Telegram app, available on the App Store or Google Play.
Setup Instructions:
Connect with the bot using the following link: Rossmann Forecasting Bot.
Send the store number (ID) in the chat to obtain the sales prediction for the next six weeks.
* Example Output:

## Note:
* After several hours of inactivity, the bot may enter a rest mode. In this case, the response to the first message upon reactivation might take up to 2 minutes. When active, the bot returns sales forecasts immediately.
# Additional Information
## Data Analysis and Model Performance Metrics 
For detailed performance metrics, model evaluation results, a complete exploratory data analysis and complete code refer to the notebook (End-to-End_Sales_Forecasting.ipynb) in this folder .
## Data Sources
The data used in this project is sourced from kaggle [https://www.kaggle.com/c/rossmann-store-sales/data]. Ensure you have access to this data if you wish to reproduce the results.

