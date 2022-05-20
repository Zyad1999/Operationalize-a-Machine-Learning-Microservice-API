[![CircleCI](https://circleci.com/gh/Zyad1999/Operationalize-a-Machine-Learning-Microservice-API/tree/master.svg?style=svg)](https://circleci.com/gh/Zyad1999/Operationalize-a-Machine-Learning-Microservice-API/tree/master)

## Project Overview
Take an application that uses trained model to predicts housing prices in boston and containerize that app using docker and then upload the image
to dockerhub and then run that image using kubernetes.

Files explanation
  -Makefile: contains some helpful python commands like linting and creating env and installing req
  -Dockerfile: Creats docker image of the application
  -config.yml: the main circleci workflow file
  -app.py: the flask app that takes the input and calls models to get prediction
  -make_prediction.sh: send request to running container and get prediction back  
  -run_docker.sh: builds and runs docker image and portforward
  -run_kubernetes.sh: run image on dockerhub on local kubernetes cluster and portforward
  -upload_docker.sh: uploads docker image to dockerhub

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
