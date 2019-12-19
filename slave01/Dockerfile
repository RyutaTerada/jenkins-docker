FROM ubuntu:latest
#
RUN apt-get update
RUN apt-get -y install sudo openssh-server openjdk-8-jdk git gcc make openssl libssl-dev libbz2-dev libreadline-dev libsqlite3-dev
#
RUN mkdir -p /var/run/sshd
RUN useradd -d /home/jenkins -m -s /bin/bash jenkins
RUN echo jenkins:your_password | chpasswd
RUN echo 'jenkins ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers
#
EXPOSE 22
CMD ["/usr/sbin/sshd","-D"]