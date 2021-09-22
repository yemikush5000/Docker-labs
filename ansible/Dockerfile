FROM jenkins/jenkins

USER root

RUN apt update

RUN apt-get install -y python

RUN  curl -O https://bootstrap.pypa.io/pip/2.7/get-pip.py && \
     python get-pip.py && \
     pip install ansible --upgrade

USER jenkins



