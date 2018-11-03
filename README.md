# ObjectDetection_raspberry-pi
for raspberrypi
- will be updated soon!!
- You can use RaspberryPi ObjectDetection Project

# Develop enviroment
 1. Collect Image & Test Device
- Raspberry pi (model B+)
- Picamera

 2. Train Device
- OS  :Ubuntu 18.0.4 
- CPU : I7-5930K
- RAM : 32G
- GC  : 1080 GTX * 3


# Requriement
- openCV 3.4.3
- Cuda 9.0 , Cudnn 7 
- darknet yolo

# Usage
1. Train
- ./darknet detector train data/obj.data data/yolo-obj.cfg darknet19_448.conv.23 -gpus 0,1,2
(gpus is option. if you have 1 graphic card, this command must be ignored)
1. ./darknet detector test data/obj.data data/yolo-obj.cfg backup/yolo-obj_800.weights data/data/img/frame77.jpg



# Result
- 10000 Times
<div>
 <img src="https://user-images.githubusercontent.com/30073100/47947460-3a229700-df60-11e8-9964-f1c3ec88071f.jpg" width="90%"></img>
 </div>
 
- 45000 Times( It takes 20Hours)
<div>
 <img src="https://user-images.githubusercontent.com/30073100/47953159-e4300c80-dfbc-11e8-9874-19008b774f76.jpg" width="90%"></img>
 </div>

