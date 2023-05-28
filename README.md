# Config4

This specific configuration consists of a Raspberry Pi 4 with the Pi Camera Module v3. The Raspberry Pi 4 serves as the platform for image processing. This is quite similar to config 2, but without the TPU.

In this configuration, OpenCV Classic is employed with an emphasis on color detection for image processing. Color detection is a fundamental technique in computer vision that allows for the identification and tracking of objects based on their specific color signatures.
This image processing technique does computation on the pixels from the camera, and therefor require less computational power from the CPU as a trained Tensorflow/YOLO model would. And is therefore the reason why we are running OpenCV Classic on this configuration, due to no TPU.

## Table of Contents
- [Software Reasoning](#Software-Reasoning)
- [References](#references)


## Software Reasoning

### OpenCV

We have not tried other alternatives to OpenCV due how well it works. OpenCV is a very well documented library, and is very easy to use. It is also very fast, and can run on the Raspberry Pi 4 without any problems. OpenCV is also very well supported by the ROS2 community, and therefor it is easy to integrate with ROS2.

### ROS2

ROS2 was chosen due to wishes from our customer, and because it is a very well documented and supported framework. ROS2 is also very easy to use, and is very well supported by the community. ROS2 is also easy to integrate with OpenCV, and is therefor a good choice for this configuration.

### cvzone

cvzone is a helper library for OpenCV. We chose to use this library due to how easy it made it to draw bounding boxes around the objects we detected. It also made it simpler to draw text on the screen, and to draw the FPS counter. It is also very well documented, and is easy to use.

### Python

We chose to use Python due to how easy it is to use, and how well it works with OpenCV and ROS2.


## References

- [OpenCV](https://opencv.org/)
- [ROS2](https://docs.ros.org/en/humble/index.html)
- [cvzone](https://github.com/cvzone/cvzone)
- [VS Code](https://code.visualstudio.com/)
