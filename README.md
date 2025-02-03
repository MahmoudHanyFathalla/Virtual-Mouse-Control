# Virtual Mouse Control using Hand Gestures

This project uses **Mediapipe** and **OpenCV** to detect hand gestures and control the mouse cursor on your computer screen in real-time. By tracking hand movements and recognizing specific gestures, the program enables intuitive control of the mouse, such as moving the cursor and simulating mouse clicks using hand gestures.

---

## Features

- **Hand Gesture Recognition**: Detects hand movements and finger positions using Mediapipe's hand tracking model.
- **Mouse Movement**: Controls the mouse cursor position based on the movement of the index and middle fingers.
- **Mouse Click Simulation**: Recognizes hand gestures (e.g., fist) to simulate mouse clicks.
- **Real-time Visualization**: Displays a live webcam feed with hand landmarks drawn for real-time feedback.
- **Multi-platform Support**: Works on any system with Python, OpenCV, and Mediapipe support.

---

## Requirements

### Software:
- Python 3.6+ (Recommended)
- **Libraries**:
  - `opencv-python` (for video capturing and GUI display)
  - `mediapipe` (for hand gesture detection)
  - `pyautogui` (for simulating mouse movements and clicks)
  - `win32api` (Windows-specific library for mouse control)
  - `screeninfo` (for retrieving screen dimensions)

### Installation:

To install the necessary dependencies, use the following `pip` commands:

```bash
pip install opencv-python mediapipe pyautogui pywin32 screeninfo
```

---

## How It Works

1. **Hand Detection**: The system uses **Mediapipe** to track your hand in the webcam feed. It detects 21 key landmarks on your hand, such as the positions of the thumb, index, middle, and other fingers.
  
2. **Gesture Recognition**: Specific hand gestures, such as raising fingers or making a fist, are used to control mouse behavior:
   - **Move Mouse**: When your fingers (index and middle) move, the mouse cursor will follow the movement.
   - **Mouse Click**: If you form a fist or use a predefined gesture, the program simulates a mouse click.
  
3. **Real-time Visualization**: A live webcam feed is displayed with the detected hand landmarks drawn on the screen, showing how the system tracks the hand in real time.

---

## Usage

1. Run the Python script:

   ```bash
   python virtual_mouse.py
   ```

2. The program will start capturing from your default webcam. Ensure your hand is visible to the webcam.
3. Perform gestures:
   - Move your fingers (index and middle) to move the cursor on the screen.
   - Make a fist or another gesture to simulate a mouse click.
4. Press **Esc (ESC)** to exit the program.

---

## Code Breakdown

- **Hand Gesture Detection**:
  The script uses **Mediapipe** to detect hand landmarks from the webcam feed. The landmarks are processed to determine the positions of the fingers and hand.

- **Mouse Movement**:
  The positions of the index and middle fingers are mapped to screen coordinates. The `pyautogui` library is used to move the mouse on the screen.

- **Mouse Click Simulation**:
  Based on specific gestures (such as a closed fist), the program simulates a mouse click using `win32api` or `pyautogui`.

---

## Example

Here’s an example of a gesture controlling the mouse:

1. **Move the mouse** by moving your index and middle fingers.
2. **Click the mouse** by forming a fist or another predefined gesture.
3. The system continuously tracks hand movements and updates the mouse position accordingly.

---

## Troubleshooting

- **No Hand Detected**: Ensure your hand is within the camera's view and properly framed in the webcam.
- **Mouse Movement Lag**: If there’s noticeable lag, reduce the webcam resolution or increase the increment rate for smoother tracking.
  
---

## License

This project is open-source and available under the **MIT License**. Feel free to modify or use it in your own projects.

---

## Acknowledgments

- **Mediapipe**: For the hand tracking model used in this project.
- **OpenCV**: For the image processing and real-time webcam capture.
- **pyautogui**: For simulating mouse movement and clicks.
- **screeninfo**: For handling screen dimensions to map the cursor correctly.
