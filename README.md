# Docker Quickstart on Windows
Quickstart guide for using Docker on Windows

### Docker
Docker allows you to run Spark, SQL, and other Data Science tools. Installing Docker and Creating Containers is a more involved process on Windows, but most the rest of Docker's functionality behaves the same as Linux. 

### Installing Docker:
Here are the requirements for installing Docker. 

* If you meet these requirements
  * [Install Docker Desktop](https://docs.docker.com/docker-for-windows/install/)
* If you don't meet these requirements (e.g. you have Windows 10 Home or below)
  * [Install Docker Toolbox](https://docs.docker.com/toolbox/toolbox_install_windows/) instead

### Creating Containers:
Follow the docker quick guide. A common problem with Windows is connecting your Docker container to your local file system. The following command should create a container:

  `$ docker run --name mongoserver -p 27017:27017 -v "$PWD":/home/data -d mongo`

Windows doesn't like "$PWD" to reference the current file path. Replace this with the full file path on your machine:

  `$ docker run --name mongoserver -p 27017:27017 -v c:/Users/username/galvanize:/home/data -d mongo`
