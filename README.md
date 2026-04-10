# IoT-milk-preservation
## Overview
This project keeps milk fresh by monitoring, displaying, controlling, and giving warnings about temperature and humidity. A DHT22 sensor constantly monitors the conditions inside the milk storage area. An LCD screen displays the live readings, showing temperature in Celsius and humidity as a percentage.
I was in charge of the temperature settings. The best range for storing milk is between 2°C and 5°C. For controlling the environment, a relay turns the cooling system on when it gets too warm and off when it gets too cold. For warnings, if the temperature goes above 5°C, a red light and buzzer activate. Above 8°C, a flashing red light signals serious danger. Below 2°C, a blue light and buzzer warn against freezing damage. The system also monitors humidity and displays warnings for low, high, or dangerous levels. An RGB light changes color to give instant visual warnings without needing to read the screen.


## Features
- Reads temperature and humidity using DHT22
- Alternating LCD display (Temp → Humidity every 2 seconds)
- RGB LED indicators:
  - Blue → Too Cold (≤ 2°C)
  - Cyan → Safe (Temp 3–5°C + Humidity 80–90%)
  - Red → Too Hot (5–8°C)
  - Flashing Red → Critical Temp (>8°C)
  - Yellow → Low Humidity (<70%)
  - Purple → High Humidity (91–95%)
  - Flash Purple/Red → Critical Humidity (>95%)
- Relay and buzzer for alerts
- Wokwi simulation included

## How to Run on Wokwi
1. Go to [Wokwi Project Link](https://wokwi.com/projects/460483933398522881).
2. Copy the code from `main.ino` and paste it into the Wokwi editor.
3. Upload the `diagram.json` file to recreate the circuit.
4. Click **Start Simulation** to see live sensor readings and alerts.

## How to Run Locally (Arduino IDE)
1. Install the **Arduino IDE**.
2. Install required libraries:
   - `DHT sensor library`
   - `LiquidCrystal_I2C`
3. Connect your ESP32, DHT22, LCD, RGB LED, relay, and buzzer as per `diagram.json`.
4. Open `main.ino` in Arduino IDE.
5. Select **ESP32 Dev Module** as the board.
6. Upload the code to your ESP32.
7. Observe readings on the LCD and LED/buzzer alerts.

## Repository Contents
- `main.ino` → Arduino sketch with logic
- `diagram.json` → Wokwi circuit diagram
- `README.md` → Documentation

## Team Contributions

| **Name**              | **Student ID** | **Role**                                   | **Responsibilities**                                                                 |
|------------------------|----------------|--------------------------------------------|--------------------------------------------------------------------------------------|
| **Oyoga Martin**       | 253‑505        | IoT Hardware Engineer / Firmware Developer | Designs and connects sensors and actuators, writes embedded firmware for ESP32, ensures reliable data acquisition. |
| **Yugu Emmanuel**      | 240‑935        | Project Manager / Quality Tester           | Oversees project workflow, coordinates tasks, ensures deliverables meet requirements, performs system testing and validation. |
| **Among Brenda**       | 258‑015        | Backend Developer / Database Administrator | Implements server‑side logic, manages database schema and queries, seeds test data, ensures secure and efficient data storage. |
| **Jjumba Ronald Tamale** | 257‑835      | Frontend / Dashboard Developer             | Builds user interface and dashboards, integrates Chart.js visualizations, ensures responsive and user‑friendly design. |

---

### License
This project is for academic purposes under the **IoT Milk Preservation CAT1 Assignment**.
