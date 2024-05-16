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

## Train YOLOv8lseg on RSOD dataset of aircraft 

`
!yolo train model=yolov8l-seg.pt data=/content/drive/MyDrive/RSOD/RSOD.yaml epochs=100 imgsz=640
`
