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

- `docker run`: This command is used to create and start a new container from a Docker image.

- `d`: This flag stands for "detached" mode, which means the container will run in the background, and the terminal will return immediately after starting the container. It allows you to continue using the terminal without being attached to the container's console.

- `p` 80:80: This option is used for port mapping. It maps port 80 of the host machine to port 80 of the container. It allows traffic coming to port 80 of the host to be redirected to port 80 of the running Nginx container.

- `nginx:latest`: This specifies the Docker image to use when creating the container. In this case, it's using the nginx image with the latest tag, which refers to the most recent version of the Nginx image available on your local system or in the Docker Hub repository.


<div align="center">
<img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1708436041590/2793af4c-2a29-4339-a2be-e40a1800a87b.png" alt="my logo">
</div>


- **Explanation**: This commands use the `docker run` commands to start a new container based on hello-world and its create image.Docker will pull the image if its not available in locally and simply container prints a message to conform that your Docker installation is working.

### Use the `docker inspect` command to view detailed information about a container or image.

`docker ps`

`docker inspect <CONTAINER_ID>`


<div align="Center">
<img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1708435885266/9e05b47a-12f0-4c1b-8175-24470c1e538e.png" alt="my_logo">
</div>


- **Explanation**: The `docker inspect` command provide the detail information of your container or image.Using docker ps -a command you check your IMAGE and CONTAINER ID of your TASK:1

### Use the `docker port` command to list the port mappings for a container.

`docker ps`

`docker port <CONTAINER_ID>`


<div align="center">
  <img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1701757021860/3ded4a89-9df3-47ad-aae3-4f4256a59006.png" alt="my logo">
</div>


- **Explanation**: The `docker port` command specify the port mapping of its containers.


### Use the `docker stats` command to view resource usage statistics for one or more containers.

`docker ps`

`docker stats <CONTAINER_ID>`


<div align="center">
  <img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1701757230634/5861827d-e41b-4ed4-800c-c49b83ef1ec6.png" alt="my logo">
</div>


- **Explanation**: This `docker stats` commands provides the real-time resource usage statistics for one or more containers.


### Use the `docker top` command to view the processes running inside a container.


`docker ps`

`docker top <CONATINER_ID>`


<div align="center">
  <img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1701757365707/0c9e9b96-48c4-4f0a-bffe-47f21c7011c5.png" alt="my logo">
</div>


- **Explanation**: The `docker top` commands display the process of running inside the containers.


### Use the `docker save` command to save an image to a tar archive.

`docker ps`

`docker save -o <output_tar_file_name>.tar <image_name>`


<div align="center">
  <img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1701757562457/ca8765d9-ca94-4fb2-a351-5ecb4f1e4911.png" alt="my logo">
</div>


- **Explanation**: The `docker save` command export to an image to a tar archive.


### Use the `docker load` command to load an image from a tar archive.


`docker ps`

`docker load -i <input_tar_file_name>.tar`


<div align="center">
  <img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1701757710856/812e5845-64fd-4d76-a091-b4e16758d8bd.png" alt="my logo">
</div>


- `-i` <input_tar_file_name>.tar: The `-i` flag stands for "input," specifying the input file containing the Docker image. `<input_tar_file_name>.tar` is the name of the tar archive file from which you want to load the Docker image.

- **Explanation**: The `docker load` commands import an image from a tar archive.

- *Finally move your tar file in to Docker directory using this command `mv nginx_file.tar Docker/`*

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

*Happy Learning*

*Thanks For Reading! :)*

*-DevOpsParthu💝💥*
