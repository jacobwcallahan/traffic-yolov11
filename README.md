
# Smart Traffic Signal System using YOLOv11

This project implements an intelligent traffic signal system using YOLOv11 for real-time vehicle detection and traffic density estimation. It dynamically adjusts traffic light durations based on lane-wise congestion detected from video feeds.

---

##  Project Overview

Traffic congestion in urban cities is often worsened by static signal systems. This project leverages the YOLOv11 deep learning model to monitor traffic density and optimize signal timings accordingly.

The system:
- Uses real-time video input from traffic cameras
- Detects and counts vehicles per lane using YOLOv11
- Adjusts signal durations to prioritize more congested lanes
- Can be deployed on both edge devices and cloud servers


##  Model Overview: YOLOv11

YOLOv11 is an advanced real-time object detection model with the following benefits:
- Enhanced backbone and neck for feature extraction
- 22% fewer parameters than YOLOv8
- Supports object detection, segmentation, classification, and oriented bounding boxes (OBB)


##  Project Objectives

1. **Model Selection and Evaluation**
   - Choose YOLOv11 for speed and accuracy.
2. **Data Collection and Preprocessing**
   - Extract and annotate traffic frames from video data.
3. **Model Fine-Tuning**
   - Apply transfer learning for urban traffic datasets.
4. **Density Estimation**
   - Count vehicles lane-wise and estimate congestion.
5. **Signal Control Logic**
   - Adjust green/red time dynamically based on congestion.
6. **Deployment**
   - Export model for deployment on edge/cloud.


##  Installation

### 1. Clone the Repository

```bash
git clone https://github.com/jacobwcallahan/traffic-yolov11.git
cd traffic-yolov11
```

###  Set Up Environment

We recommend Python 3.8+.

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

###  Dependencies

- Python 3.8+
- PyTorch
- OpenCV
- NumPy
- Matplotlib
- Pandas
- Seaborn
- tqdm
- ultralytics (for YOLOv11, if installed via pip)


##  Running the Code

```bash
python main.py
```

Or run the Jupyter notebook:

```bash
jupyter notebook MLProject_Final.ipynb
```

##  Evaluation

- Learning curves (train/val loss)
- Confusion matrix
- Precision, Recall, F1-Score
- ROC Curve
- Inference Time and FPS


##  Future Improvements

- Incorporate vehicle type weighting (e.g., prioritize buses over bikes)
- Use real-time camera feeds with socket streaming
- Integrate with smart city APIs (like Google Maps or traffic sensors)

## Sample Videos
- One sample video is provided in the folder titled "sample_video.mp4"


# Implementing the model

- Run the ML_Project_Inference_only.ipynb file
- They use the weights "best.pt" which is obtained from training the model. 
- Change the variable "input_path" in the file, this is currently set to a sample video "sample_video.mp4"
- This outputs a video with the model applied to it. It defaults to traffic_density_analysis_roi_cropped.mp4
- 
