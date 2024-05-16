# Aircraft_Segmentation
We will perfrom segmentation for aircraft detection by remote sensing on GoogleEarth images

YOLOv8l-seg summary: 401 layers, 45997728 parameters, 45997712 gradients, 221.1 GFLOP


# Quick Start

##Installations


Install the ultralytics package from PyPI

`
pip install ultralytics
`

Install the ultralytics package from GitHub


`

git clone https://github.com/ultralytics/ultralytics
`

Ultralytics yolo commands use the following syntax:


yolo TASK MODE ARGS

    TASK (optional) is one of (detect, segment, classify, pose)
    MODE (required) is one of (train, val, predict, export, track)
    ARGS (optional) are arg=value pairs like imgsz=640 that override defaults.

# Start training from a pretrained *.pt model

`
yolo train data=coco8-seg.yaml model=yolov8l-seg.pt epochs=100 imgsz=640

`



To train for class = aircraft we will specify like this :


`
yolo train data=coco8-seg.yaml model=yolov8l-seg.pt epochs=100 imgsz=640 classes=4
`




Ultralytics YOLOv8.2.16 🚀 Python-3.10.12 torch-2.2.1+cu121 CPU (Intel Xeon 2.20GHz)
engine/trainer: task=segment, mode=train, model=yolov8l-seg.pt, data=coco8-seg.yaml, epochs=100, time=None, patience=100, batch=16, imgsz=640, save=True, save_period=-1




# Predict

Using pre-trained weights
`
yolo predict model=yolov8n-seg.pt source='https://youtu.be/LNwODJXcvt4' imgsz=320
`
Using your own trained weights

`
yolo predict model=./runs/segment/train2/weights/best.pt imgsz=640 conf=0.25
`
