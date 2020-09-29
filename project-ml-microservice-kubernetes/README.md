<include a CircleCI status badge, here>

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

The project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project I will:
* Test the project code using linting
* Complete a Dockerfile to containerize this application
* Deploy the  containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested


---
## Get the code base
Step 1: Clone my following git repository where i have all the changes uploaded:
		https://github.com/gopinath-vs/DevOps_Microservices

Step 2: Goto DevOps_Microservices\project-ml-microservice-kubernetes folder



## Setup the Environment
Step 3: Run the following command to create a virtual env and to activate it:
		make install

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`


Explanation of files in the repo:
1. make_prediction.sh - This is the script to run to check the predictions
2. Makefile - Contains seps to setup environment, install libs, 
3. Dockerfile - contains steps to build docker image and run app in docker container
4. upload_docker.sh - to push the docker image to Docker hub
5. requirements.txt - Contains the list of apps/libs to be installed
6. run_docker.sh - It will run app in docker container
7. run_kubernetes.sh - It will run app in minikube (kubernetes)
8. app.py - application code
9. .circleci/config.yml - CircleCI configuration file that contains steps to run in CirccleCI CI/CD
10. output_txt_files/docker_out.txt - contains the captured log details while running app within docker containter
11. output_txt_files/kubernetes_out.txt - contains the captured log details while running app within kubernetes

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
