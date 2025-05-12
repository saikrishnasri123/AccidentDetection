# AccidentDetection
# Crash Detection System Using CCTV and YOLOv3

This project implements a real-time crash detection system using CCTV footage and the YOLOv3 object detection model. It analyzes video streams to identify potential accidents involving vehicles and raises alerts.

## 📌 Features

- Object detection using YOLOv3 (pre-trained on COCO dataset)
- Crash detection based on vehicle proximity and overlap
- Alert notification via GUI (Tkinter message box)
- Saves crash frames and logs for analysis
- Modular structure with optional post-analysis tools

## 🔧 Requirements

- Python 3.x
- OpenCV (`opencv-python`)
- NumPy
- Imutils
- Tkinter (comes with standard Python)
- YOLOv3 weights and configuration files

## 📁 Directory Structure

project/
│
├── cctv_video.py # Main detection script
├── coco.names # COCO class labels
├── yolov3.cfg # YOLOv3 config file
├── yolov3.weights # YOLOv3 pre-trained weights
├── wwd_analysis.py # Optional analysis tool
├── playCrash.py # Optional crash image viewer
├── PlayVideo.py # Optional result video player
└── output/ # Contains saved crash frames and processed frames


## 🚀 Usage

### Step 1: Download YOLOv3 Files

Download the following files and place them in the `yolo-coco/` directory:

- [`yolov3.weights`](https://pjreddie.com/media/files/yolov3.weights)
- [`yolov3.cfg`](https://github.com/pjreddie/darknet/blob/master/cfg/yolov3.cfg)
- [`coco.names`](https://github.com/pjreddie/darknet/blob/master/data/coco.names)

### Step 2: Run Detection

```bash
python cctv_video.py --input your_video.mp4 --yolo yolo-coco
