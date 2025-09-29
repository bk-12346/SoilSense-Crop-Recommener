# Sowing Success: A Machine Learning Crop Recommendation System

## 🌿 Project Overview

This project is a machine learning solution designed to assist farmers in **maximizing their crop yield** by recommending the single most suitable crop for a field based on its soil's chemical composition.

Soil testing for various metrics can be an expensive and time-consuming process. This project addresses that challenge by employing a machine learning model to provide accurate recommendations using only a few, key soil nutrient levels.

## ✨ Key Features & Goals

* **Intelligent Crop Selection:** Build a multi-class classification model to predict the optimal crop (the target variable) given a set of soil metrics.
* **Nutrient Analysis:** Leverage essential soil features including **Nitrogen (N)**, **Phosphorous (P)**, **Potassium (K)**, and **pH** value.
* **Feature Importance Study:** Determine which of the four primary soil metrics (N, P, K, or pH) is the **single most predictive feature** for the crop recommendation, allowing farmers to prioritize the most impactful test.

## 🛠️ Methodology

The analysis and modeling were performed using a Jupyter Notebook (`notebook.ipynb`) and the following steps:

1.  **Data Loading and Exploration:** The `soil_measures.csv` dataset was loaded, which contains the four soil metrics and the corresponding ideal `crop`.
2.  **Model Selection:** A **Logistic Regression** classifier (chosen for its suitability in multi-class classification) was implemented.
3.  **Feature Performance Evaluation:** The model was trained and tested **separately** for each of the four individual features (N, P, K, and pH) to compare their predictive performance using the **F1-score (weighted)**.
4.  **Final Recommendation:** The feature yielding the highest F1-score was identified as the best single predictor for crop recommendation.

## 💡 Results Highlight

The analysis successfully identified the most powerful single predictor among the soil metrics:

> **Potassium (K)** was found to be the single best predictive feature for recommending the correct crop, achieving the highest F1-score out of the four tested metrics.

This finding allows the system to provide a reliable recommendation even when a farmer is constrained to measuring only one soil metric.

## 📁 Files in This Project

* `notebook.ipynb`: The main Jupyter Notebook containing all the data cleaning, exploratory analysis, model training, and the final feature performance comparison.
* `soil_measures.csv`: The dataset used for training the machine learning model.

## 💻 How to Run

1.  **Clone the repository:**
    ```bash
    git clone [Your Repository URL]
    ```
2.  **Install dependencies:**
    This project requires standard data science libraries. You can install them using pip:
    ```bash
    pip install pandas numpy scikit-learn
    ```
3.  **Run the notebook:**
    Open the `notebook.ipynb` file in your preferred environment (Jupyter Lab, VS Code, etc.) and run the cells sequentially to reproduce the analysis and results.
