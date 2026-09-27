# ESP32 Firmware

PlatformIO firmware for the VL53L5CX 8×8 ToF sensor, upright
calibration, posture classification, vibration feedback, and MQTT.

## Setup

1. Install the PlatformIO IDE extension in VS Code.
2. Open this `esp32/` folder as the project.
3. Copy `env.example` to `.env` and enter your Wi-Fi credentials.
4. In `src/main.cpp`, use `wpaWifi = true` for UCSD enterprise
   Wi-Fi or `false` for a regular home network.
5. Confirm the board configuration in `platformio.ini` matches
   your hardware. The current target is `esp32-s3-devkitc-1`.
6. Connect the board by USB, then use PlatformIO Build and Upload.
7. Open Serial Monitor at 115200 baud.

Sit upright for five seconds when calibration begins.

## Feedback

| Posture | Vibration |
|---|---|
| Good | Off |
| Mild slouch | Pulsed |
| Severe slouch | Continuous |
| Leaning back | Off |

## Dashboard Connection

Match the MQTT broker and topic prefix across the firmware and
your chosen application:

- Firmware: `TOPIC_PREFIX` in `src/main.cpp`
- Website: `MQTT_TOPIC` in `website/.env`
- Sensor dashboard: `TOPIC_PREFIX` in `python/.env`

The included firmware prefix is `chuach1234`.

Use external motor driver circuits, and verify wiring before
powering the device. Keep `.env` credentials out of Git.