# YOLOv9-POSE

This repository takes the Human Pose Estimation model from the YOLOv9 model as implemented in YOLOv9's official documentation.
Implementation of paper - [YOLOv9: Learning What You Want to Learn Using Programmable Gradient Information](https://arxiv.org/abs/2402.13616)


## Performance 

MS COCO

| Model | Test Size | AP<sup>val</sup> | AP<sub>50</sub><sup>val</sup> | AP<sub>75</sub><sup>val</sup> | Param. | FLOPs |
| :-- | :-: | :-: | :-: | :-: | :-: | :-: |
| [**YOLOv9-POSE-T**]() | 640 | **%** | **%** | **%** | **M** | **G** |
| [**YOLOv9-POSE-S**]() | 640 | **%** | **%** | **%** | **M** | **G** |
| [**YOLOv9-POSE-M**]() | 640 | **%** | **%** | **%** | **M** | **G** |
| [**YOLOv9-POSE-C**]() | 640 | **%** | **%** | **%** | **M** | **G** |
| [**YOLOv9-POSE-E**]() | 640 | **%** | **%** | **%** | **M** | **G** |

## Prerequisites
* Python >= 3.8
* Pytorch >= 1.7.0

## Usage

Setup Conda Environment
``` shell
$ conda create --name yolov9 python=3.8
$ conda activate yolov9
```
Clone Repository(Unofficial / branch name: [yolo9u](https://github.com/WongKinYiu/yolov9/tree/yolov9u)
``` shell
$ git clone https://github.com/WongKinYiu/yolov9.git@yolov9u
```
Download Ultralytics
``` shell
$ pip install ultralytic==8.1.23
$ pip install torch==1.13.0 torchvision==0.14.0 torchaudio==0.13.0
```
Training
``` shell
$ yolo pose train data=coco-pose.yaml model=yolov9-pose.yaml epochs=100 imgsz=640
```
Validation
``` shell
yolo pose val model=path/to/best.pt  # val custom model
```
Predict
``` shell
yolo pose predict model=path/to/best.pt source='https://ultralytics.com/images/bus.jpg'
```

## Reference

* [https://github.com/WongKinYiu/yolov9](https://github.com/WongKinYiu/yolov9)


