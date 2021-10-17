# Jetson-ai-project
Project for jetson ai certificate

This program will run an image detection algorithm to detect if my face is in front the camera, and then open a text file with the "secrets" that I dont want my roomate to be able to access





you must first have the jetson image from the hello AI world downloaded

to run project:
create a folder to store the project

$mkdir unlock

Then download the project from github to the folder you just created.

To run the program, first ount the folder into docker with these commands:


$ cd jetson-inference

$ docker/run.sh --volume /unlock:/unlock


to run the program:


$ cd /unlock/

$ python3 unlocker.py --model=resnet18.onnx --labels=labels.txt --input_blob=input_0 --output_blob=output_0 /dev/video0
