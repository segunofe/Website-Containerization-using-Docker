Implementation Steps1

First, install Docker Engine on your terminal (Visual Studio Code) or EC2 instance.

In my case, on Cloud9 terminal, I remotely (via SSH) connected to an EC2 instance i already created to run my docker containers and then installed docker engine for Ubuntu operating system (since i created the Ec2 Instance using Ubuntu OS) by following the steps in the link below.

Follow this step: https://docs.docker.com/engine/install/ubuntu/

mkdir docker-containers

1. Create the Dockerfile in the same directory as index.html and style.css.

vi Dockerfile

vi index.html

vi style.css

2. Build the Docker image:

docker build . -t html-server:v1.0

3. Run the Docker container

docker run --rm -d -p 8081:8000 --name htmlserver html-server:v1.0

This runs the container in detached mode and maps port 8080 on your host machine to port 8000 in the container.

4. Access the site

Open your web browser and go to PublicIPOfEC2Instance:8080 to see the website served by the Python HTTP server.
