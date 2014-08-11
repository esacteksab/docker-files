FROM ubuntu
RUN apt-get update
RUN apt-get install python-software-properties build-essential python-dev unzip python-pip software-properties-common -y
RUN add-apt-repository ppa:fkrull/deadsnakes -y
RUN apt-get update
RUN apt-get install python3.1 python3.1-dev -y
RUN pip install virtualenv
RUN virtualenv --python=/usr/bin/python3.1 /opt/ve/py31
ADD https://github.com/sigmavirus24/betamax/archive/master.zip /opt/master.zip
RUN unzip /opt/master.zip -d /opt
WORKDIR /opt/betamax-master
RUN /opt/ve/py31/bin/pip3.1 install -r dev-requirements.txt
CMD /opt/ve/py31/bin/pip3.1 install -U dev-requirements.txt
CMD /opt/ve/py31/bin/py.test
