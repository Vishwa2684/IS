# Data Preparation
- Overview<br>
        To prepare the data for analysis, the following steps were taken

        -    The prep.py script was executed to process the raw data. However, it was noted that the script could not generate 1 GB of data as requested. An alternative code that can produce 1 GB of data would be appreciated.
        - The prepared dataset was then inspected in the test.ipynb Jupyter notebook.
<br>
    - Data Inspection<br>
        Upon examination of the dataset, it was observed that the DataFrame created by the code has 3 features that are completely filled, but two features (CPU temperature and CPU power) have a significant amount of missing values.<br>
    - Handling Missing Values<br>
        The missing values in the CPU temperature and CPU power features could not be imputed using the SimpleImputer from scikit-learn. As a result, those two features were dropped, and anomaly detection was performed on the remaining features.<br>

# Anomaly Detection
Several approaches were explored for anomaly detection:

- Unsupervised Learning:

    - Nearest Neighbors
    - Isolation Forest
    - Local Outlier Factor


- Supervised Learning:

    - Simple RNN architecture with 64 hidden units, input size, and output size of 1



- The rationale for using the RNN approach was that it could be well-suited for modeling the sequential nature of the data.
- The results showed that the Simple RNN method produced better outputs compared to the Nearest Neighbors, LOF, and Isolation Forest techniques.
- For the RNN approach, the 95th percentile of the reconstruction error was used as the threshold for identifying anomalies, as a lower threshold would risk classifying normal points as anomalies.
- Overall, the data preparation and anomaly detection processes were carried out, and the findings, including the limitations and proposed solutions, have been summarized in this README.
- Please let me know if you require any clarification or have additional requests.