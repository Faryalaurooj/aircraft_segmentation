# aircraft_segmentation
We will perfrom segmentation for aircraft detection by remote sensing on GoogleEarth images

# Quick Start
##Installations
Install the ultralytics package from PyPI

`
pip install ultralytics
`
Install the ultralytics package from GitHub


`pip install git+https://github.com/ultralytics/ultralytics.git@main
`
Ultralytics yolo commands use the following syntax:

yolo TASK MODE ARGS

    TASK (optional) is one of (detect, segment, classify, pose)
    MODE (required) is one of (train, val, predict, export, track)
    ARGS (optional) are arg=value pairs like imgsz=640 that override defaults.

# Start training from a pretrained *.pt model

`
yolo train data=coco8-seg.yaml model=yolov8l-seg.pt epochs=100 imgsz=640


# Predict

Using pre-trained weights
`
yolo predict model=yolov8n-seg.pt source='https://youtu.be/LNwODJXcvt4' imgsz=320
`
Using your own trained weights

`
yolo predict model=./runs/segment/train2/weights/best.pt imgsz=640 conf=0.25
`
