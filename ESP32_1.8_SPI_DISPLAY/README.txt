# ESP32_1.8_SPI_DISPLAY
## 1.8 Inch SPI Display on S2-MINI Board driven by UniversalDisplay and ST7735 Driver.
image
## How To

### Step 1
Flash your ESP32 with tasmota-display.bin. Reboot and connect to your Wifi.\
Ensure to use the correct firmware depending on your board (ESP-S2, ESP-C3 etc.)!\
You will need Universal File System Support (for the diplay.ini file) on the device. So this will only work with 4M+ devices.

### Step 2
Open the Web UI and go to Configuration > Module

3.3V   > VCC\
GND    > GND\
GPIO03 > LedLink (for MQTT Status)\
GPIO04 > PN532 Rx\
GPIO05 > PN532 Tx\
GPIO12 > Relay1 (not relevant here - used for other purpose in my project)\
GPIO13 > Relay2 (not relevant here - used for other purpose in my project)\
GPIO14 > Relay3 (not relevant here - used for other purpose in my project)\
and save your configuration.
### Step 3
In the Web UI go to Configuration > MQTT and set up MQTT.

#### Done!
You can now communicate with your ESP8266 via MQTT and get Card IDs (UID) from your PN532.
#### Config
```{"NAME":"PN532","GPIO":[1,1,1,544,2880,2848,1,1,224,225,226,1,1,1],"FLAG":0,"BASE":18}```

[z] [x0y0C65535][f2]BIRKENSTR[x0y27C19679][f4s3]32[x129y63C53023][k30][x1y105C53023][h156][x0y111C65535][f2]SEIBOLD

