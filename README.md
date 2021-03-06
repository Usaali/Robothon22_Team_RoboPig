# Robothon22_Team_RoboPig
This repository is the submission of team RoboPig of FHWS for the Robothon 2022 competition

For a more detailed overview, please take a look at the [pdf version](https://github.com/Usaali/Robothon22_Team_RoboPig/blob/main/Submission%20for%20Robothon%202022.pdf)

## Hardware dependencies
- UR5e robot arm
- Robotiq Hand E Gripper with IO coupling
- 3D printed gripper jaws
- Azure Kinect camera

## Software dependencies
- RoboDK
- Python
  - OpenCV
  - numpy
  - matplotlib
  - pyK4A
  - ur_rtde
  - robodk

## Quick start guide
### 1. Start RoboDK. 
- The software will load the target positions for the robot and set up the socket 
communication. 
- Setup robot communication. 
### 2. Start Python Script for the task board challenge. 
### 3. Choose the order of the tasks by inserting the task numbers in the desired order. 
### 4. Run the script by pressing enter. 
- Rough detection of the board using the camera 
  - Image processing libraries detect the task board in the image and extract corner points in image coordinates. 
  - Calculates the transformation matrices from the actual TCP pose and hand-eye calibration. 
  - Gets a camera to task board transformation with the OpenCV perspective-n-point (PNP) pose algorithm. 
  - Calculates complete transformation matrix from submatrices. 
  - Transforms task board coordinate system to the global base coordinate system. 
- The robot will start the trial by pushing the blue button. 
- Tasks are executed in the desired order. 
- The robot will finish the trial by pushing the red button.
## Submission videos
- The 5 minute video containing a video of our team explaining the solution to the taskboard and a BYOD demo of our robot platform can be found [here](https://cloud.fhws.de/s/XMiiNnsXjnTxfKD)
- The 10 minute video showing our solution doing the Taskboard challenge 5 times can be found [here](https://cloud.fhws.de/s/nXWnQFLCZbzyewY)
