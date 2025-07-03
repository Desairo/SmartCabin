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

**1. Clone the Repository**
git clone https://github.com/yourusername/holistic-cabin.git
cd holistic-cabin

**2. Hardware Setup**
Connect DHT11 to ESP32 GPIOx<br>
MAX30100 for HR/SpO2 to I2C pins<br>
IR sensor to GPIOy<br>
Fan/Buzzer to digital outputs<br>

**3.Configure Firebase**
Use your own firebase_config.json file

**4.Install Flask and Requirements**
pip install -r requirements.txt
python app.py

**5.Run on ESP32**
Flash esp_code.ino using Arduino IDE with correct pins

---
## 📂 Folder Structure
SmartCabin/
├── static/              # CSS, JS files
├── templates/           # HTML files
├── app.py               # Flask server
├── esp_code.ino         # ESP32 embedded code
├── firebase_config.json # Firebase credentials
├── model.pkl            # Trained ML model
└── README.md
