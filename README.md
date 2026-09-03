# Postura – Smart Posture Monitoring Device

Postura is a smart posture monitoring device designed to help students and desk-heavy professionals improve sitting habits during long work or study sessions. The system uses an ESP32 microcontroller, an 8x8 time-of-flight distance sensor, and vibration motors to detect when a user begins to slouch and provide real-time haptic feedback.

This project was developed for **UCSD ECE 140B** as a product-focused embedded systems project. My role focused on hardware integration, sensor testing, vibration feedback, prototype design, and customer validation.

---

## Project Overview

Many people sit for hours while studying, working, or gaming and only notice their posture after discomfort or pain begins. Postura addresses this by giving users a quiet, low-distraction reminder when their posture changes from a calibrated upright position.

The device is designed to be passive and chair-mounted, meaning users do not need to wear a strap, wristband, or harness. Once calibrated, Postura monitors the user’s seated position and provides vibration feedback when poor posture is detected.

---

## Key Features

- Real-time posture detection using an 8x8 ToF distance sensor
- ESP32-based embedded sensing and wireless communication
- Calibration mode for setting a user’s upright posture baseline
- Posture classification for good posture, mild slouch, severe slouch, and leaning back
- Dual vibration motor feedback for silent posture reminders
- MQTT communication between the device and backend
- FastAPI dashboard for live posture monitoring and session tracking
- Customer validation through interviews with students and desk-heavy professionals

---

## System Architecture

```text
User Sitting Position
        ↓
VL53L5CX 8x8 ToF Sensor
        ↓
ESP32 Microcontroller
        ↓
Posture Classification Logic
        ↓
Vibration Motor Feedback
        ↓
MQTT Communication
        ↓
FastAPI Backend
        ↓
Live Dashboard / Session Tracking
```

---

## Hardware Components

| Component | Purpose |
|---|---|
| ESP32 | Main microcontroller for sensing, logic, and wireless communication |
| VL53L5CX ToF Sensor | Measures distance between the device and the user’s back |
| Vibration Motors | Provide haptic feedback when slouching is detected |
| LiPo Battery | Powers the portable prototype |
| 3D-Printed Housing | Holds electronics and mounts to the chair/pillow system |
| Pillow / Chair Mount | Positions the device behind the user |

---

## Software Components

### ESP32 Firmware

The ESP32 firmware reads the 8x8 ToF sensor, calibrates the user’s upright posture, classifies posture states, and triggers vibration feedback. The firmware also publishes posture data over MQTT so the backend can display live sensor information.

### Backend Server

The backend receives posture data from the ESP32 using MQTT. It also supports live dashboard updates, posture session tracking, and data logging.

### Web Dashboard

The dashboard allows users to view live posture data, calibrate their posture baseline, and track posture behavior over time.

---

## Customer Discovery

We conducted customer interviews with students and desk-heavy professionals to validate the problem. Interviewees reported poor posture during long sitting sessions and often only noticed the issue after pain, soreness, or fatigue started.

Key findings:

- Users lose posture awareness when focused on studying, work, or deadlines.
- Many users have no active posture solution beyond pillows, stretching, chair adjustments, or footrests.
- Vibration feedback was preferred because it is quiet and less distracting.
- Users wanted a passive chair-mounted solution instead of a wearable device.
- A healthcare professional suggested adding a pause/on-off feature to avoid alerts during normal movement.

---

## Business Model

Postura is designed as a one-time purchase product with two possible versions:

| Version | Estimated Price | Estimated Unit Cost | Gross Profit |
|---|---:|---:|---:|
| Standard Device | $22.99 | $12 | ~$10 |
| Pillow Upgrade | $42.99 | $30 | ~$13 |

The initial target market is students and desk-heavy professionals who sit for long periods and want a simple posture reminder that does not interrupt their workflow.

---

## My Contributions

- Integrated ESP32 hardware with the ToF sensor and vibration motors
- Helped design and test the posture feedback system
- Supported prototype wiring, power setup, and physical mounting
- Tested posture states such as upright sitting, mild slouching, severe slouching, and leaning back
- Conducted customer interviews to validate pain points and product direction
- Helped define the product’s value proposition, traction, and business model

---

## Challenges and Lessons Learned

One major design challenge was creating a posture reminder that was helpful without being annoying. Interviews showed that users care about posture, but they do not want a device that interrupts studying or work. This pushed the project toward quiet vibration feedback, a passive chair-mounted design, and a future pause/on-off feature.

Another challenge was distinguishing true slouching from normal movement, such as reaching for an item or shifting in a chair. Future testing would focus on improving classification accuracy and reducing false alerts.

---

## Future Improvements

- Add a pause/on-off feature for moments when users are moving around
- Improve detection accuracy across different body types and chairs
- Add mobile app support
- Expand session tracking and long-term posture analytics
- Integrate with Apple Health or other wellness platforms
- Run longer user testing with students and desk-heavy professionals

---

## Team

Developed by Group 12 for UCSD ECE 140B.

Team members:

- Aden Tan
- Alex Wei
- Colin Hua
- Richard Kim