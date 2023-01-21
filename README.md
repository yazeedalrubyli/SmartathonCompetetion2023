# SmartathonCompetetion2023

## Overview
In this project, a stat-of-the-art detection algorithm is used to detect objects that cause visual pollution in Saudi Arabia. The real-time object detection system that has been used is YOLO (You only look once) version 7. The objects that the model has been trained to look for are the following:
- Graffiti
- Faded signage
- Potholes
- Garbage
- Construction road
- Broken signage
- Bad streetlight
- Bad billboard
- Sand on road
- Clutter sidewalk
- Unkept facade

## Contribution
One of the main issues is the severe unbalanced in the data. In order to get good detection at least 1000 image is available for every object. Further, Object[Garbage] has the highest number of occurrences at around 8000 times. On the other hand, Object[bad streetlight] has only one occurrence. A proposed solution was to collect more images from the classes under 1000 occurrences and try to reach that number. Unfortunately, no time was available in our budget to collect images for the severely affected labels. Image dimensions are one of the challenges that first faced during the initial investigation of the data because the dimensions were different. The problem has been solved by doubling the dimension of the (xmin,ymin, xmax, ymin). Another challenge was to convert from/to yolo format without messing things up. Such a solution can be scalable by building a pipeline with containerization, orchestration, and distribution where images are fed to the algorithm to increase its performance over time without consuming further resources.

## Further Development
The training was slow due to the lack of time and resources. Only one GPU was used via Colab. Further, hyperparameters can be modified to best fit the problem at hand.

## Credits
- Yolov7 by WongKinYiu (https://github.com/WongKinYiu/yolov7)
