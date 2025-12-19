🚀 Predictive Maintenance of Machines using IoT & Deep Learning
📌 Overview
This project implements a predictive maintenance system that continuously monitors machine parameters using IoT sensors and predicts potential failures through a Deep Learning LSTM model.
Real-time sensor data from a water pump is collected using NodeMCU and transmitted to AWS IoT Core. The model analyzes sensor readings to detect anomalies, enabling maintenance teams to take corrective actions before failures occur.
🧩 Problem Statement
Traditional machine maintenance results in:
Unexpected breakdowns
Increased downtime
High repair & maintenance cost
Reactive and scheduled maintenance strategies either respond too late or occur too frequently.
The goal is to accurately predict machine failure in advance using real-time sensor data to optimize maintenance and increase system reliability.
🎯 Project Objectives
Develop a real-time IoT-based predictive maintenance system
Monitor vibration, temperature, and current continuously
Use an LSTM model to detect anomalies and classify machine condition
Reduce unplanned downtime and avoid sudden failures
🔧 Hardware Components
Component	Description
ESP8266 NodeMCU	Main control unit + MQTT communication
DHT11	Measures motor temperature
MPU6050	Detects vibration and movement
ACS712 Current Sensor	Measures current drawn by motor
Relay Module	Controls the water pump motor
☁️ System Workflow
Sensor data collected by NodeMCU
Data transmitted to AWS IoT Core using MQTT protocol
Cloud processes and stores sensor data
LSTM model predicts machine health in real time
Results displayed on Blynk dashboard and web UI
🧹 Data Preprocessing Steps
Removed invalid characters using regex
Converted values to numerical format
Standardized timestamps
Extracted features:
vibration magnitude
temperature
current
hour and day
Feature scaling:
MinMax Scaling for vibration
StandardScaler for other values
Time-series windowing: sequence length = 10
K-Means clustering for label creation
🤖 LSTM Deep Learning Model
Architecture
LSTM Layer – 64 units (ReLU)
Dropout – 30%
LSTM Layer – 64 units (ReLU)
Dropout – 20%
Dense – 32 neurons (ReLU)
Output – 3 neurons Softmax
Training Details
80/20 training & testing split
50 epochs, batch size 64
Adam optimizer
Validation split: 20%
Early stopping
ReduceLROnPlateau
🔍 Prediction & Monitoring
Real-time data fed into model
Anomaly/failure probability calculated
Motor status displayed via dashboard
Enables early maintenance scheduling
📊 Results
Successful anomaly prediction from real-time IoT data
Improved fault detection accuracy
Reduced unexpected machine downtime
Demonstrated feasibility of IoT + DL predictive maintenance
📌 Conclusion
The project demonstrates how IoT and Deep Learning can be integrated to build a real-time predictive maintenance solution.
Benefits:
Prevents motor failure
Reduces maintenance cost
Improves machine lifespan
Supports intelligent Industry 4.0 maintenance strategy
