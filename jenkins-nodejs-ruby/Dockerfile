FROM jenkins:latest


RUN mkdir /tmp/WEB-INF
RUN mkdir /tmp/WEB-INF/plugins

RUN curl -L https://updates.jenkins-ci.org/latest/nodejs.hpi -o /tmp/WEB-INF/plugins/nodejs.hpi
RUN curl -L https://updates.jenkins-ci.org/latest/ruby-runtime.hpi -o /tmp/WEB-INF/plugins/ruby-runtime.hpi

RUN curl -L https://updates.jenkins-ci.org/latest/publish-over-ssh.hpi -o /tmp/WEB-INF/plugins/publish-over-ssh.hpi

RUN curl -L https://updates.jenkins-ci.org/latest/config-file-provider.hpi -o /tmp/WEB-INF/plugins/config-file-provider.hpi

USER root
RUN cd /tmp; zip --grow /usr/share/jenkins/jenkins.war WEB-INF/*
USER jenkins
