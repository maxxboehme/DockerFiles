# This is a base image for development
# Contains basic software needed for building
# Installs
# - make
# - curl
# - wget
# - git
# - oepnssh-client openssh-server
# - cmake
# - unzip bzip2

FROM debian:latest

RUN apt-get update -y

RUN apt-get install -y make

RUN apt-get install -y curl wget

RUN apt-get install -y git

RUN apt-get install -y openssh-client openssh-server

RUN apt-get install -y cmake

RUN apt-get install -y unzip bzip2
