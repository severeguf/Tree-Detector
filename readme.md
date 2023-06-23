# Tree Detector

 This project uses sattelite images of the earth to detect if there are trees in the image or not.

![add image descrition here](direct image link here)

## The Algorithm

Add an explanation of the algorithm and how it works. Make sure to include details about how the code works, what it depends on, and any other relevant info. Add images or other descriptions for your project here. 
I used a dataset of satellite images of places with trees, and no trees. (https://www.kaggle.com/datasets/mcagriaksoy/trees-in-satellite-imagery?resource=download) The dataset works perfectly for my project because the images are useful in training and running the model. Although there is not much code required to run the project, I still had to make folders and move the pictures around in order to upload them and run it in Visual Studio. The algorithm is simple, because the AI learns from thousands of different pictures with trees and no trees, and uses what it has learned to detect if there are trees in the image or not.

## Running this project

1. Add steps for running this project.
change directories:  jetson-inference/python/training/classification/data
run the docker container
run training script to re-train: python3 train.py --model-dir=models/<change-name> data/<dataset-name>
run the export script: python3 onnx_export.py --model-dir=models/<change-name>
change directories to classification
check to see if model is on nano: ls models/<change-name>/
run command to show results: imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/cat/01.jpg result.jpg


2. Make sure to include any required libraries that need to be installed for your project to run.
The only library needed is the jetson-inference library.
[View a video explanation here](video link)
