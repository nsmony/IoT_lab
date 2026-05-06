**Course:** ICT 360
**University:** American University of Phnom Penh  
**Group:** Group 4
**Instructor:** Professor Seng Theara


## I. Project Overview

AgriSafe Rot Spotter is an IoT-based system designed to detect post-harvest spoilage at an early stage using a multi-modal approach. The system integrates environmental sensors and computer vision to monitor the condition of stored agricultural products such as fruits and vegetables.

The system uses Edge AI (local processing) to analyze both sensor data and images in real time. By combining temperature, humidity, and visual features such as color and texture, the system can identify early signs of spoilage before they become severe.

This allows users to take action early, reducing food waste, saving costs, and improving overall food quality.


## II. Problem Statement

Post-harvest spoilage is a major issue in agriculture:

- Large amounts of food are wasted due to late detection
- Manual inspection is slow and inaccurate
- Environmental conditions are not continuously monitored
- Lack of automation leads to delayed response and financial loss

Spoilage commonly occurs during storage and transportation, causing significant waste and economic damage .


## III. Objectives

- Combine image and sensor data (multi-modal detection)
- Detect spoilage at an early stage
- Process data locally using Edge AI
- Reduce agricultural losses and improve efficiency


## IV. System Architecture

The system follows this structure:

**Input → Edge Processing → Output → Action**
### System Architecture Diagram
<img width="7059" height="4224" alt="ESP32 LCD HTTP Route Flow-2026-05-03-153937" src="https://github.com/user-attachments/assets/9adf51d7-b48e-44c9-97b7-9fa95b160078" />


This architecture is also illustrated in the system architecture diagram, showing the interaction between hardware, control logic, and AI server layers .


### 1. Input

- ESP32-CAM captures images of fruits
- DHT11 sensor measures temperature and humidity
- IR sensor detects object presence


### 2. Processing

- ESP32 processes sensor and image data
- AI model analyzes color, texture, and environmental conditions
- Web server enables remote monitoring


### 3. Output

- LCD displays system status
- Web dashboard shows real-time data
- Alerts notify users when spoilage is detected


### 4. Action

- Servo/DC motor controls sorting gate
- Gate closes if spoilage detected
- Gate remains open if fruits are healthy


## V. Key Features

- Multi-modal detection (image + sensor data)
- Real-time monitoring system
- Internet-enabled web dashboard
- Edge computing (low latency)
- Automatic gate control
- Early warning system
- Low-cost and scalable design


## VI. Methodology

### 1. System Design

The system integrates ESP32, sensors, camera, motors, and network connectivity into a unified workflow.


### 2. Data Processing

Sensor and image data are processed locally using Edge AI or rule-based logic for fast response.


### 3. Spoilage Detection

Spoilage is detected based on:

- Color changes
- Texture abnormalities
- Environmental conditions (temperature and humidity)


### 4. Automated Response

- Gate closes when spoilage is detected
- Prevents spoiled fruits from continuing


### 5. Alert System

- LCD displays warnings
- Web dashboard shows live status
- Alerts notify users immediately


### 6. Testing and Evaluation

System is tested under different conditions to measure:

- Accuracy
- Response time
- System reliability


## VII. Components

- ESP32
- DroidCam
- DHT11 Sensor
- I2C LCD Display
- IR Sensor
- Servo Motor
- 2 DC Motors
- Motor Driver
- Power Supply

<img width="2030" height="916" alt="Hardware" src="https://github.com/user-attachments/assets/a85eaa80-f679-43b0-b6b1-a58d44ce4ffe" />



## VIII. System Workflow

This workflow is consistent with the system flow diagram shown on Page 5 .

<img width="8192" height="919" alt="ESP32 LCD HTTP Route Flow-2026-05-03-154735" src="https://github.com/user-attachments/assets/7ca9c21d-e451-4d93-9729-5dfe397c1fbb" />


## IX. Model Training

The AI model is trained using **YOLO26l** with a custom dataset.

Dataset includes:

- Fresh grape
- Rotten grape
- Fresh strawberry
- Rotten strawberry

The dataset was manually collected and labeled to improve detection accuracy.


## X. Challenges and Solutions

### Challenges:

- ESP32-CAM has low image quality → reduced model accuracy
- Limited dataset
- Lack of experience in model training

### Solutions:

- Used **DroidCam** for higher-quality image input
- Recollected and expanded dataset
- Improved training process


## XI. Results

- Early detection of spoilage
- Improved accuracy using multi-modal data
- Reduced food loss during storage
- Faster response compared to manual inspection


## XII. Conclusion

AgriSafe Rot Spotter demonstrates how IoT and Edge AI can be combined to solve real-world agricultural problems. By integrating sensor data with image analysis, the system provides an efficient solution for early spoilage detection and automated response.

This project highlights the potential of smart agriculture systems in reducing waste, improving food quality, and increasing operational efficiency.


## XIII. Future Improvements

- Improve AI model accuracy with larger dataset
- Add cloud integration for data analytics
- Expand to more types of fruits and vegetables
- Enhance mobile app support for monitoring
