# base image: last debian release
FROM debian:jessie

# name of the maintainer of this image
LABEL maintainer "Anthony.Baire@irisa.fr"

# install the latest upgrades
RUN apt-get update && apt-get -y dist-upgrade

# install nginx
RUN apt-get -y --no-install-recommends  install nginx

# set the default container command
# -> run nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]

# Tell the docker engine that there will be something listening on the tcp port 80
EXPOSE 80
