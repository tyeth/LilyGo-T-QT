<h1 align = "center"> 🌟T-QT🌟</h1>

<img  width="480" src=image/logo.png>

## Description

T-QT is a development board whose main control chip is ESP32-S3. It is equipped with a 0.85-inch LCD color screen and two programmable buttons. Retains the same layout design as T-Display. You can directly use ESP32S3 for USB communication or programming.

***
## Pinmap

<img  width="480" src=image/pinmap_en.jpg>
<img  width="480" src=image/specifications_en.jpg>

***
<h3 align = "left">Product 📷:</h3>

| Product |                            Product Link                             |
| :-----: | :-----------------------------------------------------------------: |
|  T-QT   | [AliExpress](https://www.aliexpress.com/item/1005004405292321.html) |


***
## Quick Start

> Arduino:
>- Click "File" in the upper left corner -> Preferences -> Additional Development >Board Manager URL -> Enter the URL in the input box.
(ESP32S3 is a new chip, and the SDK version needs to be version 2.0.3 or above)
> `https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json`
>-  Click OK and the software will be installed by itself. After installation, restart the Arduino IDE software.

> PlatfromIO:
> - PlatformIO plug-in installation: Click on the extension on the left column -> search platformIO -> install the first plug-in
> - Click Platforms -> Embedded -> search Espressif 32 in the input box -> select the corresponding firmware installation

> ESP-IDF:
> - The installation method is also inconsistent depending on the system, it is recommended to refer to the [official manual](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html) for installation


***
## Quick question and answer
1. Does the onboard lithium battery charge function?
> T-QT does not have the function of charging lithium batteries, but it can support the access of lithium batteries at that time. The battery voltage status can be detected using IO4. 
2. Is it normal for the chip to continue to heat up during use?
> The ESP32S3 will continue to heat up during use. Due to the small size of the baseboard, the heat of the ESP32S3 cannot be dissipated in time, so the overall temperature is stable at about 50-60 degrees Celsius. This temperature does not affect the normal use of the chip.
3. Unable to write?
> Press and hold the BOOT button on the board (located on the left side of the front of the screen), keep it tight, then plug in the USB and click to upload the sketch

## Tips

- The program can be written normally, but there is still no display after writing
    1. There are factory test files in the firmware folder, which can be flashed into the board to check whether the board is normal. If there is still no display, then it can be judged that there is a problem with the board or the screen
    2. Delete the <TFT_eSPI> in the libraries, and replace the <TFT_eSPI> in the <lib> folder of the main page to the libraries directory
    3. When opening the Arduino IDE, it prompts whether to upgrade the library, please choose not to upgrade, otherwise it will overwrite the configuration of the <TFT_eSPI> display