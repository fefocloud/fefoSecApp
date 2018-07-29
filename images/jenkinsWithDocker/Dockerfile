FROM jenkins/jenkins:lts
LABEL br.com.fefocloud.version="0.0.1-beta"

RUN curl -fsSL https://get.docker.com/ | sh
RUN systemctl start docker
RUN systemctl enable docker
RUN usermod -aG docker $(whoami)


