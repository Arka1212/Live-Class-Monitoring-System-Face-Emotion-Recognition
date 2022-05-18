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

### 📉 ResNet50 (Model name ----> model_A)
Performed model creation using transfer learning taking the help of pretrained "ResNet50" architecture. Following are the loss and accuracy curves of the model (Model name ---> model_A).

![image](https://user-images.githubusercontent.com/85817763/169116129-deb100a1-4966-4c21-9950-8d2945fa4ce1.png)
![image](https://user-images.githubusercontent.com/85817763/169116185-ad6f5fb3-d5b7-4708-8e5a-a143ed475fcf.png)

Model got a training accuracy of 35.96% and validation accuracy of 31.43%. Focusing on the accuracy, its clear that this model cannot be used to implement in the real time scenario.

### 📉 Convolutional Neural Network (CNN)

#### CNN 1 (Model name ----> model_B)
Its the first CNN model. Following are the loss and accuracy curves of the model.

![image](https://user-images.githubusercontent.com/85817763/169116573-1897c824-4a77-404f-936a-6393a67c6611.png)
![image](https://user-images.githubusercontent.com/85817763/169116607-d0d493d0-3165-4acd-9792-996a2cbdc03e.png)


The first custom CNN model performed quite good and satisfactory with a training accuracy of 64.32% and validation accuracy of 65.09%. 

#### CNN 2 (Model name ----> model_C)
Its the second CNN model which is exactly the same as the first CNN model but the only difference is that its trained using 0.0001 learning rate instead of default learning rate just to check if it manages to boost the accuracy of the model. Following are the loss and accuracy curves of the model.

![image](https://user-images.githubusercontent.com/85817763/169117581-82bf1837-1f58-4eca-b301-2ced15496bab.png)
![image](https://user-images.githubusercontent.com/85817763/169117619-0f8bdb6e-8bb3-47b4-848c-392c036390f2.png)

This model also performed good with training accuracy of 63.52% and validation accuracy of 64.61%. Though was not able to beat the first CNN model's accuracy score.

So, first CNN model is saved as its the model with highest accuracy and can be used to develop a face emotion detection web application.
