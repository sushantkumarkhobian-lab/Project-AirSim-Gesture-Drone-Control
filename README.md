# Gesture Controlled Drone Navigation using AirSim

A real-time gesture-controlled drone navigation system built using Python, OpenCV, MediaPipe, and AirSim. The project enables intuitive drone control through hand gestures, allowing users to navigate a simulated drone without traditional controllers.

## Features

- Real-time hand tracking using MediaPipe
- Gesture-based drone control
- Position hold (hover) functionality
- Gesture-based takeoff
- Gesture-based landing
- Forward and backward navigation
- Left and right navigation
- Altitude control
- Smooth landing mechanism
- Live gesture recognition display
- AirSim drone simulation environment

## Gesture Controls

| Gesture | Action |
|----------|----------|
| Index Finger Up | Move Up / Takeoff |
| Thumb Down | Move Down |
| Index Finger Left | Move Left |
| Thumb Right | Move Right |
| Two Fingers Up | Move Forward |
| Two Fingers Down | Move Backward |
| Closed Fist | Hover at Current Position |
| Three Fingers Up | Land |

## Hover Mode

When a closed fist is detected, the drone stores its current position and continuously corrects its movement to remain at that location, creating a position-hold effect similar to real drone hover modes.

## Landing Mode

When three fingers pointing upward are detected:

- Landing procedure starts immediately
- All other commands are ignored
- Drone descends automatically
- Command lock is removed after timeout

## Technologies Used

- Python
- OpenCV
- MediaPipe
- AirSim
- Computer Vision
- Human-Computer Interaction

## Installation

### AirSim Setup

Please refer to the following repository for complete AirSim installation and setup instructions:

https://github.com/sushantkumarkhobian-lab/AirSim-Drone-Navigation

### Install Required Libraries

```bash
pip install opencv-python
pip install mediapipe
pip install airsim

```

## Output

<img width="1000" alt="Demo_Output" src="https://github.com/user-attachments/assets/ab6f7f97-3619-439a-a031-4ba09d95e06d" />






