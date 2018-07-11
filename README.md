
# POLY_ESP8266
>Easy to use secure client library for ESP 8266. Use it freely using simple commands.
>It counters the problems faced by people having no response to AT commands.
>Now Connect to Wifi With your ESP8266 without using AT Commands
### Creating IOT Based Projects Made Easy By - PolyESP8266 (Made by Pawan Kumar)
## Instructions to use:
##### METHOD 1 (USING ESP8266 FLASHER and Arduino Board)
- Step 1. Connect the Arduino Board to PC
- Step 2. Upload empty void setup and void loop.
- Step 3. Choose your ESP-8266 from boards selection
- Step 3. Connect ESP8266 RX to RX and TX to TX pin on Arduino and GPIO 0 to GND, VCC to 3.3 and GND to GND pins.
- Step 4. Upload Firmware.bin to your ESP8266 using ESP8266 Flash Tool.
- thats it. You are ready to go with this firmware.
### How to use your ESP8266 for IOT Projects without AT Commands?
- Open your serial monitor with 9600 rate.
- The device will display @:RET=START;
- Type your Desired Command to perform the operation.
- It also has a feature to store and connect to the last connected Wirless Address.
##### Here are few commands that you can use in your projects.
###### Check the Status of the device
- STATUS=;
- [THE DEVICE WILL RESPOND @:RET=OK;]
###### Connect to Wifi eg. AndroidAP having password 123456789
- SSID=AndroidAP;
- [THE DEVICE WILL RESPOND ###OK:SSID=AndroidAP]
- PASSKEY=123456789;
- [THE DEVICE WILL RESPOND ###OK:PASSKEY=123456789]
###### You can also use multiple commands in one line
- SSID=AndroidAP;PASSKEY=123456789;
- [###OK:SSID=AndroidAP
###OK:PASSKEY=123456789]
###### INITIATE CONNECTION TO THE WIFI
- CONNECT=;
- [###OK:CONNECT=]
###### CHECK IF YOU ARE CONNECTED TO WIFI
- SHOW=;
- Or You can also use WIFISTATUS=;
- [The Device will return @:RET=CONNECTED;]
###### You can check the ip or mac address of your esp8266
- GETIP=;
- [THE DEVICE WILL SHOW @:RET=192.168.43.11;]
- IF YOU ARE NOT CONNECTED TO THE WIFI IT WILL SHOW 0.0.0.0 IN @RET
- GETMAC=;
- [THE DEVICE WILL RETURN @:RET=AA:AA:AA:AA:AA:AA;]
###### To connect to the server
- SERVER=www.server.com;
- [###OK:SERVER=www.server.com]
- PORT=443;
- [###OK:PORT=443]
- STARTSESSION=;
- [@:RET=FAILED;] IF SERVER IS NOT REACHABLE
- [@:RET=CONNECTED;] IF YOU ARE CONNECTED
- If you want to send your data through a API on that server example www.server.com/api?values=123456&key=123456789&...
- type URI=api?values=123456&key=123456789&...;
- [MAKE SURE YOU DON'T USE = OR ; IN THE URI STRING. ; IS USED ONLY AT THE LAST OF URI]
- type HEADERS.OUT=; to see the status of the API Request
- to get the output of API Request type HTML.OUT=;
##### It is important remember following things while using this firmware
- ###### All the statements starting with ###OK: are debug statements. You can disable them by DEBUG=DISABLE; or enable by DEBUG=ENABLE; All debug statements start with ###OK: and echo out your command.
- ###### All the statements starting with @RET: are return statements. You can change their output at some commands into integer 1 or 0 depending upon output. For example @:RET=CONNECTED; will now be @:RET=1; For this you need to type RETBOOL=ENABLE; or RETBOOL=1; All return statements start with @RET: and end with ;.

- For Example programs refer examples folder

### Stuck somewhere? Feel free to contact 
## support@megaminds.tech
