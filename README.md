# E-Attendance-System-based-on-YOLOv3-Darknet-Model
E-Attendance System is based on recognizing the presence of the students using Facial Recognition and then maintaining the records of the students' attendance on MySQL Database. So, the core idea behind our problem is **Object Detection**. Here, objects are the faces of the students whom attendance is to be marked as "Present".

### Our Setup
In our setup we have considered only four Classes(or Objects) for Detection i.e., faces of four students.
All the images in our dataset are hand-clicked by Moto-G5-Plus inside the classrooms of Indian Institute of Information Technology(IIIT), Pune. 
- The dimension of all the images reduced to 800 600 PPI.
- We have considered 601 images for training.
- We have considered 54 images for validating the quality of training.
- There are approx. 150 images for each class.
- All the images are annotated manually using LabelImg tool.
- Technique of Transfer Learning is used for training our dataset.
- Pre-Trained weights are taken from [darknet53.conv.74](https://pjreddie.com/media/files/darknet53.conv.74).
- Our Dataset consists of images taken for extreme cases to maintain a better trade-off between Precision and Recall i.e., 
  - Case 1 : When NO student whose "Present" is to be marked is really present.
  - Case 2 : When ALL students whose "Present" is to be marked are really present.
  - Case 3 : When SOME students whose "Present" is to be marked are really present.
  - Case 4 : All the above cases when other students are also present(or absent) in the class.
  - Case 5 : Images taken in LOW light as well.
- Training is done Google Colaboratory with 12.72GB RAM and 108GB Storage.
- Sample Images of Dataset used for training :
  - []/(path to be given here).
  - []/(path to be given here).
  - []/(path to be given here).

### Core Idea
 > **Object Detection = Object Localisation + Object Recognition (Object Classification)**

Our Problem of Object Detection can be broken down into two sub-problems : 
- 1. Object Localisation
- 2. Object Recognition

Object Localisation i.e., localising the object within an image can be achieved through Regression techniques whereas Object Recognition i.e., classifying the object localised within bounding boxes, this can be achieved through classification techniques.

Combining both the techniques we have various versions of RCNN i.e., RCNN, Fast-RCNN, Faster-RCNN but these models are quite slow when they deal in real time.
Therefore we are using YOLO(You-Only-Look-Once) based model which can process 45 frames per second i.e., fast enough to deal with real time problems.
 ### Results
