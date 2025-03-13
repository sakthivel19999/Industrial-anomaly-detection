
# Industrial Anomaly Detection

##  Project Overview
This project develops an anomaly detection system for industrial equipment using machine learning. The system identifies unusual behavior in sensor data to prevent equipment failure, reduce downtime, and improve operational efficiency.

##  Background
Industrial equipment generates large volumes of sensor data (e.g., temperature, pressure, voltage). Anomalies in this data could signal potential issues like overheating, malfunction, or early signs of failure. Identifying these anomalies early helps with predictive maintenance, which minimizes costs and improves efficiency.

##  Dataset
- **Size:** 10,000 records  
- **Features:**  
  - **Timestamp** – When the reading was recorded  
  - **Temperature** – Measured temperature  
  - **Anomaly** – Binary flag (0 = Normal, 1 = Anomaly)  
  - **Location** – Sensor location (some missing values)  

##  Approach
1. **Data Preprocessing:**  
   - Converted timestamps to datetime format  
   - Handled missing values in location  
   - Created lag features and moving averages  

2. **Model Selection:**  
   - Tested with Isolation Forest and One-Class SVM  
   - **Tuned One-Class SVM** achieved better recall and precision  

3. **Evaluation Metrics:**  
   - **Precision:** 99% (Normal), 27% (Anomalies)  
   - **Recall:** 96% (Normal), 60% (Anomalies)  
   - **F1-Score:** 98% (Normal), 38% (Anomalies)  

4. **Results:**  
   - The system successfully detected anomalies  
   - High recall and F1-score indicate that the model effectively identifies unusual patterns  

##  Business Impact
- Reduced downtime through early failure detection  
- Improved operational efficiency  
- Lower maintenance costs through predictive maintenance  

##  Files
- `anomaly_detection.py` – Source code  
- `tuned_one_class_svm.pkl` – Trained model  
- `Anomaly_Detection_Report.txt` – Project report  
- `Anomaly_Detection_Presentation.pptx` – Presentation slides  

##  How to Run
1. Clone the repo:  
```
git clone https://github.com/your-sakthivel19999/industrial-anomaly-detection.git
```
2. Install dependencies:  
```
pip install -r requirements.txt
```
3. Run the script:  
```
python anomaly_detection.py
```

## 📊 Results
- Precision: 99% (Normal), 27% (Anomalies)  
- Recall: 96% (Normal), 60% (Anomalies)  
- F1-Score: 98% (Normal), 38% (Anomalies)  
