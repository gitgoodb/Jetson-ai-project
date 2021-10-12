# Jetson-ai-project
Project for jetson ai certificate

This program will run an image detection algorithm to detect if my face is in front the camera, and then open a text file with the "secrets" that I dont want my roomate to be able to access





you must first have the jetson image from the hello AI world downloaded

to run project, download the project to home/face

then mount the folder into docker with these commands:


$ cd jetson-inference

$ docker/run.sh --volume ~/face:/face


to run the program:


$ cd /face/

$ python3 my_face.py --model=resnet18.onnx --labels=labels.txt --input_blob=input_0 --output_blob=output_0 /dev/video0
