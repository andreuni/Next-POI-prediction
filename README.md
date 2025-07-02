# Next POI Recommendation: GNNs for Spatiotemporal Analysis

This project addresses the **Next Point-of-Interest (Next-POI) Recommendation Task**, leveraging Graph Neural Networks (GNNs) for spatiotemporal analysis. The goal is to improve the accuracy of predicting the next location a user is likely to visit, based on their historical data.

---

## Problem Statement
- **Challenge**: Predicting the next POI is complex due to the intricate and unpredictable nature of human behavior.
- **Objective**: Enhance the accuracy of recommendations by analyzing spatiotemporal and similarity patterns.

---

## Dataset
Dataset used: 'TSMC2014 dataset', New-York check-ins

## Model Architecture

The proposed model consists of three main pipelines:

### 1. Spatial Pipeline
- **Purpose**: Analyze how geographical locations influence user movements.
- **Model**: Graph Neural Networks (GCN, GAT).
- **Input**: Spatial graphs representing all the POIs visited by a user.

### 2. Temporal Pipeline
- **Purpose**: Capture time-sensitive patterns and dependencies between transitions.
- **Model**: LSTM (Long Short-Term Memory).
- **Input**: Temporal graphs based on POI transitions over time slots.

### 3. Similarity Pipeline
- **Purpose**: Cluster users based on historical behavior and recommend POIs based on similar user patterns.
- **Methods**:
  - **Cosine Similarity**: To measure user behavior similarities.
  - **K-Means Clustering**: For dimensionality reduction and user segmentation.

- **Fully Connected Layer**: For final predictions.

---

## Loss Function
- A custom loss function combining:
  - **Binary Cross Entropy (BCE)**: To handle binary classification tasks.
  - **Cross Entropy (CE)**: For categorical tasks.
- Final loss: **α BCE + β CE**, with tuned weights for balanced optimization.

---

## Results
- The model successfully combines spatial, temporal, and similarity pipelines to improve prediction accuracy for the next POI task.
- Comparative analysis demonstrated significant improvements over baseline models.


