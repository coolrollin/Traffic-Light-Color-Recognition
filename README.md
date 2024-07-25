# Traffic-Light-Color-Recognition
This is a Network Program that can recognize traffic lights and their colors! This project was meant to be more portable and easy to use in a real world context. Application developers can import my model to python or C++ programs that use webcams. Their programs can use this model to classify still images taken from those webcams.

## The Algorithm
The model I used was first trained through a **resnet-18 based image classifier** and made using an **NVIDIA Jetson Nano**. my model had went through **transfer learning**, meaning that the model I have used was already made, it was just given a new task to be trained and learned on. This allows for the model to be trained faster, since it still has knowledge from the previous task. The model went through 42 epochs in a span of around 2-3 hours, with a starting accuracy of 58% for training, and 54% for validation. When it was donne, the training accuracy reached 86%, and the validation accuracy reached 96%. Example output run on an image of a yellow light is shown below.

![Confidence of Image](https://github.com/user-attachments/assets/793cea33-a2be-4728-8fc1-b49e0c8263e3)

![Test Image](https://github.com/user-attachments/assets/bff4293f-ef7f-4318-b0df-6d0b3d4ee349)

## Running the project
This will teach you how to input your own images to be tested!

**REQUIREMENTS**
-Clone *dusty_nv's Jetson Inference model* https://github.com/dusty-nv/jetson-inference 

-Download *my resnet-18 imagenet classifier model and example images* https://drive.google.com/drive/folders/1RBMfOSrS8cGapmC_GW9gDhgxr904MJNN

- Put the model in the /jetson-inference/python/training/classification/models/traffic_light directory


**HOW TO RUN THE MODEL**
1. navigate to /jetson-inference/python/training/classification
2. set bash variables `NET=/models/traffic_light` and `DATASET` to a directory of your choice with images to classify.
3. run the command `imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/NAME_OF_CLASS_FOLDER/NAME_OF_JPEG DESIRED_NAME_OF_OUTPUT_JPG`. The most probable output class of the model should be listed in the terminal.
