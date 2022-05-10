# Live-Class-Monitoring-System-Face-Emotion-Recognition

------------------------------------------------------------------------------------------------------------------------------------------------------------
## Introduction
Facial Emotion Recognition (FER) is the technology that analyses facial expressions from both static images and videos in order to reveal information on one’s emotional state. It belongs to the family of technologies often referred to as ‘affective computing’, a multidisciplinary field of research on computer’s capabilities to recognise and interpret human emotions and affective states and it often builds on Artificial Intelligence technologies. Facial expressions are forms of non-verbal
communication, providing hints for human emotions. FER analysis comprises three steps face detection, facial expression detection, expression classification to an emotional state.

So, the need for such kind of use cases has lead to Artificial Intelligence's rapid development, which made a significant contribution to the technological world. Machine Learning (ML) and Deep Learning (DL) algorithms have achieved considerable success in various applications such as classification systems, recommendation systems, pattern recognition etc.

So, emotion recognition is a very active current field of computer vision research that involves facial emotion detection and the automatic assessment of sentiment from visual data. Human-machine interaction is an important area of research where artificially intelligent systems with visual perception aim to gain an understanding of human interaction.

![image](https://user-images.githubusercontent.com/85817763/166962634-e056c082-c214-46f6-b037-1d8d9e3ad9c5.png)

## Problem Statement
The Indian education landscape has been undergoing rapid changes for the past 10 years owing to the advancement of web-based learning services, specifically, eLearning platforms.

Global E-learning is estimated to witness an 8X over the next 5 years to reach USD 2B in 2021. India is expected to grow with a CAGR of 44% crossing the 10M users mark in 2021. Although the market is growing on a rapid scale, there are major challenges associated with digital learning when compared with brick and mortar classrooms. One of many challenges is how to ensure quality learning for students. Digital platforms might overpower physical classrooms in terms of content quality but when it comes to understanding whether students are able to grasp the content in a live class scenario is yet an open-end challenge.

In a physical classroom during a lecturing teacher can see the faces and assess the emotion of the class and tune their lecture accordingly, whether he is going fast or slow. He can identify students who need special attention. Digital classrooms are conducted via video telephony software program (ex-Zoom) where it’s not possible for medium scale class (25-50) to see all students and access the mood. Because of this drawback, students are not focusing on content due to lack of surveillance. While digital platforms have limitations in terms of physical surveillance but it comes with the power of data and machines which can work for you. It provides data in the form of video, audio, and texts which can be analysed using deep learning algorithms. Deep learning backed system not only solves the surveillance issue, but it also removes the human bias from the system, and all information is no longer in the teacher’s brain rather translated in numbers that can be analysed and tracked.

## Objective
I will solve the above mentioned challenge by applying deep learning algorithms to live video data. The solution to this problem is by recognizing facial emotions. The main aim is to use 'Tensorflow' which is a popular framework of  machine learning and deep learning. It is a free and open-source library which is released on 9 November 2015 and developed by Google Brain Team. It is entirely based on Python programming language and used for numerical computation and data flow, which makes machine learning and deep learning faster and easier.


![image](https://user-images.githubusercontent.com/85817763/166960555-84f50568-1c53-4aca-9b90-bb22975b0314.png)

## Head-start References
❖ https://towardsdatascience.com/face-detection-recognition-and-emotion-detection-in-8-lines-of-code-b2ce32d4d5de

❖ https://towardsdatascience.com/video-facial-expression-detection-with-deep-learning-applying-fast-ai-d9dcfd5bcf10

❖ https://github.com/atulapra/Emotion-detection

❖ https://medium.com/analytics-vidhya/building-a-real-time-emotion-detector-towards-machine-with-e-q-c20b17f89220

## Dataset
Following dataset is been used to address the above problem statement.

Dataset link - https://www.kaggle.com/msambare/fer2013

## Dataset Information
The data consists of 48x48 pixel grayscale images of faces. The faces have been automatically registered so that the face is more or less centred and occupies about the same amount of space in each image.

The task is to categorize each face based on the emotion shown in the facial expression into one of seven categories:- 

0 = Angry 

1 = Disgust 

2 = Fear

3 = Happy

4 = Sad

5 = Surprise

6 = Neutral

##  Model Creation
Model architectures taken into consideration are as follows:
1. Convolutional Neural Networks (CNN)
2. ResNet50

### CNN
Created a customised CNN model. Loss and accuracy curves of the model are as follows:

![image](https://user-images.githubusercontent.com/85817763/167655979-db6f9b33-ccd6-418d-a46a-1090d20eb614.png)
![image](https://user-images.githubusercontent.com/85817763/167656048-70637435-8e07-4ec8-8c6d-b4cd3cdb51fd.png)

The model performed better than average with a training accuracy of 69.72% & validation accuracy of 62.09%

### ResNet50
Created a model using the pre-trained architecture of ResNet50 while freezing the layers. Loss and accuracy curves of the model are as follows:

![image](https://user-images.githubusercontent.com/85817763/167680099-96456c3c-87ee-485e-a8fb-4f771bf64f7e.png)
![image](https://user-images.githubusercontent.com/85817763/167680138-9805d7ce-f546-4a8e-a7f0-f904b8604ee8.png)

The model did not perform well with a training accuracy of 38.64% & validation accuracy of 38.77%

