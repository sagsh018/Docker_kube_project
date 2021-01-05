FROM centos:latest

RUN yum update -y 
RUN yum install nginx -y
COPY ./html/ /usr/share/nginx/html/ 

RUN ln -sf /dev/stdout /var/log/nginx/access.log \
    && ln -sf /dev/stderr /var/log/nginx/error.log 

CMD ["nginx", "-g", "daemon off;"]