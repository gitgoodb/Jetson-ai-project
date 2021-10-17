# Jetson-ai-project
Project for jetson ai certificate

This program will run an image detection algorithm to detect if my face is in front the camera, and then open a text file with the "secrets" that I dont want my roomate to be able to access

This program is in no way secure, and should not be used to store information that you want to hid from other people.  Everything is stored in plain text, and can be very easily found through the file explorer.  This is intended simply as a fun project to learn more about using the Jetson Nano.

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



To create a model yourself, use the camera-capture built into hello-ai-world, documented here: https://github.com/dusty-nv/jetson-inference/blob/master/docs/pytorch-collect.md
Be sure to leave your camera in a fixed position and if at all possible have it pointing towards a blank background to make the recognition process simpler.  
After collecting the images of both yourself and the person or people who you want to keep out of the file, follow the instructions to train and export your model.  Then copy that model into the folder where you have the rest of the project saved.
