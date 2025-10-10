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
- You included essential libraries:
- WiFi.h for internet connectivity.
- HTTPClient.h for sending data to the server (ThingSpeak).
- PulseSensorPlayground.h for pulse detection.
- DFRobot_MLX90614.h for temperature readings.
- LiquidCrystal_I2C.h for LCD display.
<img width="642" height="212" alt="picture 38" src="https://github.com/user-attachments/assets/a8bde3ff-bf24-416c-873a-05c1e0dbb148" />:
 - Threshold Settings:
 - Pulse Rate Thresholds
- Normal resting range: 60 – 100 BPM
- Below 60 BPM → device shows Low Pulse Alert
- Above 100 BPM → device shows High Pulse Alert
- Temperature Thresholds:
- Normal body temperature: 36.5°C – 37.5°C
- Below 36.5°C → device shows Low Temperature Alert
- Above 37.5°C → device shows Fever Alert
- <img width="942" height="763" alt="picture 39 " src="https://github.com/user-attachments/assets/3bfbbb52-bdf3-468d-9072-ef8f605e4ef6" />

<img width="950" height="701" alt="picture 17" src="https://github.com/user-attachments/assets/adf95965-6a7a-4d8d-96d7-9e940fe42260" />
<img width="636" height="418" alt="picture 19" src="https://github.com/user-attachments/assets/34722ee9-1414-4cef-95bd-d33ca5dc393c" />
<img width="407" height="408" alt="picture 20" src="https://github.com/user-attachments/assets/3440d723-63f5-47b4-8999-49d69da105dd" />
<img width="692" height="635" alt="picture 34" src="https://github.com/user-attachments/assets/a9ae2c42-f844-4e88-84bd-9d4640982743" />
<img width="1920" height="1080" alt="PICTURE 33" src="https://github.com/user-attachments/assets/8d9a8bb8-bde0-4a14-b8b1-2d2187928a44" />
<img width="577" height="391" alt="picture 35" src="https://github.com/user-attachments/assets/749e1c9d-b166-4dc0-a38b-f726d5a30cae" />
<img width="942" height="764" alt="Screenshot 2025-09-17 090517" src="https://github.com/user-attachments/assets/a26357a3-3089-4b22-b734-56b95026443d" />
<img width="1407" height="751" alt="Screenshot 2025-09-17 153346" src="https://github.com/user-attachments/assets/a8acc202-f146-4af3-bbb1-2ffed5d8e270" />



