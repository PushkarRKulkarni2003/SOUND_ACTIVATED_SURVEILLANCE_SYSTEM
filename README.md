# SOUND ACTIVATED SURVEILLANCE SYSTEM

A simple surveillance setup using **ESP32-CAM** + **INMP441 microphone**.  
When the sound crosses a threshold, the ESP32-CAM captures an image and records a short audio clip to **SPIFFS**, which can be viewed/downloaded from a **local web interface**.

## Hardware
- ESP32-CAM (OV2640)
- INMP441 I2S Microphone  
  - WS → GPIO2  
  - SCK → GPIO14  
  - SD → GPIO15

## Features
- Detects sound threshold in real-time
- Captures image + audio clip
- Stores data in SPIFFS
- Local web server for viewing/downloading files

## Usage
1. Flash the code to ESP32-CAM.
2. Connect the mic as per the pins above.
3. Update WiFi credentials in code.
4. Access the web interface at:  
   `http://<ESP32-IP>/`

## Future Improvements
- Add emergency-sound CNN classifier
- Push notification on trigger
