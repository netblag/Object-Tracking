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

![demo ](https://imgur.com/IKVnYWK)
