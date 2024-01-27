# Object-Tracking
This Python script uses OpenCV's CamShift algorithm for real-time object tracking in a video stream. Users interactively select an object by defining a bounding box through mouse clicks. The program continuously tracks and highlights the chosen object, offering a straightforward and interactive tracking experience.

## Dependencies
- [OpenCV (cv2)](https://opencv.org/)
- [NumPy (np)](https://numpy.org/)

Make sure to install these dependencies using the following:
```bash
pip install opencv-python numpy
```

## Instructions

1. Run the script, and it will open a window named 'Result'.

2. To select the object to track, click the left mouse button twice. The first click sets the initial point (x, y), and the second  click sets the opposite corner of the bounding box (x+w, y+h).

3. Once the object is selected, the tracker initializes, and you can see the bounding box following the object in the video stream.



## Controls

.Left-click to select the object.
.Right-click to cancel the selection.
.Press 'q' to exit the application.


## Code Explanation

* The program initializes a video capture object (cap) to capture video     from the default camera (cv2.VideoCapture(0)).
* It uses a named window called 'Result' to display the output.
* Mouse events are handled using the cv2.setMouseCallback function. Left-clicking sets the initial and final points of the bounding box, and right-clicking cancels the selection.
* The initialize function is responsible for setting up the Region of Interest (ROI) for tracking using the CamShift algorithm.
* The main loop continuously reads frames from the video stream, converts them to HSV format, and performs object tracking using    the CamShift algorithm.
* The tracked object's bounding box is drawn on the frame using cv2.polylines.
* Pressing `q` terminates the program.


## Notes

Ensure your camera is working and accessible.
The program may need adjustments based on your specific use case and the characteristics of the objects you want to track.

![demo ](https://private-user-images.githubusercontent.com/143696916/300198279-81e5276d-fe24-4cbb-bf05-e8a146a16e41.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDYzNzg2NDYsIm5iZiI6MTcwNjM3ODM0NiwicGF0aCI6Ii8xNDM2OTY5MTYvMzAwMTk4Mjc5LTgxZTUyNzZkLWZlMjQtNGNiYi1iZjA1LWU4YTE0NmExNmU0MS5naWY_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMTI3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDEyN1QxNzU5MDZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02OTY2NjNmZDhkYmVkMjVmZjg2YThiZDhiODI2Y2QwMzczMTg2NjRlZTJkMjQyMDBjZjdmMTM2NmMyYjJlMGEzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.7htuS_kaX0LM_LV9fhO-8EBcUvi-Osw226OuyA8xSts)
