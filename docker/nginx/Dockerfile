FROM centos:centos7
LABEL  version=nginx1 

# Update CentOS
RUN yum update -y

# Add CentOS 7 EPEL repository
RUN yum install epel-release -y

# Install nginx
RUN yum install nginx -y; yum clean all

# Copy test HTML file
COPY ./index.html /usr/share/nginx/html/index.html 

# Expose Port 80
EXPOSE 80

STOPSIGNAL SIGTERM
CMD ["nginx", "-g", "daemon off;"]
