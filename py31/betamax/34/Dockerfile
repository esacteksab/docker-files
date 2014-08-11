FROM ubuntu
RUN apt-get update
RUN apt-get install python-software-properties build-essential python-dev unzip python-pip software-properties-common -y
RUN add-apt-repository ppa:fkrull/deadsnakes -y
RUN apt-get update
RUN apt-get install python3.4 python3.4-dev -y
RUN pip install virtualenv
RUN virtualenv --python=/usr/bin/python3.4 /opt/ve/py34
ADD https://github.com/sigmavirus24/betamax/archive/master.zip /opt/master.zip
RUN unzip /opt/master.zip -d /opt
WORKDIR /opt/betamax-master
RUN /opt/ve/py34/bin/pip3.4 install -r dev-requirements.txt
CMD /opt/ve/py34/bin/pip3.4 install -U dev-requirements.txt
CMD /opt/ve/py34/bin/py.test
