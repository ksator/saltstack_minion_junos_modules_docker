# About this repository 
This repository has a Dockerfile for SaltStack minion and the dependencies for junos modules. 
At each git push, the Docker Hub pull down this repository and build a docker image using the Dockerfile and push it onto the Docker Hub.

# Requirement 
Install Docker

# Usage
To download the Docker image from the Docker registry, use this command:
```
docker pull ksator/saltstack_minion_junos_modules_docker
```
```
docker images
```
# Example  

## Pull images:
```
docker pull ksator/saltstack_master_junos_syslog_engine_docker
docker pull ksator/saltstack_minion_junos_modules_docker
docker images
```
## Instanciate containers: 
```
docker run -d -t --rm --name master -p 516:516/udp -p 4505:4505 -p 4506:4506 ksator/saltstack_master_junos_syslog_engine_docker
docker run -d -t --rm --name minion1 -p 4605:4505 -p 4606:4506 ksator/saltstack_minion_junos_modules_docker
docker ps
```

## If you want to connect to a container cli, run these commands:
```
docker exec -it master bash
exit
```
```
docker exec -it minion1 bash
exit
```
## Then you still need to configure the containers


