<div align="center">

  # Hybrid-Anchor Rotation Detector for Oriented Object Detection
</div>

![image](https://github.com/HiImKing1509/Hybrid-Anchor-Rotation-Detector/blob/master/images/hardet_architecture.png)

## Introduction

Oriented object detection in aerial images involves identifying objects with varying sizes and orientations, gaining significant attention in computer vision and pattern recognition. Current state-of-the-art detectors use either two-stage or one-stage approaches and commonly adopt Anchor-based strategies. These methods require a redundant number of generated anchors for training and could be inefficient for the limited computational resources. In contrast, Anchor-free mechanisms are faster processing times by eliminating the need for anchor-related hyperparameters. However, they significantly diminish the number of training samples, excoriating the detection accuracy. To address these limitations, we present a **Hybrid-Anchor Rotation Detector (HA-RDet)** that combines the advantages of both anchor-based and anchor-free schemes for oriented object detection. Our approach utilizes only one preset anchor for each location on the feature maps and refines these anchors using our introduced Orientation-Aware Convolution technique, significantly boosting the detection performance of HA-RDet. We extensively evaluate HA-RDet with ResNet50 on challenging benchmarks and achieve competitive accuracies, such as DOTA-v1 (75.41% mAP), DIOR-R (65.3% mAP), and HRSC2016 (90.2% mAP) against current anchor-based methods while utilizing fewer training resources. We hope our baseline could establish a foundation for further advancements in oriented object detection.

## Installation

## Benchmark and Model Zoo

### DOTA dataset

| Model    |    Backbone       | #anchors              | VRAM (GB) | #params                   | FPS | mAP | Config | Download |
| ------ |:-------------:|:----------------------:|:-----------------------------------------------------:|:-------------------------:|:----:|:----:|:---:|:--:|
| S2A-Net| ResNet50+FPN | 1 | 4.6 | ~39M | 15.5 | 74.19 | - | - |
| Oriented R-CNN| ResNet50+FPN | 20 | 14.2 | ~41M | 13.5 | 75.69 | - | - |
| **HA-RDet (our)** | ResNet50+FPN | 1 | 6.8 | ~56M | 12.1 | 75.41 | <a href="https://github.com/HiImKing1509/Hybrid-Anchor-Rotation-Detector/blob/master/configs/ha_rdet/hardet_baseline_r50_fpn_1x_dota_le90.py">config</a> | <a href="https://drive.google.com/file/d/1_8xUpm8dX5oypkBCiDuqYolG2u3_KuYW/view?usp=drive_link">model</a> / <a href="https://github.com/HiImKing1509/Hybrid-Anchor-Rotation-Detector/blob/master/logs/hardet_baseline_r50_fpn_1x_dota_le90.txt">log</a> |
| **HA-RDet (our)** | ResNet101+FPN | 1 | - | - | - | 76.02 | <a href="https://github.com/HiImKing1509/Hybrid-Anchor-Rotation-Detector/blob/master/configs/ha_rdet/hardet_baseline_r101_fpn_1x_dota_le90.py">config</a> | <a href="https://drive.google.com/file/d/1Zm7eYrepwAmjJ0TaHti4d6Znn9T4bl__/view?usp=drive_link">model</a> / <a href="https://github.com/HiImKing1509/Hybrid-Anchor-Rotation-Detector/blob/master/logs/hardet_baseline_r101_fpn_1x_dota_le90.txt">log</a> |
| **HA-RDet (our)** | ResNeXt101_DCNv2+FPN | 1 | - | - | - | 77.012 | <a href="https://github.com/HiImKing1509/Hybrid-Anchor-Rotation-Detector/blob/master/configs/ha_rdet/hardet_baseline_rx101_dcn_fpn_1x_dota_le90.py">config</a> | <a href="https://drive.google.com/file/d/1_29jCteJpW-13MxClbZP7eHuRY9HJPTH/view?usp=drive_link">model</a> / <a href="https://github.com/HiImKing1509/Hybrid-Anchor-Rotation-Detector/blob/master/logs/hardet_baseline_rx101_dcn_fpn_1x_dota_le90.txt">log</a> |

### HRSC2016
### DIOR-R