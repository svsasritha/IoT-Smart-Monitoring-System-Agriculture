# IoT Smart Monitoring System for Agriculture

This repository contains my solution for the “Smart Monitoring System” problem statement given as part of the recruitment process by Cerevyn Solutions. The objective of this solution is to design an IoT-based system that monitors soil conditions and generates alerts for irrigation.

---

## Problem Statement

Design an IoT-based monitoring solution for agriculture or aquaculture that monitors environmental parameters and triggers alerts based on threshold conditions.

For this solution, I have focused on an agriculture use case where soil moisture and temperature are monitored to assist in irrigation decisions.

---

## System Overview

The proposed system uses sensors to collect soil and environmental data. A microcontroller (ESP32) acts as the gateway and sends data to a cloud platform. The cloud dashboard visualizes the data and generates alerts when the values cross predefined limits.

---

## Sensor Selection and Justification

- **Soil Moisture Sensor**  
  Used to measure the water content in soil. This helps in deciding when irrigation is required.

- **DHT11 / DHT22 Sensor**  
  Measures temperature and humidity. Temperature affects crop growth and evaporation rate.

- **DS18B20 Temperature Sensor (Optional)**  
  Measures soil temperature near plant roots, which is important for crop health.

---

## Data Flow Explanation

1. Sensors collect real-time soil and environmental data.  
2. The ESP32 microcontroller reads sensor values and performs basic processing.  
3. Data is transmitted to a cloud platform (such as ThingSpeak or Firebase) using Wi-Fi.  
4. The cloud platform stores and visualizes the data on a dashboard.  
5. Alert logic is applied to notify the user when irrigation is required.

---

## Alert Logic (Edge–Cloud Logic)

- If soil moisture is less than 30%, an irrigation alert is triggered.  
- If temperature exceeds 40°C, a warning alert is generated.  

Alerts can be sent via SMS, email, or mobile notification in a real-world implementation.

---

## Sample JSON Output

```json
{
  "soil_moisture": 28,
  "temperature": 36.5,
  "humidity": 72,
  "timestamp": "2026-02-07 10:30:00"
}
```

---

## System Architecture

The system architecture consists of sensor nodes deployed in the agricultural field, an ESP32 microcontroller acting as the gateway, and a cloud platform for data storage and visualization. The system performs data acquisition from sensors, edge-level processing, cloud communication, and alert generation.  
The detailed block diagram and system flow diagram are included in the attached PDF document.

---

## Future Enhancements

- Automated irrigation using relay-controlled water pumps  
- Mobile application for farmers to receive real-time alerts  
- AI-based irrigation prediction using historical sensor data  
- Solar-powered sensor nodes for remote agricultural fields  
- Integration with weather forecast APIs for intelligent irrigation decisions  

---

## Files in This Repository

- **IoT_Smart_Monitoring_System_Final_Submission.pdf** – Detailed solution document containing system architecture, block diagram, data flow, and explanation.

---

## Author

Vyshnavi Sri Asritha Sighakolli
B.Tech Electrical and Electronics Engineering  
Interested in IoT, Embedded Systems, and Smart Agriculture
