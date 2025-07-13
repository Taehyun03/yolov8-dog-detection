{\rtf1\ansi\ansicpg949\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # YOLOv8 Dog Detection\
\
This repository contains a YOLOv8-based object detection model trained to detect dogs using a custom-labeled dataset.\
\
## Project Structure\
\
```\
\uc0\u9500 \u9472 \u9472  train/             # Training images and labels\
\uc0\u9500 \u9472 \u9472  val/               # Validation images and labels\
\uc0\u9500 \u9472 \u9472  data.yaml          # YOLOv8 dataset configuration\
\uc0\u9500 \u9472 \u9472  README.dataset.txt\
\uc0\u9500 \u9472 \u9472  README.roboflow.txt\
\uc0\u9500 \u9472 \u9472  best.pt            # (optional) Trained YOLOv8 model weights\
```\
\
## Dataset\
\
- Labeled using Roboflow\
- Total images: **100**\
- Classes: **dog** (1 class)\
\
## Model Info\
\
- **Model Used**: YOLOv8n (Nano)\
- **Training Epochs**: 50\
- **Image Size**: 640x640\
- **Precision**: 99.7%\
- **Recall**: 100%\
- **mAP@0.5**: 99.5%\
- **mAP@0.5:0.95**: 75.8%\
\
## How to Train (Colab)\
\
```python\
from ultralytics import YOLO\
\
model = YOLO("yolov8n.pt")\
model.train(\
    data="data.yaml",\
    epochs=50,\
    imgsz=640,\
    batch=8\
)\
```\
\
## Result Preview\
\
- Output saved to `runs/detect/train2`\
- Inference results available after training\
- Example prediction images can be added here later\
\
## \uc0\u9997 \u65039  Author\
\
- Name: **\uc0\u44608 \u53468 \u54788 **\
- School: **\uc0\u44221 \u49345 \u44397 \u47549 \u45824 \u54617 \u44368  \u49548 \u54532 \u53944 \u50920 \u50612 \u44277 \u54617 \u44284 **\
- Project: **\uc0\u51064 \u48292 \u53668  \u47700 \u51060 \u52964 \u53668  \u44284 \u51228  2, 3 \u49688 \u54665 \u50857 **\
}