# Comparison of Faster RCNN and Yolov8

1. Take photos of the environment of two or more objects. (at least 100 instances between all objects) 

2. Annotate them on roboflow. 

3. Train a Faster RCNN model using detectron2.

4. Train Yolov8 the smallest size.

5. Evaluate both models based on mAP and speed and size.

# Colab notebook 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ph5e2CnSSzz1PawlEmexuePMeGG2aadh?usp=sharing)

# Take photos of the environment

In this example, I have worked with objects such as a screwdriver and a wrench. Below are examples of data images of two types of objects:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/fox.jpeg" alt="Fox" width="320"/><img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/spoon.jpeg" alt="Spoon" width="320"/>

# Annotation with roboflow

Next, I annotated 100 made objects (50 of each type) using roboflow

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/annotation.png" alt="Annotation" width="1200"/>

# Faster RCNN using detectron2

Based on the official detectron2 and roboflow documentation, I was able to train RCNN using detectron2.

Sample predictions:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/rcnn-preds-1.png" alt="preds" width="320"/><img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/rcnn-preds-2.png" alt="preds" width="320"/>

# Yolov8

Based on the official documentation of yolo and rotoflow, I was able to train the Yolov8 model/

Sample predictions:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/yolo-preds.jpg" alt="preds" width="1200"/>

# Comparison

**Mean Average Precision (mAP)**:
  - Faster RCNN: 84.53%
  - Yolov8: 93.33%

Yolov8 has slightly better mAP than RCNN.

**Speed:**
  - Faster RCNN: training for 24 epochs in 56 minutes
  - Yolov8: training for 24 epochs in 2 minutes

Yolov8 is much faster than RCNN.

**Model size:**
  - Fater RCNN: 719.7 MB
  - Yolov8: 22.5 MB
  
Yolov8 is much smaller than RCNN.


**Thus, Yolov8 better in every way**

# Resources

- https://docs.roboflow.com
- https://blog.roboflow.com/how-to-train-detectron2/
- https://blog.roboflow.com/how-to-train-yolov8-on-a-custom-dataset/
- https://github.com/facebookresearch/detectron2
- https://ultralytics.com/yolov8


