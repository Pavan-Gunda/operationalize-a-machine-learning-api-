# operationalize-a-machine-learning-api-
[![CircleCI](https://circleci.com/gh/ph4n666/operationalize-a-machine-learning-api-.svg?style=svg)](https://app.circleci.com/pipelines/github/ph4n666/operationalize-a-machine-learning-api-)
    

# Cloud DevOps, Scaling Microservices

The project's goal is to operationalize a machine learning microservice using kubernetes. The service serves out predictions (inference) about housing prices through API calls. The model has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on.


### Install

- Docker
- Virtualbox
- hadolint
### Files explanation
- config.yml: CircleCI configuration file for running the tests
- app.py: Python flask app that serves out predictions (inference) about housing prices through API calls
- Dockerfile: Dockerfile for building the image
- make_prediction.sh: Send a request to the Python flask app to get a prediction
- Makefile: includes instructions on environment setup and lint tests
- run_docker.sh: file to be able to get Docker running, locally
- run_kubernetes.sh: file to run the app in kubernetes
- upload_docker.sh: file to upload the image to docker


### Run the project
1. To  build and run the docker image 
```
./run_docker.sh
```
2. To predict using the app in docker container as well as kubernetes cluster 
```
./make_prediction.sh
```
3.To create a cluster using minikube  
```
minikube start 
```

4. To deploy this application in kubernetes run:
```
./run_kubernetes.sh
```

5. Delete the cluster
```
minikube delete
