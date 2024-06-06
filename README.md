# Overview 
Implementation of Computer Vision for Suspicious Activity Detection using YOLOv8(You Only Look Once) in  OpenCV a computer vision library. This project involves the use YOLOv8 a pretrained object detection model and custom logic for the detection of suspicious elements in the video footage.

# User Interface and Implementation
A StreamLit user interface is made based on python script to show the efficiency and working of the model by making the frontend user interface with it.

The below set of images show the implementation of abandoned object detection based on YOLOv8. Here is a drop and drop graphical pointer user interface wherein a video is fed directly, at the moment this project is made on the basis video input manually, but the future scope lies by putting a video stream using streaming application like apache kafka or web-sockets(but may not be so useful).

This is the proposed full product architecture model
![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/a28f0958-acad-49e9-8830-bbd2535bca21)

This is its ERD diagram for the product architecture
![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/7b2016e6-5bd7-49b6-8f0a-2eef5f596a94)

# Abandoned Object Detection
The logic behind this is that once the distance between the person and bag which are highlighted as the objects to detected in the coco.txt file of the YOLOv8 tracker, it only detects these two objects and once the two get apart by a particular pixels it flags it as an adandoned object as shown in the screenshots below.

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/dd7c6916-5202-4ef3-85bb-d2103fae178f)

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/e06ef032-d8d6-4f6b-9aa8-839b56360943)

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/77cd4dba-8104-42f4-9331-48d5ee854ae3)

# Counting the number of people entering or leaving a place
This logic is build on the basis of region of concern or ROC, here we cant checking the entire frame to check whos entering the train and whos leaving. So the implementation of this comes such that there are 2 region of concerns, and if a person entering the train has to move through the outer ROC and then inner ROC, vice versa for a person leaving. So this way the count is established as shown in frames below.

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/3cd92310-4b81-4f5b-b560-6ca3e1fa654f)

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/6b3c40e3-04c9-4430-a59f-6a4efcdf49ee)

# Zone Density
This logic or part of the model is build by couting the no. of people in each region of the frame inside a video. The small boxes annotated around people and object show the confidence ratio. And the number at the center of each zone is showing the count of the people.

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/75e672c8-2a1b-489b-a4ad-6dec22636bc7)

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/298245d6-dbb8-4ff8-b032-cbf84e51ce89)

# Hyperparameter Tuning
The model used for this project is YOLOv8, which is a pretrained object detection model trained on a particular dataset. For the specific requirement of adding parameter tuning, this image annotation is done on Roboflow as shown in the screenshots below to increase the accuracy of the system.

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/9a78adff-de58-45a6-90ee-bef54b84aa16)

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/d0cd6410-d666-47fc-9568-be404093f42a)

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/65e78df0-1b79-4ef9-940a-152dcf7e0dc8)

precision analysis based on the custom dataset
![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/6ca82901-00f1-4849-b796-447891f0e712)

confusion matrix based on the custom dataset
![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/e2073a0b-e69d-41b6-b0f1-84c8b38131ef)

# Product Results
These are the results of the model build

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/721fa70b-5a63-41d4-9fdb-cd35d24876b0)

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/6a11e113-f073-4496-8451-9d5a51992f99)

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/d880cd99-a684-424a-89ab-c0eea5a9e999)

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/423fc008-c551-41c1-a674-a665ec398651)

![image](https://github.com/AdityaDighe/YOLO-v8-Suspicious-Activity-Detection/assets/98305705/32af20df-1f55-41cc-aa74-d049f6a52b2a)



