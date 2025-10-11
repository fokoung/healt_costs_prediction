Sure — here’s your cleaned, professional `README.md` in plain text format (no emojis, no markdown formatting):

---

# Health Cost Predictor

## Overview

Health Cost Predictor is a full-stack web application that predicts annual health insurance costs based on user inputs. It uses a deep learning regression model built with TensorFlow and Keras, served through a Flask backend, and presented via a modern, responsive HTML + Tailwind CSS frontend.

This project demonstrates a complete machine learning pipeline — from data preprocessing and model training in a Jupyter Notebook, to deploying the model through a REST API, and creating a seamless user interface for real-time interaction.

## Features

* Interactive Predictions: Enter your age, BMI, number of children, smoking status, sex, and region to instantly get a cost prediction.
* Modern UI/UX: Clean and responsive interface with frosted-glass styling and smooth animations.
* RESTful Backend: A lightweight Flask server exposes the trained TensorFlow model via a simple /predict API endpoint.
* Decoupled Architecture: The frontend and backend are completely independent, supporting easy updates and scaling.

## Tech Stack

Backend: Python, Flask, TensorFlow/Keras, Pandas
Frontend: HTML, Tailwind CSS, JavaScript
Model Training: Jupyter Notebook

## Setup and Installation

Follow the steps below to run the project locally.

1. Prerequisites

   * Python 3.8 or higher
   * pip and venv for package management

2. Clone the Repository
   git clone [https://your-repository-url.git](https://your-repository-url.git)
   cd health-cost-predictor

3. Set Up the Backend

   Create and activate a virtual environment:
   python3 -m venv .venv
   source .venv/bin/activate
   (On Windows: .venv\Scripts\activate)

   Install dependencies:
   pip install tensorflow pandas flask flask-cors

   Train and Export the Model:

   * Open Copie_de_fcc_predict_health_costs_with_regression.ipynb in Jupyter Notebook.
   * Run all cells to train the model.
   * At the end, export the model with:
     model.export('health_cost_predictor')

   This creates a folder named health_cost_predictor/ in your project directory.
   Ensure the health_cost_predictor folder is in the same directory as app.py.

   Run the Flask Server:
   python app.py
   The backend will start at [http://127.0.0.1:5000](http://127.0.0.1:5000).
   If successful, you’ll see a message confirming that the model loaded properly.

4. Run the Frontend
   Open the index.html file in your web browser (Chrome, Firefox, etc.).
   Once the page loads, fill out the form, click “Predict Cost,” and view your predicted health insurance cost instantly.

## How It Works

1. The user fills out the form in index.html and clicks “Predict Cost.”
2. JavaScript captures the inputs, builds a JSON object, and sends a POST request to /predict.
3. The Flask server (app.py) receives and preprocesses the data:

   * One-hot encodes categorical variables.
   * Computes interaction features like bmi_smoker.
4. The preprocessed data is fed into the loaded TensorFlow model.
5. The model outputs a predicted annual cost.
6. Flask sends this result back as JSON.
7. The frontend dynamically updates the page to display the prediction.

## Future Improvements

* Add user authentication and prediction history.
* Containerize with Docker for easier deployment.
* Integrate with a database to log predictions and analyze trends.
* Deploy the full stack on Render, Vercel, or AWS.


---

