# ChurnShield — Customer Churn Prediction Dashboard

A production-grade ML dashboard and live predictor for telecom customer churn, built on TanStack Start and deployed to Netlify.

## Project Overview

ChurnShield visualises the performance of a machine-learning model that predicts whether a telecom customer will churn. The model was trained on 7,000+ records, uses SMOTE oversampling to correct class imbalance, and achieves **88.2% accuracy** with an **AUC-ROC of 0.91**. The original Flask REST API is deployed on Render.

## Key Features

- **Model metrics dashboard** — accuracy, recall, AUC-ROC, and training-set size at a glance
- **ROC curve** — interactive chart showing the classifier's discrimination power
- **Recall improvement chart** — pre- vs post-SMOTE recall (61% → 83%)
- **Feature importance** — horizontal bar chart showing the most predictive customer attributes
- **Class distribution** — doughnut chart illustrating the original 73/27 class split
- **Performance radar** — multi-metric comparison before and after SMOTE balancing
- **Live churn predictor** — form-based simulation of the REST API, returning risk level and probability score
- **API reference** — copyable cURL examples mirroring the Flask endpoint contract

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | TanStack Start (React 19) |
| Styling | Tailwind CSS v4 |
| Charts | Chart.js + react-chartjs-2 |
| Hosting | Netlify |
| ML Backend | scikit-learn, imbalanced-learn, Flask (Render) |

## Running Locally

```bash
npm install
npm run dev
```

The dev server starts on <http://localhost:3000>.

> **Note:** The "Live Churn Predictor" on the dashboard runs a client-side logistic regression simulation matching the deployed model's decision boundary — no backend call required for the demo.
