## **Short Questions**

### 1. **Define IoT and mention its key components.**

**Internet of Things (IoT)** is a network of interconnected physical devices embedded with sensors, software, and communication technologies that collect and exchange data over the internet. It enables automation, remote monitoring, and real-time decision-making.

#### **Key Components of IoT**

1. **Sensors & Actuators** – Sensors collect data from the environment (e.g., temperature, humidity), while actuators perform actions (e.g., turning on a fan).
2. **Connectivity** – IoT devices use wireless or wired communication (Wi-Fi, Bluetooth, Zigbee, 4G/5G, LoRa) to send and receive data.
3. **Edge Processing** – Some devices have built-in microcontrollers (Arduino, ESP32) that process data locally.
4. **Cloud Computing** – Data is stored and analyzed in cloud platforms like AWS IoT, Google Cloud IoT.
5. **User Interface** – Applications (web, mobile) allow users to monitor and control IoT devices.

---

### 2. **Differentiate between digital and analog sensors.**

| **Feature**        | **Digital Sensor**          | **Analog Sensor**                         |
| ------------------ | --------------------------- | ----------------------------------------- |
| **Output Type**    | Discrete (Binary: 0 or 1)   | Continuous (Voltage or Resistance change) |
| **Data Precision** | High (Exact values)         | Less precise (Needs ADC conversion)       |
| **Interference**   | Less prone to noise         | More sensitive to noise                   |
| **Example**        | PIR Sensor, IR Sensor, RFID | Temperature Sensor, LDR, Microphone       |

**Example:**

* A **PIR sensor** (digital) detects motion and outputs HIGH/LOW.
* A **LDR (Light Dependent Resistor)** (analog) gives varying voltage depending on light intensity.

---

### 3. **List five real-life applications of IoT.**

1. **Smart Homes** – IoT-based smart thermostats (Nest), voice assistants (Alexa, Google Home) automate home environments.
2. **Wearable Health Devices** – Smartwatches track heart rate, steps, and oxygen levels.
3. **Smart Agriculture** – IoT soil moisture sensors help farmers optimize irrigation.
4. **Industrial IoT (IIoT)** – Sensors monitor factory equipment for predictive maintenance.
5. **Smart Traffic Management** – IoT-enabled traffic lights adjust signals based on vehicle flow.

---

### 4. **How do sensors and actuators communicate in an IoT system?**

1. **Sensors collect environmental data** (e.g., a temperature sensor detects heat).
2. The sensor sends this data to a **microcontroller (ESP32, Raspberry Pi)** via **analog/digital interfaces** (I2C, SPI, UART).
3. The microcontroller processes this data and **sends commands** to an actuator.
4. The actuator performs an action (e.g., turning on a motor, buzzer, or light).

Example:

* A **temperature sensor** detects heat. If the temperature exceeds 30°C, a **fan (actuator)** is turned ON.

---

### 5. **What is the significance of Wireless Sensor Networks (WSN) in IoT?**

A **Wireless Sensor Network (WSN)** is a network of sensor nodes that communicate wirelessly to collect and transmit data.

#### **Importance in IoT:**

* **Real-time Monitoring:** Sensors collect data continuously for automation.
* **Remote Access:** IoT devices can be controlled remotely via mobile apps.
* **Energy Efficiency:** WSN devices use low-power communication like Zigbee or LoRa to optimize battery life.
* **Scalability:** Multiple sensor nodes can be deployed over large areas (e.g., smart cities, industrial monitoring).

Example: In **smart agriculture**, WSN-based soil moisture sensors send data to cloud platforms, allowing farmers to monitor crops remotely.

---

### 6. **Write a simple Arduino IDE code to blink an LED.**

```cpp
void setup() {
  pinMode(13, OUTPUT);  // Set pin 13 as an output
}

void loop() {
  digitalWrite(13, HIGH);  // Turn LED ON
  delay(1000);             // Wait for 1 second
  digitalWrite(13, LOW);   // Turn LED OFF
  delay(1000);             // Wait for 1 second
}
```

---

## **Long Questions**

### 1. **Explain the definition, conceptual framework, and architectural view of IoT.**

#### **Definition of IoT**

IoT refers to a system of internet-connected devices that communicate and exchange data without human intervention.

#### **Conceptual Framework of IoT**

IoT systems work on **sensing, networking, data processing, and applications.**

* **Perception Layer**: Sensors collect data.
* **Network Layer**: Data is transmitted via the internet or wireless networks.
* **Processing Layer**: Edge devices (ESP32, Raspberry Pi) or cloud servers analyze data.
* **Application Layer**: Users interact via mobile/web apps.

#### **Architectural View of IoT**

| **Layer**             | **Function**                                                    |
| --------------------- | --------------------------------------------------------------- |
| **Perception Layer**  | Sensors & actuators collect data                                |
| **Network Layer**     | Transfers data using Wi-Fi, Bluetooth, LoRa                     |
| **Edge Layer**        | Local data processing on microcontrollers (ESP32, Raspberry Pi) |
| **Cloud Layer**       | Data storage and analysis using AWS, Google Cloud               |
| **Application Layer** | Mobile apps, dashboards for user interaction                    |

---

### 2. **What is Machine-to-Machine (M2M) communication? Explain its role in IoT with examples.**

#### **Definition:**

Machine-to-Machine (M2M) communication refers to **direct data exchange between devices** without human intervention.

#### **Role in IoT:**

* Automates processes by allowing smart devices to **communicate and make decisions**.
* Reduces human effort and **enhances efficiency** in industrial applications.
* Enables **real-time monitoring** and predictive maintenance.

#### **Examples of M2M in IoT:**

1. **Smart Meters**: Electricity meters send real-time usage data to utility providers for automatic billing.
2. **Healthcare Monitoring**: Smartwatches send heart rate data to hospitals.
3. **Industrial IoT (IIoT)**: Machines detect malfunctions and notify engineers.

---

### 3. **Describe the various technologies behind IoT and their significance.**

| **Technology**             | **Role in IoT**                                       |
| -------------------------- | ----------------------------------------------------- |
| **Wireless Communication** | Wi-Fi, Zigbee, LoRa, 5G enable device connectivity    |
| **Cloud Computing**        | AWS, Google Cloud store and process IoT data          |
| **Big Data & AI**          | AI algorithms analyze sensor data for decision-making |
| **Embedded Systems**       | ESP32, Arduino, Raspberry Pi process data locally     |

---

### 4. **Compare different types of IoT development boards.**

| **Feature**      | **Arduino**        | **Raspberry Pi**            | **ESP8266**   |
| ---------------- | ------------------ | --------------------------- | ------------- |
| **Processor**    | 8-bit AVR          | 64-bit ARM                  | 32-bit Xtensa |
| **Connectivity** | Limited            | Ethernet, Wi-Fi             | Wi-Fi         |
| **Use Case**     | Basic IoT projects | Advanced AI/ML applications | Wireless IoT  |

---

### 5. **Discuss RFID technology in IoT. How does it enhance IoT applications?**

RFID (Radio Frequency Identification) uses radio waves to track and identify objects using RFID tags and readers.

#### **How RFID Enhances IoT:**

* Enables **real-time tracking** in supply chains.
* Used in **smart inventory management** for automation.
* Enhances **security systems** via access control (RFID-based door locks).

---

### 6. **Explain the different types of sensors and actuators used in IoT systems.**

**Sensors (Data Collection):**

* **Temperature Sensor** (DHT11) – Monitors heat levels.
* **Motion Sensor** (PIR) – Detects movement.
* **Gas Sensor** (MQ-135) – Detects harmful gases.

**Actuators (Action Execution):**

* **Servo Motor** – Controls robotic arms.
* **Relay** – Turns appliances ON/OFF.
