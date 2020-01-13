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

POSTGRESS_USERNAME;
POSTGRESS_PASSWORD;
POSTGRESS_DB;
POSTGRESS_HOST;
AWS_REGION;
AWS_PROFILE;
AWS_BUCKET;
JWT_SECRET;

### Build docker images and upload
`docker-compose -f docker-compose-build.yaml build --parallel`  
`docker images`  
`docker-compose up`
`docker-compose -f docker-compose-build.yaml push`


