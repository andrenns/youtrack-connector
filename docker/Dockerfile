FROM centos:8
RUN dnf -y install python3 python3-pip python3-devel
COPY ./requirements.txt /github-connector/requirements.txt
ADD . /github-connector
WORKDIR /github-connector
RUN yum -y install graphviz
RUN yum -y install gcc
RUN pip3 install -r requirements.txt
RUN yum -y install unzip
RUN unzip -o ngrok-stable-linux-amd64.zip
ENTRYPOINT [ "python3" ]
EXPOSE 5000
CMD [ "main.py" ]