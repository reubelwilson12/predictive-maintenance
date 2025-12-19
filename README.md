# ⚙️ Predictive Maintenance of Machines using IoT & Deep Learning 🚀

## 📝 Overview

This project implements an IoT-based predictive maintenance system using real-time sensor data and an LSTM Deep Learning model.

Sensors monitor temperature, vibration, and current from a water pump.  
The data is transmitted to AWS IoT Core using MQTT and analyzed for early failure prediction.

---

## ❗ Problem Statement

Machines fail unexpectedly in industrial environments, causing:

- ⚠️ Sudden breakdowns  
- ⏳ Downtime and delay  
- 💸 High maintenance cost  

Reactive or scheduled maintenance is inefficient.  
A data-driven predictive approach is required to detect degradation early.

---

## 🎯 Objectives

- 📡 Collect real-time machine sensor data  
- 🤖 Predict anomalies using LSTM model  
- 🔐 Transmit data securely using MQTT  
- 🛠 Reduce unplanned downtime and breakdowns  
- 📈 Improve operational efficiency  

---

## 🔧 Hardware Components

- 🧠 ESP8266 NodeMCU microcontroller  
- 🌡 DHT11 – temperature sensor  
- 📳 MPU6050 – accelerometer + gyroscope  
- ⚡ ACS712 – current sensor  
- 🔌 Relay module – motor control  

---

## 🔄 System Workflow

1️⃣ Sensors measure vibration, temperature, and current  
2️⃣ NodeMCU sends data to AWS IoT Core via MQTT  
3️⃣ Data preprocessing performed in cloud/local environment  
4️⃣ LSTM model predicts machine health status  
5️⃣ Dashboard/UI displays predictions in real time  
6️⃣ Alerts raised for abnormal operation  

---

## 🧹 Data Preprocessing Steps

- 🧽 Removal of invalid characters  
- 🔢 Conversion to numerical format  
- 🕒 Standard timestamp formatting  
- 🔍 Feature extraction: vibration, hour, day  
- 📊 Feature scaling:  
  - MinMax for vibration  
  - StandardScaler for temperature/current/time  
- 📈 Time-series windowing (sequence length = 10)  
- 🔎 K-Means clustering to label data into 3 health states  

---

## 🤖 LSTM Model Architecture

- 🔸 LSTM (64 units, ReLU activation)  
- 🔸 Dropout (30%)  
- 🔸 LSTM (64 units, ReLU activation)  
- 🔸 Dropout (20%)  
- 🔸 Dense layer (32 neurons, ReLU)  
- 🔸 Softmax output for 3-class classification  

### 🏋 Training Details

- 🧩 Train-test split: 80/20  
- 🔁 Epochs: 50  
- 📦 Batch size: 64  
- ⚙ Optimizer: Adam  
- ⛔ EarlyStopping + ReduceLROnPlateau callbacks  

---

## 📡 Prediction & Monitoring

- Real-time sensor data streamed to cloud  
- ML model predicts machine health state  
- Dashboard/web UI shows machine condition  
- ⚠ Alerts triggered before actual failure  

---

## 📊 Results

- ✔ Accurate anomaly detection  
- ✔ Reduced unexpected downtime  
- ✔ Preventive maintenance achieved  
- ✔ Demonstrated IoT + AI feasibility  

---

## 🏁 Conclusion

This project successfully integrates IoT sensing and LSTM deep learning for predictive maintenance.

It enables:

- ⚙ Preventive servicing  
- 💰 Reduced maintenance cost  
- ⏳ Increased machine lifespan  
- 🏭 Support for Industry 4.0 intelligent automation  



(Add references here)

