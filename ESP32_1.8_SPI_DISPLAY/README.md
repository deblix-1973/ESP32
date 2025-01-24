# ESP32_1.8_SPI_DISPLAY
## 1.8 Inch SPI Display on S2-MINI Board driven by UniversalDisplay and ST7735 Driver.
![ESP32_1 8_SPI_DISPLAY](https://github.com/user-attachments/assets/110dd347-68e3-4918-b1d6-bf47b45172f8)
## How To
### Step 1
Flash your ESP32 with tasmota32-display.bin. Reboot and connect to your Wifi and MQTT broker.\
Ensure to use the correct firmware depending on your board (ESP-S2, ESP-C3 etc.).
> [!TIP]
> You will need **Universal File System** Support (for the diplay.ini file) and **UniversalDisplay** Support on the device.\
> This will only work with 4M+ devices.
### Step 2
Open the Web UI and go to Configuration > Module

| Display | S2-Mini GPIO | Module |
| --- | --- | --- |
| GND | GND | `GND` |
| VCC | 3.3V | `3.3V` |
| SCL | GPIO07 | `SPI CLK` |
| SDA | GPIO11 | `SPI MOSI` |
| RES | GPIO05 | `Display Rst` |
| DC | GPIO09 | `SPI DC` |
| CS | GPIO012 | `SPI CS` |
| BLK | GPIO03 | `PWM` |

Set any unused GPIO to `OptionA3` (e. g. GPIO02) to start uDriver and load the display driver settings.

### Step 3
Download the corresponding display.ini file from the Tasmota Github Space and upload this file to your device.

### Step 4
Adjust your Display via Console using commands like...
+ DisplayModel
+ DisplayMode
+ DisplayRotate
+ DisplayText

> [!NOTE]
> The command **DisplayDimmer** will not work with this example as it is controlled via the slider in the WebUI.
> 
> ![WebUI](https://github.com/user-attachments/assets/a8e20420-09a8-4834-abca-12677e112e40)

### Ready to Go!


