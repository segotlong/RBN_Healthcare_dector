components 
| Component              | Pin on Component | Connected to ESP32 Pin        | Notes                                 |
| ---------------------- | ---------------- | ----------------------------- | ------------------------------------- |
| **Pulse Sensor**       | Signal (S)       | GPIO34 (Analog Input)         | Reads pulse wave data                 |
|                        | VCC              | 3.3V                          | Power supply                          |
|                        | GND              | GND                           | Ground connection                     |
| **Temperature Sensor** | Data             | GPIO32 (Analog/Digital Input) | Measures temperature                  |
|                        | VCC              | 3.3V                          | Power supply  
|                        | GND              | GND                           | Ground connection                     |
| **LCD Display (I²C)**  | SDA              | GPIO21 (SDA)                  | I²C data line                         |
|                        | SCL              | GPIO22 (SCL)                  | I²C clock line                        |
|                        | VCC              | 5V                            | Power supply                          |
|                        | GND              | GND                           | Ground connection                     |
| **Battery**            | +                | VIN                           | 9V battery through switch             |
|                        | –                | GND                           | Ground                                |
| **Switch**             | In-line with VIN | VIN (ESP32 input)             | Controls power flow                   |

Software Development:
Library Integration
You included essential libraries:
WiFi.h for internet connectivity.
HTTPClient.h for sending data to the server (ThingSpeak).
PulseSensorPlayground.h for pulse detection.
DFRobot_MLX90614.h for temperature readings.
LiquidCrystal_I2C.h for LCD display.
<img width="642" height="212" alt="picture 38" src="https://github.com/user-attachments/assets/a8bde3ff-bf24-416c-873a-05c1e0dbb148" />:
 Threshold Settings:
 Pulse Rate Thresholds
Normal resting range: 60 – 100 BPM
Below 60 BPM → device shows Low Pulse Alert
Above 100 BPM → device shows High Pulse Alert
Temperature Thresholds:
Normal body temperature: 36.5°C – 37.5°C
Below 36.5°C → device shows Low Temperature Alert
Above 37.5°C → device shows Fever Alert
<img width="942" height="763" alt="picture 39 " src="https://github.com/user-attachments/assets/3bfbbb52-bdf3-468d-9072-ef8f605e4ef6" />

