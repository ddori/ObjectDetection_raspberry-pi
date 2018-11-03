# ObjectDetection_raspberry-pi
for raspberrypi
You can use RaspberryPi ObjectDetection Project

#Develop enviroment
<Collect Image & Test Device>
1. Raspberry pi (model B+)
2. Picamera

<Train>
OS  :Ubuntu 18.0.4 
CPU : 17-5930K
RAM : 32G
GC  : 1080 GTX * 3


#Requriement
1. openCV 3.4.3
2. Cuda 9.0 , Cudnn 7 


# Usage
1. ./darknet detector test data/obj.data data/yolo-obj.cfg backup/yolo-obj_800.weights data/data/img/frame77.jpg



#Result
10000 Times
<div>
 <img src="https://user-images.githubusercontent.com/30073100/47947460-3a229700-df60-11e8-9964-f1c3ec88071f.jpg" width="90%"></img>
 </div>

