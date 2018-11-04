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
- keras , tensorflow
- (install git clone https://github.com/pjreddie/darknet )
- (install http://pjreddie.com/media/files/darknet19_448.conv.23 ) we use convolutional layer

# Usage
1. Collect Data
- You can collect Data by pi-camera

2. Labelling & Annotation
- I used Yolo-Mark, ( https://github.com/AlexeyAB/Yolo_mark)

3. Use Yolo Darknet & Train ( I used 182 images to train)
- Darknet Program and Dataset are so heavy, so I uploaded my Drive()
- ./darknet detector train data/obj.data data/yolo-obj.cfg darknet19_448.conv.23 -gpus 0,1,2
(gpus is option. if you have 1 graphic card, this command must be ignored)

- Or If you want to ignore this steps, install https://drive.google.com/file/d/1dyIzCND9XUpJbjuR0rJ72at23sdtKShT/view?usp=sharing , this is my train model

2. convert model to keras
- python3 ./yad2k.py yolo-obj.cfg yolo-obj_final.weights model_data/yolo.h5
- (you have to use YAD2K https://github.com/allanzelener/YAD2K ) 
- (Or you can use my Drive())

3. Detect
- (image) ./darknet detector test data/obj.data data/yolo-obj.cfg backup/yolo-obj_final.weights data/data/img/frame77.jpg
- (webcam) ./darknet detector demo data/obj.data data/yolo-obj.cfg backup/ yolo-obj_final.weights data
- (Use keras) (run yolo.py)


# Result
- 10000 Times
<div>
 <img src="https://user-images.githubusercontent.com/30073100/47947460-3a229700-df60-11e8-9964-f1c3ec88071f.jpg" width="90%"></img>
 </div>
 
- 45000 Times( It takes 20Hours)
<div>
 <img src="https://user-images.githubusercontent.com/30073100/47953159-e4300c80-dfbc-11e8-9874-19008b774f76.jpg" width="90%">
 <img src="https://user-images.githubusercontent.com/30073100/47960844-82b38080-e044-11e8-8b94-051d4b14867f.png" width=90%">
 <img src="https://user-images.githubusercontent.com/30073100/47959927-6bb86280-e033-11e8-8af1-4ca2c5ee38ce.jpg" width'"90%"> 
 </img>
 </div>

