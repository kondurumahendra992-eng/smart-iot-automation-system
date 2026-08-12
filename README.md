# Smart IoT Automation System – Smart Temperature Control

## 📌 Project Description

The **Smart IoT Automation System** is an Arduino-based automation project designed for **smart AC and server-room temperature control**. The system continuously monitors temperature using a **TMP36 temperature sensor**. When the temperature reaches the defined threshold, the Arduino automatically activates a cooling fan through a relay.

The system can also use an **LDR and PIR sensor** for automatic lighting control. Sensor readings and device status are displayed through the **Serial Monitor** for monitoring and debugging.

## 🎯 Objectives

* Monitor room temperature continuously.
* Automatically control a cooling fan.
* Activate a buzzer during high-temperature conditions.
* Automatically control lighting using LDR and PIR sensors.
* Display/log sensor readings for monitoring.
* Demonstrate real-world embedded-system automation.

## 🧰 Components

* Arduino UNO
* TMP36 Temperature Sensor
* LDR
* PIR Motion Sensor
* Relay Modules
* DC Motor/Fan
* Buzzer
* Lamp/LED
* Resistors
* Breadboard
* Jumper Wires

## ⚙️ Working Principle

```text
TMP36 Temperature Sensor
          ↓
      Arduino UNO
          ↓
   Temperature > 30°C?
       ↙       ↘
     YES        NO
      ↓          ↓
   Fan ON     Fan OFF
   Buzzer ON  Buzzer OFF
```

For lighting:

```text
LDR + PIR
   ↓
Arduino UNO
   ↓
Dark + Motion?
  ↙       ↘
YES       NO
 ↓         ↓
Light ON  Light OFF
```

## 🔌 Pin Configuration

| Component   | Arduino Pin |
| ----------- | ----------- |
| LDR         | A0          |
| TMP36       | A1          |
| PIR         | D8          |
| Fan Relay   | D7          |
| Light Relay | D6          |

## 🌡️ Temperature Threshold

* **≥ 30°C:** Fan ON
* **≤ 28°C:** Fan OFF
* The 2°C difference prevents rapid relay switching.

## 🖥️ Monitoring

The Serial Monitor displays:

```text
Temperature: 31.2 C | LDR: 320 | Motion: YES | Fan: ON | Light: ON
```

## 🚀 Future Enhancements

* Add **ESP32 Wi-Fi connectivity**.
* Send temperature data to a cloud dashboard.
* Add mobile-app monitoring.
* Add automatic AC control.
* Store historical temperature data.
* Add alerts through IoT/cloud services.

## ✅ Advantages

* Automatic operation
* Low-cost implementation
* Energy-efficient lighting control
* Real-time monitoring
* Suitable for smart-home and server-room applications
* Easy to simulate in Tinkercad

## ⚠️ Limitations

* Basic Arduino version does not have Internet connectivity.
* TMP36 requires calibration for more accurate real-world measurements.
* LDR threshold depends on room lighting conditions.
* PIR can occasionally produce false detections.
* Real AC/mains loads require proper electrical isolation and protection.

## 🧪 Tinkercad Testing

1. Start the Tinkercad simulation.
2. Set temperature below **28°C** → Fan OFF.
3. Increase temperature to **30°C or above** → Fan ON.
4. Make the LDR area dark.
5. Trigger the PIR sensor → Light ON.
6. Open Serial Monitor at **9600 baud**.
7. Observe temperature, light, motion, fan, and light status.

## 👨‍💻 Project Type

**Embedded Systems / IoT / Smart Automation**

## 🏠 Real-World Applications

* Smart AC systems
* Server rooms
* Computer rooms
* Smart homes
* Industrial equipment cooling
* Electronics protection systems
* Automated office lighting
