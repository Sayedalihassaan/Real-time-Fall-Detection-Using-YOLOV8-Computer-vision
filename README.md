
# Real-time Fall Detection Using YOLOv8 and Computer Vision

## 📜 Overview

This project aims to detect falls in real-time using computer vision and deep learning techniques. By leveraging the power of the YOLOv8 object detection model, the system identifies persons in a video feed and assesses whether they are falling based on their posture and movement patterns.

### 🌟 Key Features

- **Real-Time Detection:** Detects falls in live video streams or pre-recorded videos.
- **YOLOv8 Integration:** Uses the state-of-the-art YOLOv8 model for robust person detection.
- **Pose Estimation:** Employs MediaPipe for accurate human pose estimation.
- **Alerts and Notifications:** Sends real-time alerts through audio alarms and Telegram notifications.
- **Custom Tracking:** Uses a custom object tracker to track individual persons across frames.

## 🎥 Demo

![Fall Detection Demo](demo.gif)  
*Real-time fall detection in action.*

## 🛠️ Installation

Follow these steps to set up the project on your local machine.

### Prerequisites

- Python 3.7+
- `pip` package manager

### Libraries and Dependencies

Install the necessary libraries using pip:

```bash
pip install opencv-python mediapipe ultralytics numpy cvzone pygame telepot
```

### Additional Setup

1. **YOLOv8 Weights:**
   - Download the YOLOv8 weights file (`yolov8n.pt`) and place it in the project directory.

2. **COCO Class Names:**
   - Ensure you have a `coco.txt` file in your project directory containing the COCO class names.

3. **Telegram Bot:**
   - Create a Telegram bot and get the bot token and chat ID to enable notifications. Replace the placeholders in the script with your bot's details.

4. **Audio Alert:**
   - Ensure you have an `alarm.wav` file for audio alerts in your project directory.

## 🚀 Usage

1. **Navigate to the Project Directory:**

    ```bash
    cd path_to_your_project
    ```

2. **Run the Script:**

    ```bash
    python fall_detection.py
    ```

3. **Stop the Program:**
   - Press 'q' to stop the video and exit the program.

## 📂 Project Structure

```
Real-time-Fall-Detection-Using-YOLOv8-Computer-vision
│
├── fall_detection.py          # Main script to run fall detection
├── tracker.py                 # Custom tracker for person tracking
├── yolov8n.pt                 # YOLOv8 weights file
├── coco.txt                   # COCO class names file
├── alarm.wav                  # Alarm sound file for fall detection
└── README.md                  # Project documentation
```

## ⚙️ How It Works

1. **Video Capture:**
   - The program captures video from a file or a live stream.

2. **Person Detection:**
   - YOLOv8 detects persons in the video frames.

3. **Pose Estimation:**
   - MediaPipe detects keypoints of the detected persons for pose estimation.

4. **Fall Detection Logic:**
   - If a person’s bounding box aspect ratio exceeds a certain threshold, a fall is detected.

5. **Alerts:**
   - An audio alarm is played, and a photo is sent to a predefined Telegram chat for immediate action.

## 🌐 Telegram Integration

The project integrates with Telegram to provide instant notifications when a fall is detected.

### Setting Up Telegram Bot

1. **Create a Bot:**
   - Search for `BotFather` in Telegram and follow the instructions to create a new bot.

2. **Get the Token:**
   - Note down the token provided by `BotFather`.

3. **Find Your Chat ID:**
   - Start a chat with your bot and send a message.
   - Visit `https://api.telegram.org/bot<YourBOTToken>/getUpdates` to find your chat ID from the updates.

## 📋 To-Do

- [ ] Enhance fall detection logic with more complex pose analysis.
- [ ] Add support for multiple video sources.
- [ ] Implement a more advanced tracking algorithm.
- [ ] Deploy as a web application for easier access and monitoring.

## 📝 Contributing

Contributions are welcome! Please open an issue or submit a pull request for any changes or additions.

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- **[MediaPipe](https://mediapipe.dev/)** for providing robust pose estimation tools.
- **[Ultralytics](https://ultralytics.com/)** for the YOLOv8 model.
- **[OpenCV](https://opencv.org/)** for computer vision capabilities.

## 📧 Contact

For any queries or suggestions, feel free to reach out via GitHub or email at [saiedhassaan2@gmail.com].
