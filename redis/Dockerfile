FROM centos

MAINTAINER dheeraj

RUN yum update -y && yum -y install epel-release && yum install redis -y

EXPOSE 6379

ENTRYPOINT ["/usr/bin/redis-server"]
