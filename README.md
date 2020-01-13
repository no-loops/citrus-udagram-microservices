# Udagram Microservices
> Udacity Cloud Developer Nanodegree

# Github Location
> https://github.com/no-loops/citrus-udagram-microservices

# Docker Images
> https://hub.docker.com/r/citrusdev/

# Installation Steps
### Install Pre-requisites
1. Docker 
2. AWS CLI
3. Eksctl
4. AWS-iam-authenticator
5. Kubectl

### Setup the following Environmental variables 
(you might also have to explicity define these variables in addition to adding them to your profile)
```
POSTGRESS_USERNAME;
POSTGRESS_PASSWORD;
POSTGRESS_DB;
POSTGRESS_HOST;
AWS_REGION;
AWS_PROFILE;
AWS_BUCKET;
JWT_SECRET;
```

### Build docker images and upload
`docker-compose -f docker-compose-build.yaml build --parallel`  
`docker images`   
`docker-compose up`  
`docker-compose -f docker-compose-build.yaml push`

### Create a Kubernetes Cluster on Amazon EKS with eksctl
`eksctl create cluster --name "ClusterName" --version 1.14 --nodegroup-name standard-workers --node-type t3.medium --nodes 3 --nodes-min 1 --nodes-max 4 --node-ami auto`

 ### Setup Kubernetes Environment

Load secret files:
- `kubectl apply -f aws-secret.yaml`
- `kubectl apply -f env-secret.yaml`
- `kubectl apply -f env-configmap.yaml`  

Apply all other yaml files:
- `kubectl apply -f .`

### Check your Pods Status

`kubectl get all`

