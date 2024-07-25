# Traffic-Light-Color-Recognition
This is a Network Program that can recognize traffic lights and their colors! This project was meant to be more portable and easy to use, as it was trained to be used for the road, but due to time limits, it can only be used to recognize downloaded images on a computer/labtop. **iDTech UCLA Demo**

## The Algorithm
The model I used was first trained through a **resnet-18 based image classifier** and made using an **NVIDIA Jetson Nano**. my model had went through **transfer learning**, meaning that the model I have used was already made, it was just given a new task to be trained and learned on. This allows for the model to be trained faster, since it still has knowledge from the previous task. The model went through 42 epochs in a span of around 2-3 hours, with a starting accuracy of 58% for training, and 54% for validation. When it was donne, the training accuracy reached 86%, and the validation accuracy reached 96%. Here is a test run to show that it works
![Confidence of Image](https://github.com/user-attachments/assets/793cea33-a2be-4728-8fc1-b49e0c8263e3)
![Test Image](https://github.com/user-attachments/assets/bff4293f-ef7f-4318-b0df-6d0b3d4ee349)

## Running the project
This will teach you how to input your own images to be tested!
**REQUIREMENTS**
-Clone *dusty_nv's Jetson Inference model* https://github.com/dusty-nv/jetson-inference 
-Download *my resnet-18 imagenet classifier model and example images* https://drive.google.com/drive/folders/1RBMfOSrS8cGapmC_GW9gDhgxr904MJNN
**HOW TO RUN THE MODEL**

