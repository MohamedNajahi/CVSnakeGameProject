# Real-Time Hand-Tracked Snake Game

# Gameplay Instructions
- Use your hand to control the snake's movement.
- Avoid collisions with the snake's body.
- Eat food items to increase your score and the snake's length.
- Press 'r' to restart the game.
- Press 'p' to pause/unpause the game.
- Troubleshooting
- Issue: The webcam does not turn on.


## Overview
The Real-Time Hand-Tracked Snake Game is an interactive game that utilizes computer vision to track hand movements via a webcam. Players control a snake by moving their hands, aiming to eat food items while avoiding collisions. The game includes sound effects for various events and maintains a high score.

## Features
- Real-time hand tracking using a webcam.
- Interactive gameplay with visual and audio feedback.
- High score tracking.
- Game pause and restart functionality.

## Prerequisites

### Hardware
- A computer with a webcam.

### Software
- Python 3.x

### Required Libraries
- OpenCV
- NumPy
- cvzone
- playsound3
- pickle-mixin

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/realtime-snake-game.git
    cd realtime-snake-game
    ```

2. Install the required libraries:
    ```bash
    pip install opencv-python-headless numpy cvzone playsound3 pickle-mixin
    ```

3. Ensure that you have the required sound files (`food_eaten.mp3` and `game_over.mp3`) and the food image file (`egg.png`) in the same directory as the main script.

## Project Files

- `main.py`: The main script to run the game.
- `egg.png`: The image used for the food.
- `food_eaten.mp3`: Sound effect for eating food.
- `game_over.mp3`: Sound effect for game over.
- `high_score.pkl`: File to store the high score.

## Code Explanation

### Imports and Setup

The project begins with importing necessary libraries and setting up the webcam:

```python
import math
import random
import cvzone
import cv2
import numpy as np
from cvzone.HandTrackingModule import HandDetector
from playsound3.playsound3 import playsound
import threading
import pickle
import os
import time

