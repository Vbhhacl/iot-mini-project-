# iot-mini-project-
temperature based fan speed controller
# Temperature-Based Fan Speed Controller Using Arduino UNO

A beginner-friendly Arduino project that adjusts the speed of a DC fan based on temperature readings from an LM35 sensor. Ideal for cooling or thermal management applications.

🧩 Features

- Reads ambient temperature via LM35 sensor.
- Controls a DC fan using PWM via a TIP122 transistor.
- Displays temperature on the Serial Monitor.
- Adjustable threshold and speed control in code.
- Automatic fan speed adjustment based on temperature.

 🛠️ Hardware Components

| Component         | Quantity |
|------------------|:--------:|
| Arduino UNO      | 1        |
| LM35 Temperature Sensor | 1 |
| DC Fan (5V)      | 1        |
| TIP122 Transistor (or equivalent) | 1 |
| Diode (e.g., 1N4007) | 1     |
| Resistor (4.7 kΩ) | 1       |
| Breadboard & Jumper Wires | As needed |

🔌 Circuit Diagram

1. LM35 Sensor 
   - VCC → 5 V  
   - GND → GND  
   - Output → Arduino Analog Pin A0  

2. Fan Control via TIP122
   - Fan negative → Collector  
   - Emitter → GND  
   - Fan positive → 5 V  
   - Base → Arduino PWM pin (e.g., D9) through 4.7 kΩ resistor  
   - Diode across fan (cathode to 5 V, anode to collector)

3. Common GND: Connect Arduino GND, fan GND, and TIP122 emitter.

🛠️ How It Works :
1.Reads analog voltage from LM35 every second.
2.Converts voltage to temperature (°C).
3.Sets PWM fan speed based on temperature range:
 < 25 °C → Off
 25–30 °C → Low
 30–35 °C → Medium
 35 °C → Full speed
4.Outputs readings and speed via Serial Monitor.
