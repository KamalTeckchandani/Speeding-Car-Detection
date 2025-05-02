🚗 **Speeding Car Detection in Video**

This project detects and highlights speeding cars in a video using MATLAB's Computer Vision toolbox.
It uses background subtraction, blob detection, and simple motion tracking to estimate vehicle speed and identify speed violations.

📂 **Project Structure**

Input Video: t1.mp4 (provided by the user)

Main Script: speeding_car_detection.m

Dependencies: MATLAB Computer Vision Toolbox functions (e.g., vision.ForegroundDetector, vision.BlobAnalysis, etc.)

🔥 **Features**

Detects moving vehicles using Gaussian Mixture Model (GMM) background subtraction.

Tracks detected vehicles across frames based on their centroids.

Estimates vehicle speed as displacement per frame (in pixels).

Flags speeding cars:

Green box for normal vehicles.

Red box for vehicles moving faster than a specified threshold.

Displays live annotated video showing detection results.

⚙️ **How It Works**

Video Initialization:
Loads the video file t1.mp4 and extracts frame properties.

Foreground Detection:
A Gaussian Mixture Model separates moving objects (cars) from the static background.

Noise Removal:
Morphological operations (opening) remove noise and small artifacts from the foreground mask.

Object Detection:
Blob analysis identifies vehicle bounding boxes and centroids.

Tracking and Speed Estimation:
Centroids are matched across frames; distance moved is computed to estimate speed.

Speeding Detection:
Cars exceeding the SpeedThreshold (pixels moved per frame) are highlighted in red.

Result Display:
Frames with bounding boxes and speeding information are displayed in real-time.

🛠️ **Requirements**

MATLAB (R2020a or later recommended)

Computer Vision Toolbox

Hardware acceleration enabled for faster video processing (optional but recommended)

🚀 **How to Run**

Place your input video t3.mp4 in the project folder.

Open and run speeding_car_detection.m in MATLAB.

A video player window will open, displaying detection results live.

⚡ **Parameters You Can Adjust**

Parameter	Purpose	Default
SpeedThreshold	Number of pixels moved per frame to classify as speeding	15
NumGaussians	Number of Gaussians in background model	3
MinBlobArea	Minimum detected object size (to ignore small objects)	5% of frame area

📷 **Example Output**

Green Boxes: Normal moving cars.

Red Boxes: Cars identified as speeding.

(Sample images can be added here if you want)

📌 **Notes**

The current speed measurement is in pixels/frame, not real-world units (km/h or mph).

For real-world speed detection, camera calibration and conversion factors would be needed.

Performance depends on frame rate, resolution, and the quality of the input video.

📚 **Future Improvements**
Implement object ID tracking (assign a unique ID to each car).

Improve tracking using Kalman Filters or Optical Flow.

Estimate speed in real-world units using calibration techniques.

Save speeding violations to a report (CSV or video snapshots).

📬 **Contact**

GitHub: (https://github.com/KamalTeckchandani)

LinkedIn: https://www.linkedin.com/in/kamal-teckchandani/

