# DockerAUV
# Installing Docker

These steps listed below are for Ubuntu Desktop 18 LTS. You can find the full official docs and steps for other Linux distributions here:  
Ubuntu: https://docs.docker.com/install/linux/docker-ce/ubuntu/  
Fedora: https://docs.docker.com/install/linux/docker-ce/fedora/  
CentOS: https://docs.docker.com/install/linux/docker-ce/centos/  
Debian: https://docs.docker.com/install/linux/docker-ce/debian/  
Installing Docker  
The Docker docs suggest setting up a Docker repository to install and update from.   
This is where you should start:  
https://docs.docker.com/install/linux/docker-ce/ubuntu/#set-up-the-repository    
This should download and run the test container printing "hello world" to your console.   
Installing Docker Compose  
Unlike the Mac and Windows Docker Desktop versions, we must manually install Docker Compose. See the instructions for the installation steps (Click on the tab for Linux)  
https://docs.docker.com/compose/install/#install-compose  
After completing, test your installation:  
docker-compose -v  
This should print the version and build numbers to your console.   
Run without Sudo  
Follow these instructions to run Docker commands without sudo:  
https://docs.docker.com/install/linux/linux-postinstall/#manage-docker-as-a-non-root-user  
The docker group will likely already be created, but you still need to add your user to this group.  
Start on Boot  
Follow these instructions so that Docker and its services start automatically on boot:  
https://docs.docker.com/install/linux/linux-postinstall/#configure-docker-to-start-on-boot  
You may need to restart your system. 

# Running the build
Pull the repository into your working directory.   
Now build the image using docker. Type this command in directory of the DockerFile
```Shell
docker build -t ros .
```
This should build the image. Nos you can use use 
```
docker ps
```
to get the container id while some container is running. Copy the container id. There won't be any need of container id after we start using docker hub.  
Finally run the image using

```
docker run -it ros
```
To run a terminal in the same container :
```
docker exec -it container_id bash
```
Remember you'll have to source the environment variables for every new terminal CURRENTLY. This will be fixed in future.
```
cd catkin_ws
source devel/setup.bash
```

