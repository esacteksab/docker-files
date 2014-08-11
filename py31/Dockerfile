FROM ubuntu
RUN apt-get update
RUN apt-get install python-software-properties build-essential python-dev unzip python-pip software-properties-common -y
RUN add-apt-repository ppa:fkrull/deadsnakes -y
RUN apt-get update
RUN apt-get install python3.1 python3.1-dev -y
RUN pip install virtualenv
RUN virtualenv --python=/usr/bin/python3.1 /opt/ve/py31
ADD https://github.com/sigmavirus24/github3.py/archive/develop.zip /opt/develop.zip
RUN unzip /opt/develop.zip -d /opt
WORKDIR /opt/github3.py-develop
CMD /opt/ve/py31/bin/python setup.py test
