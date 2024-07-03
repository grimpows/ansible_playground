FROM python:bookworm
LABEL type="demo"

ARG ANSIBLE_VERSION=9.1.0

RUN apt update && apt upgrade -y && apt install sshpass
RUN apt-get install iputils-ping  -y


RUN apt-get install tree -y
RUN pip3 install toml

RUN ssh-keygen -t rsa -f "/root/.ssh/id_rsa" -N ""

COPY ./ssh.config /root/.ssh/config

RUN ls -la ~/.ssh

RUN chmod 600 ~/.ssh/config

RUN apt install ansible -y


# RUN pip install "ansible==$ANSIBLE_VERSION"

CMD ["tail", "-f", "/dev/null"]
