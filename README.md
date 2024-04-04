# ROS with OpenCV

- The publisher/subscriber and OpenCV portion is based on this [ROS tutorial](http://wiki.ros.org/cv_bridge/Tutorials/ConvertingBetweenROSImagesAndOpenCVImagesPython)

## Prerequisites
- Install Ubuntu in Virtual Machine or Dual boot (Ubuntu 20 preferred)
- Install ROS (ROS Noetic preferred)

## Cloning the repo
Go to home directory if you're not already there
```
cd ~
```
Run following commands
```
git clone https://github.com/myatnoeoo6612/ROS-openCV_Package.git
```

## Building tutorial package
Sourcing setup file lets your computer know where your project files are
```
cd ~/ros_openCV_ws/
catkin_make
source ~/ros_openCV_ws/devel/setup.bash
```
## Check the Camera Device
```
ls /dev/ | grep video
```
## Change the Camera device in the "camera_publisher.py"
```
videoCaptureObject = cv2.VideoCapture(?) <= change in here  
```
Save the file.

## Launch the files
```
source ~/ros_openCV_ws/devel/setup.bash
roscore
roslaunch ros_opencv camera_myat.launch
```
