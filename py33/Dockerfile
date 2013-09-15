FROM ubuntu
# make sure the package repository is up to date
RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update
RUN apt-get install python-software-properties build-essential -y
RUN add-apt-repository ppa:fkrull/deadsnakes -y
RUN apt-get update
RUN apt-get install python3.3 python3.3-dev -y
RUN apt-get install python-pip -y
