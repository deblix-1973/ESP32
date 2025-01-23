# ESP32_1.8_SPI_DISPLAY
## 1.8 Inch SPI Display on S2-MINI Board driven by UniversalDisplay and ST7735 Driver.
![ESP32_1 8_SPI_DISPLAY](https://github.com/user-attachments/assets/110dd347-68e3-4918-b1d6-bf47b45172f8)
## How To

### Step 1
Flash your ESP32 with tasmota-display.bin. Reboot and connect to your Wifi.\
Ensure to use the correct firmware depending on your board (ESP-S2, ESP-C3 etc.)!\
> [!NOTE] You will need **Universal File System** Support (for the diplay.ini file) and **UniversalDisplay** Support on the device.\
This will only work with 4M+ devices.

### Step 2
Open the Web UI and go to Configuration > Module

> GND > GND\
> VCC > 3.3V\
> SCL > GPIO07 > SPI CLK\
SDA > GPIO11 > `SPI MOSI`\
RES > GPIO05 > Display Rst\
DC > GPIO09 > SPI DC\
CS > GPIO012 > SPI CS\
BLK > GPIO03 > PWM (to adjust Backgrund LED in WebUI)\

and set any unused GPIO to **OptionA3** to enable driver\
here GPIO02 > OptionA3	

