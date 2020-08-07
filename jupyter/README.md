## This folder contains what is needed to create a docker image, run it to create a jupyter server with azure cli and spark installed.

## 1. Use dockerfile to create image

## 2. Run this cmd in WSL: 

> docker run -it --rm --user 1000 -p 8888:8888 -p 4040:4040 -v $(pwd):/home/jovyan azurecli-jupyter-spark

A url will be provided that you can run in a browser

**NOTE:** 
This was tested in WSL, Windows Subsytem for Linux. It is unknown if it will work in Windows.
