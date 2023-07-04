<div align="center">

  # Hybrid-Anchor Rotation Detector for Oriented Object Detection
</div>

![image](https://github.com/HiImKing1509/Hybrid-Anchor-Rotation-Detector/assets/84212036/135e3707-f2bb-455b-bd83-857cdde06336)

## Introduction

Oriented object detection in aerial images involves identifying objects with varying sizes and orientations, gaining significant attention in computer vision and pattern recognition. Current state-of-the-art detectors use either two-stage or one-stage approaches and commonly adopt Anchor-based strategies. These methods require a redundant number of generated anchors for training and could be inefficient for the limited computational resources. In contrast, Anchor-free mechanisms are faster processing times by eliminating the need for anchor-related hyperparameters. However, they significantly diminish the number of training samples, excoriating the detection accuracy. To address these limitations, we present a **Hybrid-Anchor Rotation Detector (HA-RDet)** that combines the advantages of both anchor-based and anchor-free schemes for oriented object detection. Our approach utilizes only one preset anchor for each location on the feature maps and refines these anchors using our introduced Orientation-Aware Convolution technique, significantly boosting the detection performance of HA-RDet. We extensively evaluate HA-RDet with ResNet50 on challenging benchmarks and achieve competitive accuracies, such as DOTA-v1 (75.41% mAP), DIOR-R (65.3% mAP), and HRSC2016 (90.2% mAP) against current anchor-based methods while utilizing fewer training resources. We hope our baseline could establish a foundation for further advancements in oriented object detection.

## Benchmark and Model Zoo

### DOTA dataset

| Model    |    Backbone       | #anchors              | VRAM (GB) | #params                   | FPS | mAP | Config | Download |
| ------ |:-------------:|:----------------------:|:-----------------------------------------------------:|:-------------------------:|:----:|:----:|:---:|:--:|
| S2A-Net| ResNet50+FPN | 1 | 4.6 | ~39M | 15.5 | 74.19 | - | - |
| Oriented R-CNN| ResNet50+FPN | 20 | 14.2 | ~41M | 13.5 | 75.69 | - | - |
| **HA-RDet (our)** | ResNet50+FPN | 1 | 6.8 | ~56M | 12.1 | 75.41 | - | - |
| **HA-RDet (our)** | ResNet101+FPN | 1 | - | - | - | 76.02 | - | - |
| **HA-RDet (our)** | ResNeXt101_DCNv2+FPN | 1 | - | - | - | 77.012 | - | - |
