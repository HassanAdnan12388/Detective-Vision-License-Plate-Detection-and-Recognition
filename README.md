# Detective-Vision-License-Plate-Detection-and-Recognition
Detective Vision: License Plate Detection and Recognition

# Overview
This project focuses on real-time vehicle identification by detecting license plates and recognizing the characters on them using computer vision techniques. The system leverages state-of-the-art models, including #SuperPoint# and #SuperGlue#, to detect and match keypoints between the license plate and a reference image. The project uses a custom-built pipeline to project images onto video feeds and identify license plate numbers.

# Part 1: Implement a real-time system to detect license plates from video frames using the #YOLOv8# model.
Process video frames to detect vehicles, extract license plate regions, and project a reference image onto the detected plate area.
Handle video input, process frames, and display processed frames with the projected image.

# Part 2: Character Recognition 
Utilize a pre-trained #CNN-based# model to recognize characters from the detected license plates.
Extract keypoints using #SuperPoint# and match them to the reference image with #SuperGlue#.
Display the recognized characters on the projected license plate area in real-time.

# Part 3: Real-Time Performance Optimization (30 Marks)
Optimize the system for real-time performance, ensuring the video processing speed is fast enough to handle continuous input.
Implement frame-by-frame processing with efficient image handling and keypoint matching for reduced latency.
Test and validate the system’s performance in various scenarios with different lighting conditions and license plate types.

# Model Architecture
## YOLOv8# License Plate Detection
The #YOLOv8# model is used for vehicle and license plate detection.
Pre-trained weights are used for the detection task.
The model outputs bounding boxes around detected license plates.
## SuperPoint# and #SuperGlue# for Keypoint Matching
#SuperPoint# is used to extract keypoints from both the detected license plates and the reference images.
#SuperGlue# matches keypoints between the images to establish the correspondence for the projection.
Projection Pipeline
The keypoints are used to find the homography between the detected license plate and the reference image.
The reference image is then warped and projected onto the detected license plate in the video frame.
The projection is updated in real-time as the video plays.

# Technologies Used

## Python#: Programming language used for implementing the entire system.
## YOLOv8#: Object detection model used for detecting vehicles and license plates.
## SuperPoint#: Pre-trained model used for keypoint extraction from images.
## SuperGlue#: Used for matching keypoints between the detected license plate and reference image.
## OpenCV#: Computer vision library used for video processing, image manipulation, and keypoint matching.
## PyTorch#: Framework for model implementation and inference.
