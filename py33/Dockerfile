FROM ubuntu
RUN apt-get update
RUN apt-get install python-software-properties build-essential -y
RUN add-apt-repository ppa:fkrull/deadsnakes -y
RUN apt-get update
RUN apt-get install python3.3 python3.3-dev -y
RUN apt-get install python-pip
RUN pip install virtualenv
