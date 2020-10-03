[![DeepSource](https://deepsource.io/gh/Rajatkhatri7/Face-With-Yolo.svg/?label=active+issues&show_trend=true)](https://deepsource.io/gh/Rajatkhatri7/Face-With-Yolo/?ref=repository-badge)

[![DeepSource](https://deepsource.io/gh/Rajatkhatri7/Face-With-Yolo.svg/?label=resolved+issues&show_trend=true)](https://deepsource.io/gh/Rajatkhatri7/Face-With-Yolo/?ref=repository-badge)
# Face-With-Yolo

Yolov3 is an algorithm that uses deep convolutional neural networks to perform object detection. This repository implements Yolov3 using TensorFlow 2.0

![image](https://github.com/Rajatkhatri7/Face-With-Yolo/blob/master/detections/download.png)

## Getting started

#### Pip
```bash
# TensorFlow CPU
pip install -r requirements.txt
```

### Downloading official pretrained weights(optional)
For Linux: Download official yolov3 weights pretrained on COCO dataset. if you want to run it on pretrained weights 

```
# yolov3
wget https://pjreddie.com/media/files/yolov3.weights -O weights/yolov3.weights

# yolov3-tiny
wget https://pjreddie.com/media/files/yolov3-tiny.weights -O weights/yolov3-tiny.weights

```

For Windows:
You can download the yolov3 weights by clicking [here](https://pjreddie.com/media/files/yolov3.weights) and yolov3-tiny [here](https://pjreddie.com/media/files/yolov3-tiny.weights) then save them to the weights folder.

### Using Custom trained weights
Add your custom weights file to weights folder and your custom .names file into data/labels folder.
[Click here](https://drive.google.com/file/d/1-7VwHN6bBbcQ9CZTQzDLSDGCL6MJkDus/view?usp=drivesdk) to download Custom weights which i trained on face dataset.
  
### Saving your yolov3 weights as a TensorFlow model.
Load the weights using `load_weights.py` script. This will convert the yolov3 weights into TensorFlow .ckpt model files!

```
# yolov3
python load_weights.py

# yolov3-tiny
python load_weights.py --weights ./weights/yolov3-tiny.weights --output ./weights/yolov3-tiny.tf --tiny
```

After executing one of the above lines, you should see .tf files in your weights folder.

## Running the TensorFlow model
The tensorflow model can  be run through using `detect.py` script. 

Don't forget to set the IoU (Intersection over Union) and Confidence Thresholds within your yolov3-tf2/models.py file

### Usage examples

Let's run an example or two using sample images found within the data/images folder. 

```bash
# yolov3
python detect.py --images "data/images/dog.jpg, data/images/office.jpg"

# yolov3-tiny
python detect.py --weights ./weights/yolov3-tiny.tf --tiny --images "data/images/dog.jpg"

# webcam
python detect_video.py --video 0

# video file
python detect_video.py --video data/video/paris.mp4 --weights ./weights/yolov3-tiny.tf --tiny

# video file with output saved (can save webcam like this too)
python detect_video.py --video path_to_file.mp4 --output ./detections/output.avi
```
Then you can find the detections in the `detections` folder.

=======










```











```






  






























 




  


.

