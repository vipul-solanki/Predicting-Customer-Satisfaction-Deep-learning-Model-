
# Proactive Customer Satisfaction Prediction 🚀

View notebook in [nbviewer](https://nbviewer.org/github/vipul-solanki/Predicting-Customer-Satisfaction-Deep-learning-Model-/blob/main/DL_Submission.ipynb)

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![Framework](https://img.shields.io/badge/Framework-TensorFlow/Keras-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

This project tackles a common problem for e-commerce platforms: **How can we know if a customer is unhappy *before* they leave a bad review?** Instead of relying on slow, reactive surveys, this project builds a deep learning model to predict a customer's satisfaction score in real-time, based on the data from their support interaction.

The goal is to turn customer service from a reactive "damage control" unit into a proactive "customer happiness" engine.

---
## Key Features ✨
* **Deep Exploratory Data Analysis (EDA):** A full investigation into the data with over 10+ visualizations to uncover hidden patterns and tell a story.
* **Multi-Input Neural Network:** A special two-branch neural network designed to simultaneously understand different types of data:
    * An **LSTM branch** to analyze the sentiment and context of customer's text comments.
    * A **Dense branch** to learn from tabular data like issue category, agent tenure, and item price.
* **Optimized Training:** Implemented **Early Stopping** to train the model efficiently, prevent overfitting, and automatically find the best version of the model.
* **Model Interpretability with SHAP:** Used advanced SHAP (SHapley Additive exPlanations) techniques to look inside the "black box" model and understand exactly *why* it makes its predictions.

---
## The Core Insight 🎯
After building and analyzing the model, one finding stood out above all others:

> **Response Time is the most critical factor influencing customer satisfaction.**

Our final SHAP analysis proved that `response_time_minutes` was overwhelmingly the most important feature the model used to predict a customer's CSAT score. This provides a clear, actionable insight for the business: the fastest way to improve satisfaction is to improve response speed.

---
## Model Performance 📊
The final, optimized model achieved a **Mean Absolute Error (MAE) of 0.84** on the unseen test set.

This means, on average, the model's prediction of a customer's 1-5 satisfaction score is off by only **0.84 points**, providing a solid and reliable predictive signal.

---
## Visual Highlights
 <table>
  <tr>
    <td align="center"><b>Response Time is a Key Driver</b></td>
    <td align="center"><b>Feature Importance (SHAP)</b></td>
  </tr>
  <tr>
    <td><img src="[RESPONSE TIME CHART](https://github.com/vipul-solanki/Predicting-Customer-Satisfaction-Deep-learning-Model-/blob/main/Response%20Time%20vs.%20CSAT%20Score.png)" alt="Box plot showing that lower CSAT scores are linked to higher response times." width="100%"></td>
    <td><img src="[SHAP PLOT](https://github.com/vipul-solanki/Predicting-Customer-Satisfaction-Deep-learning-Model-/blob/main/shap_chart.png)" alt="SHAP summary plot showing response_time_minutes as the most important feature." width="100%"></td>
  </tr>
 </table>



---
## Tech Stack 💻
* Python
* TensorFlow & Keras
* Pandas for data manipulation
* Scikit-learn for preprocessing
* Seaborn & Matplotlib for visualization
* SHAP for model interpretability

---
## How to Run This Project 🏃‍♂️
1.  **Clone the repository:**
    ```bash
    git clone https://github.com/vipul-solanki/Predicting-Customer-Satisfaction-Deep-learning-Model-
    ```
2.  **Install dependencies:**
    It's recommended to create a virtual environment first. All required libraries are listed at the top of the notebook and can be installed via pip.
3.  **Run the Notebook:**
    Open the `eCommerce_CSAT_Prediction.ipynb` file in Google Colab or a local Jupyter environment and run the cells sequentially.

