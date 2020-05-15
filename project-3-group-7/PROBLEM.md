# Problem Statement

In this project, you will have to implement a simple image classification server. You will use a pre-trained model and build a container to use the model for inference.

You should use the PyTorch machine learning framework, an open-source library based on the Torch library. You are required to use a pre-trained Densenet-121 model for Pytorch, which is publicly available online. Your code will use the model for inference: it will take an image as an input and return a classification as an output. You are not required to change, retrain, or modify the model.

Your code should run as a backend server that handles HTTP requests. The HTTP requests will include test images to classify. The server will be included in a docker container using a Python 3.7 image as the launching point. You are required to create a README file that lists the steps required to run the classifier. The steps should be straightforward. They should just involve running the docker image and then sending a POST or GET request with the test image file to the server running the docker container.
