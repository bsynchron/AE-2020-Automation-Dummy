FROM jenkins/jenkins:lts

USER root
RUN echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main" >> /etc/apt/sources.list && \
    apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367 && \
    apt update -y && apt install sshpass ansible -y
USER jenkins
RUN ssh-keygen -t rsa -q -f "/home/jenkins_home/.ssh/id_rsa" -N ""
