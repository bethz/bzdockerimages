# bzdockerimages
Project containing Dockerfiles to build my custom images

## Python
Base image is a ubuntu image.
As of 2020Jun24, that's Ubuntu:18.04
## Python 3.7
apt install -y python3.7 and python3-pip
image is mypython:3.7.x

## Python 3.6
same as 3.7 but with 3.6
image is mypython:3.6.x

## SQLAlchemy - to be done
Based on mypython:3.7.x image plus:
apt install -y sqlalchemy
image is mypython:sqlAlc
