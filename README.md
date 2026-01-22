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



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tech Developers Directory</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #f5f7fb;
      color: #333;
    }

    header {
      background: #111827;
      color: #fff;
      padding: 15px 30px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    header h1 {
      font-size: 22px;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 20px;
    }

    nav a {
      text-decoration: none;
      color: #fff;
      font-size: 15px;
    }

    .menu-btn {
      display: none;
      font-size: 22px;
      cursor: pointer;
    }

    .hero {
      text-align: center;
      padding: 80px 20px;
      background: linear-gradient(to right, #2563eb, #1e40af);
      color: #fff;
    }

    .hero h2 {
      font-size: 36px;
      margin-bottom: 10px;
    }

    .container {
      padding: 50px 20px;
      max-width: 1200px;
      margin: auto;
    }

    .title {
      text-align: center;
      margin-bottom: 30px;
      font-size: 28px;
    }

    .developers {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
    }

    .card {
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      text-align: center;
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card img {
      width: 90px;
      border-radius: 50%;
      margin-bottom: 10px;
    }

    .card h3 {
      margin: 8px 0;
    }

    .card p {
      font-size: 14px;
      color: #555;
    }

    form {
      background: #fff;
      padding: 30px;
      border-radius: 10px;
      max-width: 500px;
      margin: auto;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    form input, form textarea {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 6px;
      border: 1px solid #ccc;
    }

    form button {
      background: #2563eb;
      color: white;
      border: none;
      padding: 12px;
      width: 100%;
      border-radius: 6px;
      cursor: pointer;
    }

    footer {
      background: #111827;
      color: #fff;
      text-align: center;
      padding: 15px;
      margin-top: 50px;
    }

    @media(max-width:768px) {
      nav ul {
        position: absolute;
        top: 60px;
        left: -100%;
        background: #111827;
        width: 100%;
        flex-direction: column;
        text-align: center;
        transition: 0.3s;
      }

      nav ul.active {
        left: 0;
      }

      .menu-btn {
        display: block;
      }
    }
  </style>
</head>

<body>

<header>
  <h1>Tech Developers</h1>
  <div class="menu-btn" onclick="toggleMenu()">☰</div>
  <nav>
    <ul id="menu">
      <li><a href="#home">Home</a></li>
      <li><a href="#developers">Developers</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>

<section class="hero" id="home">
  <h2>Find Top Tech Developers</h2>
  <p>Web, Mobile, Cloud & AI Professionals</p>
</section>

<section class="container" id="developers">
  <h2 class="title">Developer List</h2>

  <div class="developers">
    <div class="card">
      <img src="https://i.pravatar.cc/150?img=3">
      <h3>Rahul Patel</h3>
      <p>Full Stack Developer</p>
    </div>

    <div class="card">
      <img src="https://i.pravatar.cc/150?img=5">
      <h3>Anjali Shah</h3>
      <p>UI/UX Engineer</p>
    </div>

    <div class="card">
      <img src="https://i.pravatar.cc/150?img=7">
      <h3>Aman Verma</h3>
      <p>Python & AI Engineer</p>
    </div>

    <div class="card">
      <img src="https://i.pravatar.cc/150?img=9">
      <h3>Pooja Mehta</h3>
      <p>Mobile App Developer</p>
    </div>
  </div>
</section>

<section class="container" id="contact">
  <h2 class="title">Contact Developer</h2>

  <form>
    <input type="text" placeholder="Your Name" required>
    <input type="email" placeholder="Your Email" required>
    <textarea rows="4" placeholder="Your Message"></textarea>
    <button type="submit">Send Message</button>
  </form>
</section>

<footer>
  <p>© 2026 Tech Developers Directory</p>
</footer>

<script>
  function toggleMenu(){
    document.getElementById("menu").classList.toggle("active");
  }
</script>

</body>
</html>


