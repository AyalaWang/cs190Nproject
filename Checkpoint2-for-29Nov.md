# Checkpoint 2: Data Collection, Feature Selection, and Model Plan

**Group 7: Ayala Wang, Shashank Bhagwani, Shiyuan Wang, Nandhan Natarajan**

**Link to GitHub Repo**: [GitHub Repository](https://github.com/AyalaWang/cs190Nproject.git)

---

## 1. Update on Data Collection

- **Status**: 
  - We have successfully collected and labeled X packet traces using the NetUnicorn platform.
  - Each trace includes metrics such as download/upload speed, latency, jitter, and packet loss, along with metadata (location, time, environmental condition).

- **Challenges**: 
  - [Include any challenges encountered during data collection, such as issues with devices, task execution, or network anomalies].

- **Scaling Plan**:
  - We plan to [scale up / not scale up] the data collection process. 
  - If scaling up: Additional data collection will focus on [specific locations/times/conditions] to ensure comprehensive coverage.
  - If not scaling up: The current dataset is sufficient for model training and evaluation.

---

## 2. Planned Features

- **Extracted Metrics**:
  - **Download/upload speed**: Captures the data transfer rate.
  - **Latency**: Measures the delay between data request and response.
  - **Jitter**: Identifies variations in packet arrival times, critical for real-time applications.
  - **Packet loss**: Tracks the percentage of lost data packets during transmission.
  - Additional derived features (if applicable):
    - Packet size distribution
    - Inter-packet arrival times
    - Time of day (peak/off-peak).

- **Justification**:
  - These features directly impact network performance analysis and are essential for identifying bottlenecks and patterns in the campus Wi-Fi network.
  - Including metadata such as location and environmental conditions enhances the dataset’s contextual relevance.

---

## 3. Model Plan

- **Model Type**: 
  - [Insert chosen model type, e.g., Random Forest, Linear Regression, K-Means Clustering, etc.].
  - We aim to use [model type] to [e.g., predict continuous metrics, classify network performance, or cluster traces by characteristics].

- **High-Level Explanation**:
  - [Explain why this model is suitable. For example: "Random Forest is chosen for its ability to handle complex feature relationships and provide feature importance metrics."].

- **Scikit-learn Implementation**:
  - Link to the Scikit-learn documentation for the chosen model:
    - [Random Forest](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
    - [Linear Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
    - [K-Means Clustering](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)

---

## 4. Next Steps

- Continue refining the data collection process if necessary.
- Implement feature extraction and preprocessing pipelines.
- Begin initial model training and evaluation using the collected data.
- Adjust the approach based on insights gained from preliminary results.

---