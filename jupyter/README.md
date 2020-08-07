## This folder contains what is needed to create a docker image, run it to create a jupyter server with azure cli and spark installed.

There are two ways for you to use this container:
- You can pull the built image, bethz/azurecli-jupyter-spark, from DockerHub
- You can clone this repo and do a docker build locally.  If you are going to change the contents of the file, use this option.

## Cloning this repo and building the Dockerfile locally

### 1. Clone this repo

### 2. Use dockerfile to create image in WSL
> ./build.sh

Be sure Docker is installed and the daemon is running and accessible from WSL.

if build.sh does not run, try:
> chmod +x build.sh

You can check if it ran by typing:
> docker image ls

Look for bethz/azurecli-jupyter-spark 


### Congrats! You should now have a Docker container!

Run the Docker Container with this cmd in WSL in the folder where you want to create jupyter notebooks: 

> docker run -it --rm --user 1000 -p 8888:8888 -p 4040:4040 -v $(pwd):/home/jovyan azurecli-jupyter-spark

A url will be provided that you can run in a browser.  Sometimes Windows will show (or hide) an approval for docker to access your local drive from wsl.

You can create jupyter notebooks and they were be in your $pwd folder.

**NOTE:** 
This was tested in WSL, Windows Subsytem for Linux. It is unknown if it will work in Windows.
