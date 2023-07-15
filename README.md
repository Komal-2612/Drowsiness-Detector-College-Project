# Data Set  http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2
# Drowsiness Detection using Eye Aspect Ratio (EAR)

This code implements a drowsiness detection system using the Eye Aspect Ratio (EAR) metric. It uses computer vision libraries such as OpenCV, dlib, and SciPy.

## Prerequisites

Before running the code, make sure you have the following prerequisites:

- Python 3.x installed on your system.
- The following libraries installed:
  - cv2 (OpenCV)
  - dlib
  - scipy

You can install the necessary libraries by running the following command:

```
pip install opencv-python dlib scipy
```

Additionally, you need to download the "shape_predictor_68_face_landmarks.dat" file, which is the pre-trained facial landmark detection model used by dlib. You can download it from the following link:
- [shape_predictor_68_face_landmarks.dat](https://github.com/davisking/dlib-models/blob/master/shape_predictor_68_face_landmarks.dat.bz2)

## How to Run

1. Ensure that your webcam is connected to your computer.
2. Save the code to a file, e.g., `drowsiness_detection.py`.
3. Place the `shape_predictor_68_face_landmarks.dat` file in the same directory as the Python script.
4. Open a terminal or command prompt and navigate to the directory containing the script.
5. Run the script using the following command:

```
python drowsiness_detection.py
```

6. A new window will open showing the webcam feed with drowsiness detection. If the eyes are detected as drowsy (EAR < 0.26), the text "DROWSY" will be displayed on the frame.
7. To exit the application, press the 'Esc' key.

## Notes

- The code uses the Eye Aspect Ratio (EAR) to detect drowsiness. It calculates EAR based on the positions of landmarks detected on the eyes.
- The `calculate_EAR` function calculates the EAR using the Euclidean distance function from the SciPy library.
- The code uses the dlib library to detect faces and landmarks on the face. It requires the "shape_predictor_68_face_landmarks.dat" file for facial landmark detection.
- The code uses OpenCV (cv2) library for video capture and display.
- Make sure your environment has the necessary libraries installed and the correct versions to avoid any potential compatibility issues.
