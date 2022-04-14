FROM jenkins/jenkins
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt

RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt
#RUN jenkins-plugin-cli --plugins configuration-as-code:1414.v878271fc496f adoptopenjdk:1.4
