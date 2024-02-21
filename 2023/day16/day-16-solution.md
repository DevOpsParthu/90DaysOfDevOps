# Day 16 Task: Docker for DevOps Engineers.

## Docker

Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

<div align="center">
  <img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1708310367323/28a2c9c4-1167-4945-bd2b-41cb4ecae363.png" alt="my logo">
</div>

# Tasks

### As you have already installed Docker in previous days' tasks, now is the time to run Docker commands.

`sudo apt-get install docker.io -y && sudo chown $USER /var/run/docker.sock`

### Use the `docker run` command to start a new container and interact with it through the command line. [Hint: docker run hello-world or docker run nginx]

`docker run nginx`


<div align="center">
  <img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1708435793752/c2987add-48ef-4393-99d5-888e184aebf0.png" alt="my logo">
</div>


`docker run -d --name nginx -p 80:80 nginx:latest`

- docker run: This command is used to create and start a new container from a Docker image.

- d: This flag stands for "detached" mode, which means the container will run in the background, and the terminal will return immediately after starting the container. It allows you to continue using the terminal without being attached to the container's console.

- p 80:80: This option is used for port mapping. It maps port 80 of the host machine to port 80 of the container. It allows traffic coming to port 80 of the host to be redirected to port 80 of the running Nginx container.

- nginx:latest: This specifies the Docker image to use when creating the container. In this case, it's using the nginx image with the latest tag, which refers to the most recent version of the Nginx image available on your local system or in the Docker Hub repository.


<div align="center">
<img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1708436041590/2793af4c-2a29-4339-a2be-e40a1800a87b.png" alt="my logo">
</div>


- Explanation: This commands use the docker run commands to start a new container based on hello-world and its create image.Docker will pull the image if its not available in locally and simply container prints a message to conform that your Docker installation is working.

### Use the `docker inspect` command to view detailed information about a container or image.

`docker ps`

`docker inspect <CONTAINER_ID>`


<div align="Center">
<img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1708435885266/9e05b47a-12f0-4c1b-8175-24470c1e538e.png" alt="my_logo">
</div>


- Explanation: The docker inspect command provide the detail information of your container or image.Using docker ps -a command you check your IMAGE and CONTAINER ID of your TASK:1
