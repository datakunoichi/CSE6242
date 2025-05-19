# ✈️ US Flight Delay Prediction Interface Using Machine Learning

This project develops a machine learning-powered interface to predict US flight delays, improving decision-making for both airline operators and travelers. The model is based on historical flight data and network metrics, and is deployed via a browser extension and a web application for user-friendly access.

---

## 📌 Project Overview

Flight delays disrupt millions of passengers annually, leading to financial losses and poor customer experiences. This project aims to **predict flight delays** using historical data from 2019–2023 and provide an **interactive prediction interface**. By combining machine learning and network analysis, the tool helps optimize scheduling and improve flight planning.

---

## 🔍 Research Questions

Using supervised learning and network-based modeling, this project answers the following:

1. Can we predict whether a flight will be delayed based on features such as airline, route, and time of day?
2. What features contribute most significantly to accurate delay prediction?
3. How can we deliver predictions through an accessible and user-friendly interface?

---

## 📊 Data Source

The dataset was sourced from [Kaggle: Flight Delay and Cancellation Dataset (2019–2023)](https://www.kaggle.com/datasets/patrickzel/flight-delay-and-cancellation-dataset-2019-2023), which includes:

- Flight date and times
- Airline and flight number
- Origin and destination airports
- Delay durations and status
- Network centrality metrics (degree, betweenness)
- Weather and operational data (indirectly)

---

## 🧠 Model & Methodology

The project evaluated several machine learning models including:

- Random Forest
- Logistic Regression
- Support Vector Machine (SVM)
- **Final Model: XGBoost Classifier**

**Key Features Used**:
- Airline, origin, destination
- Time of day, day of week, and month
- Previous departure delay
- Flight duration interactions
- Airport network centrality metrics

**Feature Engineering**:
- Interaction terms for route and airline-specific trends
- Time binning for departure and arrival
- Label encoding for categorical features

---

## 🖥️ Innovation: Delay Prediction Interfaces

### 🔌 Chrome Plug-In

A browser extension integrates directly with Google Flights pages to provide real-time delay predictions. It auto-detects flight information and presents delay likelihood without leaving the booking site.

### 🌐 Streamlit Web App

A user-friendly web interface allows:
- Dropdown selection of flight details
- Delay predictions for multiple thresholds (15/30/45/60 minutes)
- Interactive **Pydeck map visualization** of routes

---

## 🧪 Experiments & Evaluation

| Threshold | Accuracy   | Precision | Recall | F1-Score |
|----------:|-----------:|----------:|-------:|---------:|
| 15 min    | 72.23%     | 34.0%     | 42.0%  | 38.0%    |
| 30 min    | 80.37%     | 27.0%     | 32.0%  | 29.0%    |
| 45 min    | 85.68%     | 23.0%     | 24.0%  | 23.0%    |
| 60 min    | **88.47%** | 19.0%     | 21.0%  | 20.0%    |

**Model Comparison Highlights**:
- **XGBoost** outperformed others in recall and balanced performance
- Random Forest was robust but slower
- Logistic Regression and SVM underperformed with class imbalance

---

## 📈 Feature Importance

Top predictors identified:
- Month, day of week (temporal patterns)
- Origin/Destination airports
- Previous departure delay
- Airport network centrality (degree, betweenness)

These findings emphasize the need for both operational and network-based features.

---

## 🛠️ Scripts

All scripts are stored in the `scripts/` folder:

- `process_data.py` – Data preprocessing and cleaning
- `cluster_model.py` – Unused in final, but tested during exploratory phase
- `regression_model.py` – Regression models (initial experiments)
- `create_dash.py` – Builds the interactive web dashboard
- `run.sh` – Pipeline execution script

---

## 🧪 Installation

To run the project locally:

```bash
git clone https://github.com/your-username/flight-delay-predictor.git
cd flight-delay-predictor
pip install -r requirements.txt
```

---

## 🚀 Usage

1. Run the Chrome extension to get live predictions while browsing flight sites.
2. Launch the Streamlit web app for a standalone experience:
   ```bash
   streamlit run app.py
   ```

---

## 🌍 Live Demo

> 🔗 *Live Streamlit App:* *(link placeholder)*  
> 🔗 *Chrome Extension Demo:* *(link placeholder)*

---

## 📚 References

1. Patrick Zel. [Flight Delay and Cancellation Dataset (2019–2023)](https://www.kaggle.com/datasets/patrickzel/flight-delay-and-cancellation-dataset-2019-2023)
2. Etani, N. (2021). Predictive models for on-time arrivals using weather data.
3. Rajesh Kumar Jha & Babiceanu, R. (2022). Hybrid ML models for flight delay prediction.
4. Zoutendijk & Mitici (2022). Probabilistic delay models in operational scheduling.
*(Full list in project report)*

