# this shows how we can extend/change an existing official image from Docker Hub

FROM nginx:latest
# highly recommend you always pin versions for anything beyond dev/learn
# Notice that its always better to stat with some official image from Docker hub and extend it. In this way since, these official images are 
# managed and maintained by Docker itself, our own image is also easy to maintain.

WORKDIR /usr/share/nginx/html
# change working directory to root of nginx webhost
# using WORKDIR is preferred to using 'RUN cd /some/path'
# So here basically while building the image, changeing the working directory of a container from the current directory to the root of nginx
# webhost.
# same could be done with RUN cd /usr/share/nginx/html, but it is always prefered to make use of WORKDIR, because it is always easier to use and
# describe with the help of WORKDIR in Dockerfile.

COPY index.html index.html
# So after switching to the root of nginx webhost in the previous stanza we have now copied the index.html static webpage file from our local host
# to the container directory /usr/share/nginx/html.