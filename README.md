# Gold-and-Silver-price-prediction-project

🔰 **Project Title:**
Gold and Silver Price Prediction Using Machine Learning and Flask Web Application

**📘 Project Description:**
-->This project aims to predict the next-day prices of gold and silver in the Indian market using Machine Learning techniques. The model leverages a variety of economic and market factors such as global gold/silver prices, USD/INR exchange rate, inflation indicators, repo rates, and sentiment scores.

-->The ML model is trained using historical data and deployed through a Flask-based web application, allowing users such as traders, investors, or jewelers to input current market conditions and receive real-time price predictions.

🎯 **Project Objectives:**
-Predict future gold and silver prices using regression models.

-Build an interactive web app where users can enter market values and receive predictions.

-Analyze key economic indicators affecting price fluctuations.

-Make the tool accessible for decision-making in trading and investments.


🧠 Machine Learning Details:
Model Type: Supervised Learning (Regression)

Algorithm Used: Random Forest Regressor (or other alternatives like XGBoost, LSTM)

Features Used:

  USD/INR Exchange Rate

  Global Gold and Silver Prices (USD)
 
  Inflation (India CPI)

  RBI Repo Rate

Sentiment Scores (Geopolitical & Market)

Seasonal Indicators

Commodity Demand (Gold/Silver)

Target Variables:

Gold_Price_Next_Day

Silver_Price_Next_Day

🖥️ Web App (Flask) Features:
Input Form:

Users input economic and market parameters.

Output:

Predicted price of gold for the next day.

Frontend:

Built with HTML and integrated into Flask using Jinja2 templates.

Backend:

Flask handles input routing, model loading, and prediction display.

📊 Tools & Technologies Used:
Tool	Use
Python	Core programming language
Pandas, NumPy	Data preprocessing
Scikit-learn	Model training
Flask	Web app backend
HTML/CSS	Frontend interface
Google Colab	Model development and training
Matplotlib/Seaborn	Data visualization (EDA)

🧪 Project Workflow:
Data Collection (Historical gold/silver prices & economic indicators)

Data Preprocessing (cleaning, encoding, feature engineering)

Model Training (Random Forest Regressor in Colab)

Model Export (model_gold.pkl)

Flask App Development (user input form + output prediction)

Web App Deployment (local, Render or Streamlit options)

✅ Final Output:
A trained model capable of predicting gold prices based on real-world features.

A working Flask web application that takes user inputs and displays the predicted price.

