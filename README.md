<include a CircleCI status badge, here>

[![CircleCI](https://dl.circleci.com/status-badge/img/gh/HimangiR1907/project4/tree/main.svg?stylestyle=shield)](https://dl.circleci.com/status-badge/redirect/gh/HimangiR1907/project4/tree/main)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

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

Used steps:

**handolint install** :
sudo wget -O /bin/hadolint https://github.com/hadolint/hadolint/releases/download/v1.16.3/hadolint-Linux-x86_64 
sudo chmod +x /bin/hadolint /bin/hadolint Dockerfile

**minikube install** : https://minikube.sigs.k8s.io/docs/start/
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube


**kubectl install** :
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl

Additinal links:
https://minikube.sigs.k8s.io/docs/start/
https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/


Project files:

Makefile :  Build file of the project.

requirements.txt : Dependency requirements.

un_docker.sh : Shell script for creating and running docker container.

run_kubernetes.sh: Shell script to deploy docker container on Kubernetes cluster.

upload_docker.sh : Shell script for uploading locally built docker image to dockerhub repository. 
link: https://hub.docker.com/

Dockerfile :  Dockerfile contains the application and the required dependencies. 

app.py  : REST Endpoint for prediction of housing prices in Boston.

output_txt_files : Docker ,Kubernetes output which stated the prediction i the logs itself.

model_data: model data for housing prices in Boston.

make_prediction.sh Calls prediction REST endpoint and simulates sample prediction after running the container (docker app) we are able to run the prediction using the make_prediction.sh script

.circleci/config.xml - CircleCI configuration file


[![CircleCI](https://dl.circleci.com/status-badge/img/gh/HimangiR1907/project4/tree/main.svg?style=shield)](https://dl.circleci.com/status-badge/redirect/gh/HimangiR1907/project4/tree/main)

[![CircleCI](https://dl.circleci.com/status-badge/img/gh/HimangiR1907/project4/tree/main.svg?stylestyle=shield)](https://dl.circleci.com/status-badge/redirect/gh/HimangiR1907/project4/tree/main)

