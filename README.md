# Security_Camera_System

Overview

    This repository contains code for a Security Camera System that detects motion using OpenCV in Python. The program captures video frames from a webcam, detects       differences between consecutive frames, and highlights any areas with significant movement by drawing bounding rectangles around them. This system is ideal for       setting up a simple motion-detection-based surveillance system.


Features

	•	Real-time Motion Detection: Continuously captures video feed and detects motion by comparing differences between frames.
	•	Contours and Bounding Boxes: Highlights detected motion areas by drawing bounding boxes.
	•	Adjustable Sensitivity: Contours smaller than a specified area are ignored to reduce false positives from minor changes.
	•	Quit Option: Press q to exit the program.

How It Works

	1.	The camera captures two consecutive frames.
	2.	The absolute difference between the two frames is calculated to detect changes.
	3.	The result is converted to grayscale, blurred, and then thresholded to isolate areas of motion.
	4.	Contours are drawn around significant motion areas, and bounding boxes are created for large movements.

Technologies Used

	•	Python 3.x: Core programming language used for the script.
	•	OpenCV: Library for real-time computer vision tasks.


Getting Started

Prerequisites

Ensure you have Python 3.x and OpenCV installed. Install OpenCV using:
            
    pip install opencv

Installation

	  1.	Clone this repository:
       git clone https://github.com/shivesh-22/security-camera-system.git

    2.	Navigate to the project directory:
       cd security-camera-system

Running the Program

    To start the security camera system, run the following command:
       python main.py


Usage

	•	The system will start capturing video from the default camera (webcam).
	•	Motion detected areas will be highlighted with green bounding boxes.
	•	Press q to quit the program.

Code Structure

	•	main.py: Main script containing the code for capturing video, processing frames, detecting motion, and displaying the video feed with detected areas.

Adjustable Parameters

	•	Contour Area Threshold: Adjust cv2.contourArea(c) < 5000 to filter out smaller movements (e.g., for more sensitivity, lower the threshold value).
