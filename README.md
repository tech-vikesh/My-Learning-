# Day 29 – Introduction to Docker

## Task 1: What is Docker?
## What is a Container and Why Do We Need It?
 A container is a lightweight package that contains an application along with all its dependencies, libraries, and configuration files.

## We need containers because:
- They ensure applications run the same way on every system.
- They eliminate the "It works on my machine" problem.
- They are lightweight and start quickly.
- They make application deployment easier.
- They improve resource utilization compared to virtual machines.

## Containers vs Virtual Machines
- Container > Shares the host OS kernel, Lightweight, Starts in seconds, Uses fewer resources, Suitable for microservices and DevOps
- Virtual Machines > Has its own guest OS, Heavyweight, Takes minutes to start, Uses more resources, Suitable for running multiple operating systems

## Real Difference
- A Virtual Machine virtualizes the hardware and runs a complete operating system.
- A Container virtualizes the operating system and shares the host OS kernel, making it faster and more efficient

## Docker Architecture
- Docker consists of the following components:
## 1. Docker Client
- The Docker Client is the command-line tool used by users.
## Example:
Bash_
-  docker run nginx
   The client sends commands to the Docker Daemon.

## 2. Docker Daemon (dockerd)
- The Docker Daemon is the background service that:
- Builds images
- Runs containers
- Manages networks
- Manages storage

## 3. Docker Images
- A Docker Image is a read-only template used to create containers.
## Example:
 Bash_
- nginx
- ubuntu
- mysql

## 4. Docker Containers
- A Container is a running instance of a Docker Image.
## Example:
Bash_
- docker run nginx
 This command creates and starts an Nginx container.

## 5. Docker Registry
- A Docker Registry stores Docker Images.
- The most popular registry is Docker Hub.
## Example:
Bash_
- docker pull nginx
- Docker downloads the image from Docker Hub.

## Docker Architecture Diagram
- Plain text
  +----------------+
  | Docker Client  |
  | (docker CLI)   |
  +-------+--------+
       |
       v
 +----------------+
 | Docker Daemon  |
 |   (dockerd)    |
 +-------+--------+
         |
  +-----+-----+
  |           |
  v           v
 Images    Containers
  |
  v
 Docker Hub
(Registry)


## Task 2: Install Docker
## Verify Installation
Bash_
-  docker --version

## Run Hello World Container

Bash_
-  docker run hello-world

## This command:
- Checks if the image exists locally.
- Downloads it from Docker Hub if needed.
- Creates a container.
- Runs the container.
- Displays a success message.

## Task 3: Run Real Containers
- Run Nginx Container
Bash
-  docker run -d -p 8080:80 nginx
## Open:
Plain text
-  http://localhost:8080
## You should see the Nginx welcome page.
- Run Ubuntu Container
Bash
- docker run -it ubuntu bash
## Check Linux commands:
Bash
-    pwd
-    ls
 - whoami

## Exit:
Bash
- exit
## List Running Containers
Bash
- docker ps
## List All Containers
Bash
- docker ps -a
## Stop a Container
Bash
- docker stop <container_id>
## Remove a Container
Bash
- docker rm <container_id>

