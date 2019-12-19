FROM ubuntu

RUN apt-get update && \
  apt-get install -y wget gnupg openjdk-8-jre apt-transport-https ca-certificates curl software-properties-common && \
  wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | apt-key add - && \
  sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' && \
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add - && \
  add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" && \
  apt-get update && \
  apt-get install -y jenkins docker-ce && \
  curl -L https://github.com/docker/compose/releases/download/1.20.0-rc1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose && \
  chmod +x /usr/local/bin/docker-compose