FROM ubuntu

RUN apt-get update && \
  apt-get install -y wget gnupg openjdk-8-jre && \
  wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | apt-key add - && \
  sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' && \
  apt-get update && \
  apt-get install -y jenkins git