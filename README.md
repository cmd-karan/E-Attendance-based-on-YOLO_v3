# E-Attendance-System-based-on-YOLOv3-Darknet-Model
E-Attendance System is based on recognizing the presence of the students using Facial Recognition and then maintaining the records of the students' attendance on MySQL Database. So, the core idea behind our problem is **Object Detection**. Here, objects are the faces of the students whom attendance is to be marked as "Present".
## Our Setup

In our setup we have considered only four Classes(or Objects) for Detection i.e., faces of four students.
All the images in our dataset are hand-clicked by Moto-G5-Plus inside the classrooms of Indian Institute of Information Technology(IIIT), Pune. 
-The dimension of all the images reduced to 800*600* PPI.
-We have considered 601 images for training.
-We have considered 54 images for validating the quality of training.
-There are approx. 150 images for each class.
-All the images are annotated manually using LabelImg tool.
-Technique of Transfer Learning is used for training our dataset.
-Pre-Trained weights are taken from [darknet53.conv.74](https://pjreddie.com/media/files/darknet53.conv.74).
-Our Dataset consists of images taken for extreme cases to improve maintain a better trade-off between Precision and Recall.
-


## Core Idea
**Object Detection = Object Localisation + Object Recognition (Object Classification)**
