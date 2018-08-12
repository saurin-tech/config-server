# Overview
This is a simple spring boot config-server project with [palantir gradle plugin](https://github.com/palantir/gradle-docker) that generates docker image.

## How to run 
1. To build this project `cd` into the root of the project.
2. Execute `./gradlew build docker` command. This will build the docker image for you.
    1. To check if the docker image was build or not you can execute `docker images` command and it will list images for you.
3. To run the image you've just built execute `docker run -p 8888:8888 -t saurinp12/config-server:0.0.1-SNAPSHOT`
    1. To find the IP of the container the project is running in execute `docker inspect <container id> | grep "IPAddress"`
        1. To get the container id you can execute `docker ps`