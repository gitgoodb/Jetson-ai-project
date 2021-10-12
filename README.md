# Jetson-ai-project
Project for jetson ai certificate

you must first have the jetson image from the hello AI world downloaded

to run project, download the project to home/face

then mount the folder into docker with these commands:

cd jetson-inference

docker/run.sh --volume ~/face:/face

to run the program:

cd /face/

python3 my_face.py --model=resnet18.onnx --labels=labels.txt --input_blob=input_0 --output_blob=output_0 /dev/video0
