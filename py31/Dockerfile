FROM ubuntu
# make sure the package repository is up to date
RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update
RUN apt-get install python-software-properties build-essential python-dev unzip -y
RUN add-apt-repository ppa:fkrull/deadsnakes -y
RUN apt-get update
RUN apt-get install python3.1 python3.1-dev -y
ADD https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py /tmp/ez_setup.py
RUN python /tmp/ez_setup.py
ADD https://raw.github.com/pypa/pip/master/contrib/get-pip.py /tmp/get-pip.py
RUN python /tmp/get-pip.py
RUN pip install virtualenv
RUN virtualenv --python=/usr/bin/python3.1 /opt/ve/py31
ADD https://github.com/sigmavirus24/github3.py/archive/develop.zip /opt/develop.zip
RUN unzip /opt/develop.zip -d /opt
WORKDIR /opt/github3.py-develop
CMD /opt/ve/py31/bin/python setup.py test
