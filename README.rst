Playing with Docker. Putting up my Dockerfiles. 

Different versions of Python in Ubuntu with
https://launchpad.net/~fkrull/+archive/deadsnakes

Docker's Dockerfile tutorial: http://www.docker.io/learn/dockerfile/level1/

The Dockerfiles that exist are largely a work in progress.  

The general idea is that it installs a non-standard version of Python (which
is why there is not a py27 dir/Dockerfile). It also installs pip and setuptools
via commandline rather than system packages. 

A virtualenv is created in ``/opt/ve/pyXX`` where XX = 26/31/32/33. 

I've also included the ``unzip`` package, as Github ships their packages in
'zip' rather than a 'tar'. 
