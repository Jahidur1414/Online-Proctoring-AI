# Online-Proctoring-AI
This one is a AI based online Proctoring system.

Jahidur Rahman Fahim

Gmail: jahidurrahman1414@gmail.com

![OP-1](https://user-images.githubusercontent.com/39921122/96893658-c19aa500-14ac-11eb-86f5-73b045c1dae0.PNG)

Head pose estimation is a challenging problem in computer vision because of the various steps required to solve it. Firstly, we need to locate the face in the frame and then the various facial landmarks. Now, recognizing the face seems a trivial task in this day and that is true with faces facing the camera. The problem arises when the face is at an angle. Add to that some facial landmarks are not visible due to the movement of the head. After this, we need to convert the points to 3D coordinates to find the inclination.

## Requirements

For this project, we need OpenCV and Tensorflow so let’s install them.

```
#Using pip
pip install opencv-python
pip install tensorflow

#Using conda
conda install -c conda-forge opencv
conda install -c conda-forge tensorflow
```
**Face Detection**

Our first step is to find the faces in the images on which we can find facial landmarks. For this task, we will be using a Caffe model of OpenCV’s DNN module. If you are wondering how it fares against other models like Haar Cascades or Dlib’s frontal face detector.

**Facial Landmark Detection**

The most commonly used one is Dlib’s facial landmark detection which gives us 68 landmarks, however, it does not give good accuracy. Instead, we will be using a facial landmark detector. It also gives 68 landmarks and it is a Tensorflow CNN trained on 5 datasets! The pre-trained model. 

**Pose estimation**

In computer vision the pose of an object refers to its relative orientation and position with respect to a camera. You can change the pose by either moving the object with respect to the camera, or the camera with respect to the object.

The pose estimation problem described in this tutorial is often referred to as Perspective-n-Point problem or PNP in computer vision jargon. As we shall see in the following sections in more detail, in this problem the goal is to find the pose of an object when we have a calibrated camera, and we know the locations of n 3D points on the object and the corresponding 2D projections in the image.

## Eye Tracking

In this project i used Gaze tracking for Eye tracking.

![image](https://user-images.githubusercontent.com/39921122/96896875-db89b700-14af-11eb-857f-82132304ee72.png)

The typical eye structure used in gaze tracking applications is demonstrated in that picture. The modeling of gaze direction is based either on the visual axis or on the optical axis. The visual axis, which forms the line of sight (LoS) and is considered the actual direction of gaze, is the line connecting the center of the cornea and the fovea. The optical axis, or the line of gaze (LoG), is the line passing through the centers of pupil, cornea, and the eyeball. The center of cornea is known as the nodal point of the eye. The visual and optical axes intersect at the nodal point of the eye with a certain angular offset. The position of head in 3D space can be directly estimated by knowing the 3D location of the corneal or eyeball center. In this way, there remains no need for separate head location models. Thus, the knowledge of these points is the keystone for majority of the head pose invariant models .

![image](https://user-images.githubusercontent.com/39921122/96897451-6bc7fc00-14b0-11eb-965f-614671bdc885.png)


## Getting started

First you need to move in the this github file directory using **Anaconda Command Prompt**. Then install all prerequisites using this command.

Then Download the **shape_predictor_68_face_landmarks** file from this link [Click Here](https://drive.google.com/file/d/1sqHit7yvjXMrtlVmmiP2pO1nvMn7TL1s/view?usp=sharing)

and then replace it in **Online Proctoring AI->gaze_tracking->trained_models** folder.

Also Download the **variables.data-00000-of-00001** file from this link [Click Here](https://drive.google.com/file/d/1gz7SrCsiZWle7uICqhstJFXnHphtvqpu/view?usp=sharing)

and then replace it in **Online Proctoring AI->models->pose_model->variables** folder

**Then Run Those Command.**

`pip install -r requirements.txt`

Then run the main.py file.

`python main.py`

# Thank You
