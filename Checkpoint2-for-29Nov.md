# Checkpoint 2: Data Collection, Feature Selection, and Model Plan

**Group 7: Ayala Wang, Shashank Bhagwani, Shiyuan Wang, Nandhan Natarajan**

**Link to GitHub Repo**: [GitHub Repository](https://github.com/AyalaWang/cs190Nproject.git)

---

## 1. Update on Data Collection

- **Status**: 
  - We have successfully collected and labeled **120 packet traces** using the NetUnicorn platform.
  - Each trace includes metrics such as:
    - **Download/upload speed**
    - **Latency**
    - **Jitter**
    - **Packet loss**
  - Metadata is included with each trace, capturing:
    - **Location**: Library, lecture halls, outdoor plazas.
    - **Time**: Peak and off-peak hours.
    - **Environmental condition**: Indoor and outdoor settings.

- **Challenges**: 
  - There were initial difficulties in setting up devices at some outdoor locations due to weak power sources and unstable Wi-Fi connectivity.
  - During peak hours, we observed occasional packet trace interruptions, which required rerunning the data collection tasks to ensure data consistency.

- **Scaling Plan**:
  - We plan to scale up the data collection to include **100 more traces**, focusing on less frequently sampled areas such as dormitories and remote corners of the campus.
  - Scaling will ensure broader coverage and a more representative dataset for model training.

---

## 2. Planned Features

- **Extracted Metrics**:
  - **Download/upload speed**: Captures the data transfer rate.
  - **Latency**: Measures the delay between data request and response.
  - **Jitter**: Identifies variations in packet arrival times, critical for real-time applications.
  - **Packet loss**: Tracks the percentage of lost data packets during transmission.
  - **Additional derived features**:
    - Packet size distribution.
    - Inter-packet arrival times.
    - Time of day (categorized as peak/off-peak).

- **Justification**:
  - These features provide a comprehensive view of network performance and help identify bottlenecks or patterns in UCSB’s Wi-Fi network.
  - Metadata such as location and environmental conditions enhance the dataset’s contextual relevance, allowing the model to capture nuanced impacts of different settings on network quality.

---

## 3. Model Plan

- **Model Type**: 
  - We plan to use a **Random Forest Classifier** to classify network performance into predefined categories (e.g., Good, Moderate, Poor).
  - This model was chosen for its robustness to noise, ability to handle nonlinear relationships between features, and built-in feature importance metrics.

- **High-Level Explanation**:
  - The Random Forest Classifier is well-suited for our dataset as it can effectively work with the mix of categorical (e.g., location) and continuous features (e.g., download speed, latency).
  - It will also provide insights into which features have the most significant impact on network performance, aiding UCSB IT services in targeting improvements.

- **Scikit-learn Implementation**:
  - [Random Forest Classifier Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)

---

## 4. Next Steps

- **Data Collection**:
  - Complete the planned scaling of data collection, focusing on underrepresented campus areas.
- **Feature Engineering**:
  - Extract the planned features from the collected packet traces.
  - Perform feature scaling and encoding as needed for model compatibility.
- **Model Training and Evaluation**:
  - Train the Random Forest Classifier on the labeled data.
  - Evaluate the model using cross-validation and metrics such as accuracy, F1-score, and confusion matrix.
- **Iterative Improvements**:
  - Adjust feature selection or model parameters based on preliminary results to improve performance.

---