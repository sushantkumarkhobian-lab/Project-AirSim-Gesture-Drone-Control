# Gesture Controlled Drone Navigation using Project AirSim

A real-time gesture-controlled drone navigation system built using Python, OpenCV, MediaPipe, and Project AirSim. This project enables intuitive drone control through hand gestures, allowing users to navigate a simulated drone without traditional controllers.

---

## Live Demonstration

<img width="1000" alt="Screen Recording 2026-06-27 172415" src="https://github.com/user-attachments/assets/a459d41a-7ab5-4937-8ac2-1fa166a7a9b3" />

---

## Features

* Real-time hand tracking using MediaPipe
* Gesture-based drone control in simulation
* Takeoff and landing using hand gestures
* Forward, backward, left, and right navigation
* Altitude control (ascend and descend)
* Hover (position hold) using closed fist
* Instant land + reset (clean session restart required)
* Live gesture display on camera feed
* Stable velocity-based movement (prevents altitude drift in horizontal motion)

---

## Gesture Controls

| Gesture           | Action                            |
| ----------------- | --------------------------------- |
| Index Finger Up   | Takeoff / Move Up                 |
| Index Finger Down | Move Down                         |
| Index Finger Left | Move Left                         |
| Thumb Right       | Move Right                        |
| Two Fingers Up    | Move Forward                      |
| Two Fingers Down  | Move Backward                     |
| Closed Fist       | Hover (Stop motion)               |
| Three Fingers Up  | Land (Stop + Disarm + Disconnect) |

---

## Hover Mode

When a closed fist is detected, the drone stops all motion by sending zero velocity commands continuously, maintaining a stable hover at its current position.

---

## Landing Mode

When **three fingers up** is detected:

* Drone immediately stops all motion
* Drone is disarmed
* API control is disabled
* Simulation connection is closed
* Program exits cleanly

> After landing, the system must be restarted to regain control. This ensures a clean and stable state reset in Project AirSim.

---

## Technologies Used

* Python
* OpenCV
* MediaPipe
* Project AirSim
* Computer Vision
* Human-Computer Interaction

---

## Installation


### Install Dependencies

```bash
pip install opencv-python
pip install mediapipe
pip install projectairsim
```

---

## Notes

* Horizontal movement uses velocity control with fixed altitude to prevent drift
* Gesture detection is based on MediaPipe hand landmarks with temporal smoothing
* LAND gesture is designed as a hard stop for safety and clean reset
* System requires a restart after landing for fresh initialization

---








