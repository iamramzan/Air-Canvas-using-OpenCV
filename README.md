## Air-Canvas-using-OpenCV

Ever wished to capture your imagination by simply waving your finger in the air?
In this post, we introduce Air Canvas—a virtual drawing tool that lets you sketch in the air using only your hand gestures. By leveraging the powerful capabilities of OpenCV and MediaPipe, this computer vision project tracks hand landmarks to create a seamless drawing experience.

## 🔧 Tools and Libraries Used

- Python 3: For scripting and project development.
- NumPy: To manage and manipulate data arrays efficiently.
- OpenCV: This open-source library is a cornerstone for real-time computer vision. It facilitates video frame capture and processing seamlessly.
- MediaPipe: Google’s framework for multimodal machine learning pipelines. In this project, MediaPipe powers real-time hand tracking and landmark detection.

## 💡 How It Works

- Capture Video: OpenCV captures a live video feed from the webcam.

- Process Frames: Each frame is analyzed using MediaPipe to detect and track hand landmarks in real time.

Draw Landmarks: The detected hand landmarks serve as pointers, allowing users to draw virtually by moving their hands in the air.

## 🧩 Algorithm Overview

- Frame Capture: Begin reading video frames from the webcam. Convert these frames to HSV color space, as it simplifies color detection.

- Canvas Setup: Create a canvas frame and overlay ink buttons to enable drawing functionalities.

- Hand Detection: Configure MediaPipe to detect a single hand by adjusting detection parameters.

- Landmark Identification: Pass RGB frames to MediaPipe's hand detector to locate key landmarks.

- Track Finger Movements: Detect the forefinger coordinates and continuously store them in an array across successive frames.

- Render Drawings: Use the stored coordinates to draw points on the canvas and video frames, creating the visual output of your air-drawn masterpiece.
