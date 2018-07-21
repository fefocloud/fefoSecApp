FROM jenkins/jenkins:lts
MAINTAINER leandrodmax@gmail.com

RUN curl -fsSL https://get.docker.com/ | sh
RUN systemctl start docker
RUN systemctl enable docker
RUN usermod -aG docker $(whoami)


