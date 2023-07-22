# YOLO & ByteTracker - Vehicle counting
#### Video
The [video](https://www.youtube.com/watch?v=MNn9qKG2UFI) was downloaded from Youtube. It is 5:06 minutes long

and it shows vehicle passing on a traffic. The video was downloaded in 720p resoultion.

#### Model

The code for model creation was heavily inspired by the [code](https://colab.research.google.com/github/roboflow-ai/notebooks/blob/main/notebooks/how-to-track-and-count-vehicles-with-yolov8.ipynb) created by Roboflow. It utilizes YOLOv8 model, which is used for object detection on images.

It also uses ByteTrack, which enables following an object throught all frames of the video.

We can use the first frame of the video to help us put start and end points of the line on the optimal coordinates.
![output](https://github.com/mato-m/yolo-vehicle-counting/assets/64593617/2e286aba-762c-4559-ab9a-f868760154f8)
___

The model then processes every frame of the video and tracks to see if any tracked object had passed
through the given line. The model can use multiple lines and track objects passing from both directions.

We can also set the classes of objects detected by YOLOv8 model that we want to track. In this example,

we only track objects that are vehicles - like cars, trucks and motorcycles.

The following video represents first 10 seconds of final result.

https://github.com/mato-m/yolo-car-tracking/assets/64593617/8ab0ca3a-2e07-4fe2-988c-93b266c641a6

