
# Hand Gesture Controlled PowerPoint Navigation

This project uses computer vision and hand tracking to control Microsoft PowerPoint presentations via hand gestures. It utilizes the OpenCV and Mediapipe libraries to detect and recognize hand gestures from a webcam feed. The recognized gestures trigger specific actions like opening PowerPoint, navigating slides, and closing the presentation.

## Features

- **Open PowerPoint**: A "Thumbs Up" gesture opens PowerPoint if it isn't already running.
- **Next Slide**: An "Index Finger" gesture moves to the next slide.
- **Previous Slide**: A "Ring Finger" gesture moves to the previous slide.
- **Close PowerPoint**: A "Pinky Finger" gesture closes PowerPoint.

## Prerequisites

Ensure you have the following installed:

- Python 3.x
- OpenCV (`cv2`)
- Mediapipe
- PyAutoGUI
- Numpy
- psutil

You can install the required Python libraries using pip:

```bash
pip install opencv-python mediapipe numpy pyautogui psutil
```

## How It Works

1. **Hand Detection**: The script captures video from the webcam and processes each frame using Mediapipe to detect and track hand landmarks.
2. **Gesture Recognition**: Based on the positions of specific hand landmarks, gestures like "Thumbs Up," "Index Finger," "Ring Finger," and "Pinky Finger" are recognized.
3. **Action Execution**: When a gesture is recognized, corresponding actions (like navigating PowerPoint slides) are executed.

## Running the Script

To run the script, simply execute the Python file:

```bash
python gesture_control.py
```

Ensure your webcam is connected and accessible.

### Key Controls

- Press **'q'** or close the display window to exit the application.

## Customization

- **Gesture Delay**: The `gesture_delay` variable controls the minimum delay between recognizing the same gesture multiple times. Adjust this to fine-tune the sensitivity.
- **PowerPoint Path**: If PowerPoint is not installed in the default location, update the path in the `open_powerpoint()` function.

## License

This project is licensed under the MIT License.

---

This README provides an overview of the project, instructions for setup and execution, and details on how the script works.
