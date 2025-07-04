# Smart Cabin Environment and Safety monitoring system 🚗🌡️💨

This project aims to develop a comprehensive holistic cabin environment monitoring and control system.Its Basically designed to optimize the temperature,humidity levels within a vehicle's interior,understanding the fan speed as well as monitoring the fatigueness of the driver all with the help of firebase which is being used to analyze real time data. 

---
## ⚙️ Features

- 🔥 Temperature and Humidity Monitoring (DHT11)
- ❤️ Heart Rate and SpO2 Detection (MAX30100)
- 👁️ Eye Blink Detection (IR Sensor)
- 🚨 Fatigue Alert System with Buzzer
- 🌀 Automated Fan Control based on Predicted Temperature
- 🔄 Real-Time Firebase Integration
- 📊 Web Dashboard for Live Monitoring
- 🤖 Machine Learning Model for Temperature Prediction

---
## 🧱 Hardware Setup

![Sensor Setup](./hardware/sensor_setup.jpg)
![Final Working Output](./hardware/final_output.jpg)

## 🖥️ Web Dashboard

![Live Dashboard View](./screenshots/dashboard_live.png)

---
## 🧰 Tech Stack

**Hardware**: ESP32, DHT11, MAX30100, IR Sensor, Fan, Buzzer, Eye Blink Sensor<br>
**Languages**: Python, C++, HTML, CSS, JavaScript<br>
**Backend**: Flask<br>
**Database**: Firebase Realtime Database<br>
**ML Model**: Linear Regression (for temperature prediction)<br>
**Web Hosting**: Localhost

---
## 🚀 Setup Instructions

**1. Clone the Repository**<br>
git clone https://github.com/yourusername/holistic-cabin.git<br>
cd holistic-cabin<br>

**2. Hardware Setup**<br>
Connect DHT11 to ESP32 GPIOx<br>
MAX30100 for HR/SpO2 to I2C pins<br>
IR sensor to GPIOy<br>
Fan/Buzzer to digital outputs<br>

**3.Configure Firebase**<br>
Use your own firebase_config.json file<br>

**4.Install Flask and Requirements**<br>
pip install -r requirements.txt<br>
python app.py<br>

**5.Run on ESP32**<br>
Flash esp_code.ino using Arduino IDE with correct pins<br>

---
## 📂 Folder Structure
SmartCabin/<br>
├── static/&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# CSS, JS files<br>
├── templates/&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# HTML files<br>
├── app.py&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Flask server<br>
├── esp_code.ino&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# ESP32 embedded code<br>
├── firebase_config.json&nbsp;# Firebase credentials<br>
├── model.pkl&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Trained ML model<br>
└── README.md<br>

---
## 🌐 Firebase Integration
All real-time sensor data is pushed to Firebase Realtime Database and fetched by the Flask server to display on the web dashboard and make predictions.

---
## 🔍 ML Prediction
**Model**: Linear Regression<br>
**Input** : Temp, Humidity, Previous Temp<br>
**Output**: Predicted Temp → used for Fan Speed Control<br>

---
⚠️ This repository previously contained Firebase API keys which have since been removed and revoked. Please use your own `firebase_credentials.json` file and do not commit secrets.
