FROM ubuntu
# make sure the package repository is up to date
RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update
RUN apt-get install python-software-properties build-essential python-dev git-core unzip wget -y
RUN add-apt-repository ppa:fkrull/deadsnakes -y
RUN apt-get update
RUN apt-get install python3.3 python3.3-dev -y
RUN wget https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py
RUN python ez_setup.py
RUN wget https://raw.github.com/pypa/pip/master/contrib/get-pip.py
RUN python get-pip.py
RUN pip install virtualenv
RUN virtualenv --python=/usr/bin/python3.3 /opt/ve/py33
ADD https://github.com/sigmavirus24/github3.py/archive/develop.zip /opt/develop.zip
RUN unzip /opt/develop.zip -d /opt
RUN cd /opt/github3.py-develop && /opt/ve/py33/bin/python setup.py test
