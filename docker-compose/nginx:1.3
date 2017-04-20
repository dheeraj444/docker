FROM centos:centos6

RUN yum -y update; yum clean all
RUN yum -y install epel-release; yum clean all
RUN yum -y install nginx; yum clean all
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
RUN echo "nginx round robin" > /usr/share/nginx/html/index.html
RUN cd /etc/nginx/conf.d/ && rm -rf default.conf
COPY load-balancer.conf /etc/nginx/conf.d/
EXPOSE 80

ENTRYPOINT [ "/usr/sbin/nginx" ]
