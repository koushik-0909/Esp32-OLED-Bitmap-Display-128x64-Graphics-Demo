# **ESP32 OLED Bitmap Display**  
Display custom **128x64 monochrome bitmaps** on an **SSD1306 OLED** using an **ESP32**.  

## **🛠 Hardware Requirements**  
- **ESP32 Board** (ESP32-WROOM, ESP32-C3, etc.)  
- **SSD1306 OLED Display** (128x64, I2C)  
- Breadboard & Jumper Wires  

## **🔌 Wiring (I2C Connection)**  
| OLED Pin | ESP32 Pin |  
|----------|----------|  
| **VCC**  | **3.3V** |  
| **GND**  | **GND**  |  
| **SCL**  | **GPIO 22** (Default I2C SCL) |  
| **SDA**  | **GPIO 21** (Default I2C SDA) |  

> **⚠ Note:** Some ESP32 boards use different I2C pins. Check your board's pinout!  

## **📦 Required Libraries**  
1. **Adafruit SSD1306** ([GitHub](https://github.com/adafruit/Adafruit_SSD1306))  
2. **Adafruit GFX** ([GitHub](https://github.com/adafruit/Adafruit-GFX-Library))  
3. **Wire** (Built-in)  

## **⚙ Setup & Upload**  
1. Install libraries via **Arduino Library Manager**.  
2. Connect the OLED to ESP32 as per wiring above.  
3. Upload the sketch.  
4. The **bitmap will appear instantly** on the OLED.  

## **🎨 Customizing the Bitmap**  
To use your own image:  
1. Convert it to a **128x64 monochrome bitmap**.  
2. Use **LCD Assistant** or **image2cpp** to generate the byte array.  
3. Replace the `myBitmap` array in the code.  

## **🔍 Troubleshooting**  
- **No Display?** Check I2C connections and address (default: `0x3C`).  
- **Wrong Pins?** Modify `Wire.begin(SDA, SCL)` if using non-default I2C pins.  
- **Image Corrupted?** Ensure the byte array matches **128x64 resolution**.  

## **🚀 Extensions**  
- **Animate bitmaps** for simple games or logos.  
- **Add touch controls** to cycle through multiple images.  
- **Integrate with WiFi** to fetch images dynamically.  

