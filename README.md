🔒 Security Camera Motion Detection with Alarm
=============================================

This is a simple Python project that uses OpenCV to detect motion using a webcam.
When motion is detected, an audible alarm is triggered using the `winsound` module.

📸 Features
-----------
- Real-time motion detection using webcam
- Frame differencing for detecting changes
- Alarm (beep) on detecting motion
- Exit system safely with ESC key

🧰 Requirements
---------------
- Python 3.x  
- OpenCV (`cv2`)  
- winsound (Windows only)

Install OpenCV using:

    pip install opencv-python

🚀 How It Works
---------------
1. Captures two consecutive frames from the webcam
2. Computes the absolute difference between them
3. Converts the difference to grayscale and thresholds it
4. Finds contours in the threshold image
5. If a large enough contour (motion) is detected, it plays a beep sound

▶️ Run the Code
---------------
    python security_cam.py

> Press ESC to exit the camera feed safely.

📝 Notes
--------
- The motion detection sensitivity can be changed by modifying the contour area threshold (5000).
- This code uses winsound, which works only on Windows.
  For Linux/macOS, use alternatives like: os.system('aplay beep.wav')

📂 File Structure
-----------------
    security_cam.py     # Main script for motion detection
    README.md           # Project documentation

📌 Future Improvements
----------------------
- Save detected motion frames as images or video clips
- Add email/SMS alerts
- GUI for better user interaction
- Support for multiple cameras

📄 License
----------
This project is open-source and available under the MIT License.
