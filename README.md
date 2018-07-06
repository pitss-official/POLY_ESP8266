# POLY_ESP8266
Easy to use secure client library for ESP 8266. Use it freely using simple commands.
It counters the problems faced by people having no response to AT commands.
Now Connect to Wifi With your ESP8266 without using AT Commands
===========================================================================================
Creating IOT Based Projects Made Easy By - PolyESP8266 (Made by Pawan Kumar)
===========================================================================================
Instructions to use:
METHOD 1 (USING ARDUINO BOARD) [MAKESURE TO INSTALL ESP_8266 library on your PC before proceeding. Seek google for how to install it]
--------------------------------
*Step 1. Connect the Arduino Board to PC
*Step 2. Upload empty void setup and void loop.
*Step 3. Choose your ESP-8266 from boards selection
*Step 3. Connect ESP8266 RX to RX and TX to TX pin on Arduino and GPIO 0 to GND, VCC to 3.3 and GND to GND pins.
*Step 4. Upload Firmware.ino to your ESP8266.
*thats it.
You are ready to go with this firmware.
-------------------------------

Open your serial monitor and type STATE=;
The esp will respond @RSP:OK;
To Connect to WiFi type SSID=your wifiname;PASSKEY=yourwifipassword;
Example: SSID=AndroidAP;PASSKEY=123456789;
to Initate Connection type CONNECT=;
to check wether it has been connected or not type WIFISTATUS=;
to get the IP Address alloted to your esp 8266 type GETIP=;
to get the MAC Address of your ESP8266 type GETMAC=;
for more commands please see commands.pdf
--------------------------------
