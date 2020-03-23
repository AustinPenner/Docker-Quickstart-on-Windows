# Docker Quickstart on Windows
Quickstart guide for using Docker on Windows

### Docker
Docker allows you to run Spark, SQL, and other Data Science tools. Installing Docker and Creating Containers is a more involved process on Windows, but most the rest of Docker's functionality behaves the same as Linux. 

### Installing Docker:
Here are the requirements for installing Docker. 


![Docker Requirements](https://github.com/AustinPenner/Docker-Quickstart-on-Windows/blob/master/images/Docker%20Requirements%20(Windows).png "Docker Requirements")

* If you meet these requirements
  * [Install Docker Desktop](https://docs.docker.com/docker-for-windows/install/)
  * Share your drives with Docker
    * Go to the system tray, right click on Docker Desktop and select Settings
    * Go to Resources -> File Sharing and select "C" (or whichever local drive you use)
* If you don't meet these requirements (e.g. you have Windows 10 Home or below)
  * [Install Docker Toolbox](https://docs.docker.com/toolbox/toolbox_install_windows/) instead

### Creating Containers:
Follow the docker quick guide. A common problem with Windows is connecting your Docker container to your local file system. Here's an example with mongodb:

1) If first time pulling image:    
`$ docker pull mongo`

2) Create the container, if not restarting one:   
`$ docker run --name mongoserver -p 27017:27017 -v /c/Users/username/galvanize:/home/data -d mongo`

3) Remote into docker container shell:   
`$ docker exec -it mongoserver bash`

4) Access mongo shell:   
`$ mongo`

5) Stop the terminal:   
`$ docker stop mongoserver`

6) To restart:   
`$ docker start mongoserver`



From this point the usage is much the same across operating systems. You can use the docker [quick start guide](https://github.com/GalvanizeDataScience/lectures/blob/Austin/docker/docker_quick_guide.md) from here.
