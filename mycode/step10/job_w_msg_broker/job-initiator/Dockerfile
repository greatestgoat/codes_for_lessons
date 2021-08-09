FROM ubuntu:16.04
RUN apt-get update && apt-get install -y iputils-ping dnsutils curl apt-transport-https python python-pip python-dev

# install kubectl
RUN curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add -
RUN touch /etc/apt/sources.list.d/kubernetes.list 
RUN echo "deb http://apt.kubernetes.io/ kubernetes-xenial main" | tee -a /etc/apt/sources.list.d/kubernetes.list
RUN apt-get update && apt-get install -y kubectl

# pyhon
# RUN apt-get install -y python python-pip python-dev
# RUN pip install --upgrade pip
# RUN apt-get update
RUN pip install --upgrade setuptools
COPY ./requirements.txt /requirements.txt
RUN pip install --no-cache-dir -r /requirements.txt

