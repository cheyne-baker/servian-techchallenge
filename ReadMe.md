# Servian Tech Challenge

## Design

## Prerequisists


## How to deploy

### Navigate to the git repository

### Build the deployment docker container

```
docker build -t servian/ansible:v1.0 -t servian/ansible:latest ./docker
```

### Run the docker container to deploy the solution

#### Windows
```
docker run -e AWS_ACCESS_KEY_ID=<AWS Access Key> -e AWS_SECRET_ACCESS_KEY=<AWS Secret Access Key> -e DEPLOY=<Solution Item> -v ${PWD}:/mnt servian/ansible
```

#### Linux