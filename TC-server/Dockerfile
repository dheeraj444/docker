FROM centos
MAINTAINER dheeraj, username@gmail.com
RUN yum update -y && yum install wget -y
RUN yum remove java* -y && yum install -y java-1.8.0-openjdk-devel.x86_64
#ENV JAVA_HOME /usr/lib/jvm/java-1.8.0-openjdk
ADD tc-server /opt/tc-server
#RUN export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk && cd /opt/tc-server && ./tcruntime-instance.sh create -i /opt/tc-server dheeraj && cd dheeraj/bin && ./tcruntime-ctl.sh start
RUN export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk && cd /opt/tc-server && ./tcruntime-instance.sh create -i /opt/tc-server dheeraj && cd dheeraj/webapps && wget http://mirrors.jenkins.io/war-stable/latest/jenkins.war

EXPOSE 8080

WORKDIR /opt/tc-server/dheeraj
CMD ["bin/tcruntime-ctl.sh","start"]
