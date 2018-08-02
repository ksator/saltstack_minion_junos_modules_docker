This repository has a Dockerfile for SaltStack minion and the dependencies for junos modules. 
At each git push, the Docker Hub pull down this repository and build a docker image using the Dockerfile and push it onto the Docker Hub.
To download the Docker image from the Docker registry, use this command:
```
docker pull ksator/saltstack_minion_junos_modules_docker
```
```
docker images
```
