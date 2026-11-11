# Piko
My cute mini cute keychain with ESP32-C3 SuperMini , 0.96-inch SSD1306 OLED , TTP223 touch , six indicator LEDs and a active buzzer.
the repo has a custom KiCad PCB, Gerber files and a basic Arduino animation firmware that displays the bitmapped frames of the 712 GIFs with touch and led controls.

<img width="677" height="544" alt="image" src="https://github.com/user-attachments/assets/25bbb17e-43fa-4b20-ab7e-608a250a04ce" /> 

# Details
1) ESP32-C3 SuperMini as the controller
2) 0.96-inch, 128×64 SSD1306 I²C OLED
3) Bitmap-frame animation at a target of approximately 24 FPS
4) TTP223 touch sensor input
5) Buzzer connection
6) 6 leds & 6 resitors
7) 1 transistor
8) LiPo battery connection pads
9) Custom PCB designed in KiCad
10) KiCad source files and Gerber files included


## Required Library Setup

Open Arduino IDE
Install OLED libraries: Tools -> Manage Libraries -> search Adafruit SSD1306 -> install
fig1

Add esp32 additional board manager URL: Files -> Preferences -> add https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_dev_index.json to Additional Boards Manager URLs

install esp32 board manager: Tools -> Board -> Boards Manager -> search esp32 -> install esp32 by Espressif Systems

## Components 
 refer BOM.csv

## ## Display

The project uses a:

**0.96" 128×64 SSD1306 I2C OLED**

The OLED is connected directly to the ESP32-C3.

## Pin connections

The firmware uses the I²C pins given below on the ESP32-C3 SuperMini:-

| Signal | ESP32-C3 pin |
|---|---|
| OLED SDA | GPIO8 |
| OLED SCL | GPIO9 |
| OLED power | 3V3 |
| OLED ground | GND |
| TTP223 output | GPIO3 |

## 
## Firmware

The Arduino firmware and bitmap frames are provided in `Firmware' folder

## Firmware Installation 

1. Download the raw PIKO_FIRMWARE.zip file
2. open Arduino IDE
3. open PIKO_FIRMWARE.ino
4. upload to your device

### Requirements for uploading firmware

1) Arduino IDE
2) ESP32 Arduino core
3) **Adafruit GFX Library**
4) **Adafruit SSD1306**

### Upload

1. extract Firmware/PIKO_FIRMWARE.zip
2. open the PIKO_FIRMWARE.ino file
3. ensure that all_frames.h is in the same directory as the sketch
4. install the Adafruit GFX and Adafruit SSD1306 libraries using Library Manager
5. select the correct ESP32-C3 board and serial port
6. upload the sketch and open the Serial Monitor (with baud rate 115200)

The current firmware targets 42 ms per frame (means about 24 FPS).

## PCB 

<img width="700" height="519" alt="image" src="https://github.com/user-attachments/assets/1858e9d9-c8f9-41e4-a99c-7e7ddc623fd4" />

## SHEMATICS
<img width="838" height="562" alt="image" src="https://github.com/user-attachments/assets/c01a1928-cd9c-4c10-a50d-d8c1f7014378" />

## CREDITS 
 CREDITS TO MYSELF EVERYTHINGG OWN IDEA HEHE and THIS PROJECT WAS MADE FOR #EMBASSY YSWS BY HACKCLUB
