#--------------------------------------------------------------
# build image
# https://hub.docker.com/_/python
#--------------------------------------------------------------
ARG IMAGE_VERSION=buster
FROM python:${IMAGE_VERSION}

#--------------------------------------------------------------
# ARG
#--------------------------------------------------------------
ARG WORKDIR=/workspace
ARG CLOUD_COMMANDS_VERSION

#--------------------------------------------------------------
# ENV
#--------------------------------------------------------------

#--------------------------------------------------------------
# workdir
#--------------------------------------------------------------
RUN mkdir -p ${WORKDIR}
WORKDIR  ${WORKDIR}

#--------------------------------------------------------------
# Install dependent packages
#--------------------------------------------------------------
RUN apt update && \
    apt install -y make git zip bash curl sudo jq groff && \
    pip install --upgrade pip && \
    pip install --upgrade setuptools && \
    pip install --upgrade flake8 && \
    pip install --upgrade flake8-mypy && \
    pip install --upgrade mypy && \
    pip install --upgrade autopep8 && \
    # setting commands
    curl -sSfL https://raw.githubusercontent.com/y-miyazaki/cloud-commands/master/install.sh | sh -s -- ${CLOUD_COMMANDS_VERSION}
