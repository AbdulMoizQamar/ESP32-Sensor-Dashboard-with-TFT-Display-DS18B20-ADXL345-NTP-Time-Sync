# ESP32-Sensor-Dashboard-with-TFT-Display-DS18B20-ADXL345-NTP-Time-Sync
This project demonstrates how to build a real-time sensor dashboard using the ESP32 microcontroller. It integrates multiple sensors and peripherals to provide useful environmental and motion data on a TFT display along with accurate local time synced over WiFi via NTP.

README Description:
Overview
This project demonstrates how to build a real-time sensor dashboard using the ESP32 microcontroller. It integrates multiple sensors and peripherals to provide useful environmental and motion data on a TFT display along with accurate local time synced over WiFi via NTP.

Features
Temperature monitoring with a DS18B20 waterproof temperature sensor.

3-axis acceleration sensing using the ADXL345 accelerometer for motion detection.

Real-time clock synchronization via Network Time Protocol (NTP) to display accurate local time.

TFT LCD display interface to cycle and show temperature, acceleration values, and current time.

WiFi connectivity to obtain time from an NTP server; WiFi is then turned off to conserve power.

Clean and interactive serial console output for debugging and monitoring sensor data.

Hardware Components
ESP32 Development Board
DS18B20 Temperature Sensor (1-Wire)
ADXL345 Accelerometer (I2C)
TFT Display (SPI interface, pins defined in code)
Push button for user interaction (optional, code can be extended)

Software Libraries Used
WiFi.h (ESP32 WiFi)
time.h (NTP time sync)
OneWire.h and DallasTemperature.h (for DS18B20)
Adafruit_Sensor and Adafruit_ADXL345_U (for accelerometer)
TFT_eSPI (for TFT display control)

How It Works
On startup, the ESP32 connects to a WiFi network and syncs time from an NTP server.
After time synchronization, WiFi is turned off to save power.
The DS18B20 sensor measures ambient temperature.
The ADXL345 sensor captures acceleration in X, Y, Z axes.
The TFT display cycles through showing:
Current temperature in Celsius
Acceleration readings along all axes
Current local time in hours, minutes, and seconds
Serial output logs all sensor readings and time information for debugging.
