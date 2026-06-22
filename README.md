Here is my Notion Link -<h3>https://www.notion.so/PirMotion-Dictator-With-Relay-fb3ff43e20d04d178b8fccf8748b804d?pvs=4https://dour-talk-7b0.notion.site/PirMotion-Dictator-With-Relay-fb3ff43e20d04d178b8fccf8748b804d?pvs=4 </h3>
# Motion-Activated Relay Controller

## Overview

This project uses an Arduino, PIR motion sensor, and relay module to automatically control a light or other electrical device based on motion detection.

When motion is detected, the PIR sensor sends a signal to the Arduino. The Arduino then activates the relay, which turns on the connected load (such as a light bulb). If no motion is detected for a specified period, the relay turns off automatically.

This project is useful for home automation, security systems, energy-saving lighting, and occupancy-based control systems.

---

## Features

- Motion detection using a PIR sensor
- Automatic light activation
- Automatic shutoff after inactivity
- Relay control for high-voltage devices
- Serial monitor status updates
- Low-cost and easy-to-build design

---

## Components Used

- Arduino Uno / Nano
- PIR Motion Sensor (HC-SR501)
- Relay Module
- Light Bulb or Electrical Load
- 220V AC Adapter / Power Source
- Jumper Wires
- Breadboard

---

## System Workflow

1. PIR sensor monitors the surrounding area.
2. Motion is detected.
3. Arduino receives the motion signal.
4. Arduino activates the relay.
5. Relay powers the connected light.
6. If no motion is detected for 9 seconds, the relay turns off.
7. Arduino returns to monitoring mode.

---

## Hardware Description

### PIR Motion Sensor

The PIR (Passive Infrared) sensor detects infrared radiation emitted by people and objects.

- Detects movement within its range
- Low power consumption
- Commonly used in security and automation systems

### Relay Module

The relay acts as an electronic switch.

- Allows a low-voltage Arduino signal to control high-voltage devices
- Provides electrical isolation between the control circuit and load
- Can control lights, fans, alarms, and other appliances

### Arduino

The Arduino acts as the system controller.

Responsibilities:

- Reads PIR sensor input
- Controls relay output
- Tracks motion state
- Manages timing logic
- Sends status messages to the Serial Monitor

---

## Wiring Connections

| Component | Arduino Pin |
|-----------|------------|
| PIR OUT | D11 |
| Relay IN | D12 |
| PIR VCC | 5V |
| PIR GND | GND |
| Relay VCC | 5V |
| Relay GND | GND |

---

## Arduino Code Behavior

The program continuously reads the PIR sensor.

### Motion Detected

- Relay turns ON
- Connected light turns ON
- "Motion Detected" message appears in Serial Monitor

### No Motion Detected

- Waits 9 seconds
- Relay turns OFF
- Light turns OFF
- Status message is displayed

---

## Example Serial Output

```text
Motion Detected

Motion not detected for 9 sec
Turn off LED
```

---

## Applications

- Automatic room lighting
- Security systems
- Garage lighting
- Hallway lighting
- Energy-saving automation
- Smart home projects

---

## Future Improvements

- Adjustable delay time
- LDR sensor for day/night operation
- ESP32 Wi-Fi monitoring
- Mobile app integration
- MQTT/Home Assistant support
- Battery-powered version

---

## License

This project is provided for educational and learning purposes.
