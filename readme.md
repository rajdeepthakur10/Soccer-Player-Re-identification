# Player Re-Identification in Sports Footage
This repository contains the source code and report for the Player Re-Identification Project. The project implements a solution for Re-Identification of soccer players in a Single Feed.

# Overview
This project uses the YOLOv11 object detection model to detect players and the ByteTrack algorithm for robust multi-object tracking and re-identification. The solution processes the 15sec_input_720p.mp4 video to assign and maintain a consistent player_id for each player, even when they are occluded or temporarily leave the camera's view.

The primary implementation is contained within the stealthMode_yolov11_bytetrack.ipynb Jupyter Notebook.

# Note: This notebook is designed to run in Google Colab with GPU acceleration. If running locally, ensure your CUDA environment is properly set up.

# 🛠️ Setup & Installation
1. # Dependencies

To run this project, you need Python and the libraries listed below. It is highly recommended to create a virtual environment to manage these dependencies.

Create a requirements.txt file with the following content:

Plaintext
ultralytics
supervision==0.25.1
inference-gpu
git+https://github.com/roboflow/sports.git
opencv-python
numpy
Install the dependencies using pip:

Bash
pip install -r requirements.txt
Note: This notebook was developed and tested in a Google Colab environment with GPU acceleration. If running locally, ensure you have a compatible CUDA environment for GPU support.

2. # Required Files

Before running the code, make sure you have the following files in the root directory of the project:

Model: best.pt (the provided YOLOv11 object detection model)

Video: 15sec_input_720p.mp4 (the input video for tracking)

Of course. Here is the revised "How to Run" section, updated for a Google Drive submission and recommending Google Colab.

# How to Run
This project is best run in a Google Colab environment to take advantage of the free GPU and pre-configured setup.

1. # Download the Project Folder
Download and unzip the entire project folder from the shared Google Drive link.

2. # Upload to Your Google Drive
Upload the complete, unzipped project folder (containing stealthMode_yolov11_bytetrack.ipynb, best.pt, etc.) to your own Google Drive.

3. # Open in Google Colab
Navigate to the folder in your Google Drive, right-click on the stealthMode_yolov11_bytetrack.ipynb file, and select Open with > Google Colaboratory.

4. # Execute the Notebook
Once the notebook is open in Colab, run all the cells by navigating to Runtime > Run all. The notebook is self-contained and will perform the following steps automatically:

    Install all necessary dependencies.

    Download the required video file (15sec_input_720p.mp4).

    Load the YOLOv11 model.

    Process the video frame by frame, applying the ByteTrack algorithm.

    Generate an annotated output video named output.mp4 in the same Google Drive folder.


