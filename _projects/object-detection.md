---
layout: project
title: "Object Detection for Vietnamese Traffic Signs"
subtitle: "Faster R-CNN, YOLOv12, FCOS, RetinaNet, and SSD300"
selected: "y"
order: 1
github: ""
---

A comparison of one-stage and two-stage detectors fine-tuned on the Vietnamese Traffic
Signs dataset. Traffic signs are a demanding target: the objects are small relative to the
frame, and several classes differ only in their pictogram.

**Models.** Pre-trained Faster R-CNN, YOLOv12, FCOS, RetinaNet, and SSD300, each fine-tuned
on the same data for a like-for-like comparison.

**Dataset.** Bounding boxes and class targets were labeled by hand for signage in the
Ho Chi Minh City context, and the annotated dataset was published on Kaggle.
