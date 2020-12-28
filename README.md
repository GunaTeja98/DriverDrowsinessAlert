# Driver Drowsiness Detection using Machine Learning and Iris Detection Mechanism

Venkata Guna Teja Siripurapu*, Vadapalli Surya Pramod, D C Chinni Krishnudu, Sireesha Rodda
Department of Computer Science and Engineering, GITAM Institute of Technology, GITAM University, Visakhapatnam, India
-Corresponding author*: svgteja@gmail.com

Abstract   The main theme of this paper is to alert the drowsy driver to keep him active. The system is designed as a non-intrusive real-time monitoring system. The focus will be placed on designing a system that will accurately monitor the open or closed state of the driver’s eyes in real-time. The priority is on improving the safety of the driver without being obtrusive. Face Recognition and Iris Detection technology have been used by implementing OpenCV. The Haarcasscade xml files are used to detect the eyes. By using this information and OpenCV package we detect the driver is feeling drowsy or not. After the system detects drowsiness, it triggers an alarm to alert the driver. The alarm will be on until the driver opens his eyes.     

Keywords—Machine Learning, Eye Detection, Face Recognition, Speech driven , Winsound beep alarm, Haarcasscades xml files, OpenCV.

 ## 1 Introduction

In our everyday life we come across several bus accidents and car crashes, most of them occurred due to driver’s fatigue. It is one of the major causes of accidents in the world. Based on the recent statistics estimate there was 1,200 deaths and 76,000 injuries annually, which can be attributed to fatigue-related crashes. To prevent them we have to build a detection system. The development of technologies for detecting or preventing drowsiness at the wheel is a major challenge in the field of accident avoidance systems. Because of the hazard that drowsiness presents on the road, methods need to be developed for counteracting its affects. The aim of this project is to develop a prototype drowsiness detection system. 

### 1. The system will detect a Face 
When the car is in the motion the system will be active. It will detect the face by    Computer Vision package OpenCV.
### 2.By using the haarcascade xml files
The focus will be placed on designing a system that will accurately monitor the open or closed state of the driver’s eyes in real-time. By monitoring the eyes, it is believed that the symptoms of driver fatigue can be detected early enough to avoid a car accident.
### 3. Blink Detection
Detection of fatigue involves the observation of eye movements and blink patterns in a sequence of images of a face.
### 4. Alert the driver
By a fixed alarm we can alert the driver. Until he returns to his active state the alarm will continue. After he opens his eyes the alarm will automatically stops

In this paper, the prevention of accidents caused by the driver’s fatigue can be stopped. The remainder of paper is divided as follows: Section 2 contains the related work. Section 3 contains the methodology used. Section 4 contains the results and their analysis. Section 5 contains the conclusions and further extensions to the methodology.


## 2 Related Work

There were significant contributions made earlier in the fields related to face detection technology and Iris detection. But the contributions made by different authors were as different sets. In this paper, both face recognition and iris detection.

Miaou [1] proposed an example called "Study of Vechicle scrap page Rates" using the vision based approach. The system deals with using the information gained from the binary version of the image to find the edges of the face by using the image processing.  This article describes about detecting the driver drowsiness by estimating vision system of him.

Wreggit, Kim, and Wierwille [2] had done a research on "Vehicle-Based Driver Status Performance Monitoring". These systems are developed using a non-intrusive machine vision based concepts. This reportdescribes how to find the eyes and also how to determine if the eyes are opened or closed by using retinal reflection as a means to finding the eyes on the face.

Williamson and Chamberlain[4],“Review of on-road driver fatigue monitoring devices” the system assessses the ability of conducting safe driving and notifies the driver for any dangerous situation.

Singh, Bhatia, and Kaur[7], “Eye tracking based driver fatigue monitoring and warning system”. it is implemented by compared from both the frames,if the driver is suspected to be sleeping then a warning alarm is given.
.


## 3 Methodology

In this paper, we will be using OpenCV for face recognition and Haarcascade xml files for face detection and Iris detection for effectively identifying drunken driver and generate an alert with the aim to minimize road accidents. PyCharm IDE and Python Interpreter have been used for implementation. The required packages included Threaded, NumPy, win sound and OpenCV.


For the Driver’s Face Detection, the driver has to keep the device facing him. This Mechanism was used which included 2 stages (1) Face Detection (2) Iris detection. When driver is feeling drowsy and his eyes are closed them the algorithm detects the closing if the eyes.  
                             

The next part in the flow would be drowsiness, Drowsiness of a person can be measured by the extended period of time for which his/her eyes are in closed state. In our system, primary attention is given to the faster detection of the drowsiness. 
Initially, the image is acquired by the webcam for processing. Then we use the Haarcascade file face.xml to search and detect the faces in each individual frame. If no face is detected then another frame is acquired. If a face is detected, then a region of interest in marked within the face. This region of interest contains the eyes. Defining a region of interest significantly reduces the computational requirements of the system. After that the eyes are detected from the region of interest by using Haarcascade_eye.xml
                                       


The number of frames for which eyes are closed is monitored. If the number of frames exceeds a certain threshold value, then a warning message is generated on the display showing that the driver is feeling drowsy. If an eye is detected then there is no
blink and the blink counter K are set to ‘0’. If the eyes are closed in a particular frame, then the blink counter is incremented and a blink is detected. When the eyes are closed for more than 4 frames then it is deducible that the driver is feeling drowsy. Hence drowsiness is detected and an alarm sounded. After that the whole process is
repeated as long as the driver is driving the car.
It is the same function as that of the face detection. Here eye cascade is used and minimum size of the object is decreased and optimized to detect eyes of various sizes in the image. As described earlier cvRectangle () is used to draw rectangle for sequences of eyes detected in a given frame. The detection process is continued until a key is pressed. When the key is pressed the program stops executing the detection function and stops capture form camera, releases memory and closes video window.
                           




## 4 Results

In this section we will display the results obtained at every stage. First we will be detecting the face as as shown in Figure 2. Now we will be detecting the iries. Finally we will get the results of the report.




                     

## 5 Conclusions and Future Work
The driver drowsiness can be detected by many ways,they can be sleepy,drunken,etc.This system is developed by using eye detection on how the driver is been behaving while he is driving we can differentiate between normal eye blink and drowiseness eye blink while driving. The proposed method we can reduce the road accidents. This also works with the person who is wearing spectacles and even under low lights with better outputs. We use facedetection to detect if eyes are opened or closed with several methods which will alert the driver if he is sleeping. We can also make this system advanced in future by adding "Internet Of Things". We can alert the driver relatives or friends so which makes more safer for thr driver

References
[1] Miaou, “Study of Vehicle Scrap page Rates,” Oak Ridge National Laboratory, Oak Ridge, TN,, S.P.,April 2012.

[2] Wreggit, S. S., Kim, C. L., and Wierwille, W. W., Fourth Semi-Annual Research Report”, Research on Vehicle-Based Driver Status Performance Monitoring”, Blacksburg, VA: Virginia Polytechnic Institute and State University, ISE Department, January 2013.

[3] Bill Fleming, “New Automotive Electronics Technologies”, International Conference on Pattern Recognition, pp. 484- 488,December 2012.

[4] Ann Williamson and Tim Chamberlain,“Review of on-road driver fatigue monitoring devices”, NSW Injury Risk Management Research Centre, University of New South Wales, , July 2013.

[5] E. Rogado, J.L. García, R. Barea, L.M. Bergasa, Member IEEE and E. López, February, 2013, “Driver Fatigue Detection System”, Proceedings of the IEEE International Conference on Robotics and Biometics, Bangkok, Thailand.

[6] Boon-Giin Lee and Wan-Young Chung, Member IEEE, “Driver Alertness Monitoring Using Fusion of Facial Features and Bio-Signals”, IEEE Sensors Journal, VOL. 12, NO. 7, July 2012.

[7] H. Singh, J. S. Bhatia, and J. Kaur, “Eye tracking based driver fatigue monitoring and warning system”, in Proc. IEEE IICPE, New Delhi, India, Jan. 2014.
