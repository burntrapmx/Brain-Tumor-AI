# Brain-Tumor-AI

# Project Name

An ai that detects brain tumors 
The dataset includes a total of 5,249 MRI images divided into training and validation sets. it adds labels corresponding to one of the four classes of brain tumors.

Classes

Class 0: Glioma

Class 1: Meningioma

Class 2: No Tumor

Class 3: Pituitar


![add image descrition here](direct image link here)

## The Algorithm

the algorithm works by training the AI and telling it the location of the brain tumors, once the training is complete, and an image of a tumor is shown to it, it will check the brain MRI scan for the zones of the tumors it was taught, when it detects one of the sections has a tumor, it shows it on the output

## Running this project

Open the terminal and input the comand 

"cd ~/jetson-inference",

then, open the docker using
"./docker/run.sh", 
after that, you drag the image you want to check for tumors from your dowloads folder and place it in any of the 4 classes in the subfolder of "test", afterwards, input the comand

"imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/(name of one of the subfolders of test you inputed it in)/(name of the image you imported).jpg (desired name for the output).jp"

, wait, and then the finished result will appear in there
