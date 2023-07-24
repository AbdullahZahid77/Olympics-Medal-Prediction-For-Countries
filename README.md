# Olympics-Medal-Prediction-For-Countries

This Python machine-learning project aims to predict the number of medals each country will win at the Olympic Games based on historical data. The project utilizes a linear regression model to make predictions. The dataset contains information about various countries, their athletes, age, previous medals won, and the number of medals they won in a given year.

# Dataset
The dataset used for this project is loaded from the 'teams.csv' file, containing the following columns:
'team': Name of the team participating in the Olympics.
'country': Country represented by the team.
'year': Year of the Olympic Games.
'athletes': Number of athletes representing the team in a particular year.
'age': Average age of the athletes.
'prev_medals': Number of medals won by the country in previous Olympic Games.
'medals': The target variable, representing the number of medals won by the country in a specific year.

# Data Exploration
The project starts with data exploration, analyzing correlations between the 'medals' and other numerical features like 'athletes' and 'prev_medals.' A linear regression model is considered appropriate for prediction since a high correlation is observed between 'medals' and these features.

# Data Preprocessing
Missing values in the dataset are handled by dropping rows containing any NaN values. The data is then split into training data, containing records before the year 2012, and test data, containing records from 2012 onwards.

# Model Training and Prediction
The linear regression model is trained on the training data using the 'athletes' and 'prev_medals' columns as predictors and 'medals' as the target variable. The model is used to make predictions on the test data.

# Error Analysis
The mean absolute error is calculated to evaluate the model's performance on the test data. The error is found to be below the standard deviation of the 'medals' column, indicating a reasonable level of accuracy in the predictions.

Additionally, an error ratio is calculated for each country by dividing the mean absolute error by the mean number of medals won by that country. The error ratios are then plotted as a histogram, providing insight into the predictive performance of different countries.

Overall, this project demonstrates a simple yet effective approach to predicting Olympic medals using a linear regression model based on historical data. The error analysis helps identify potential areas for improvement in the model and provides valuable information for countries to estimate their medal counts in future Olympic Games.
