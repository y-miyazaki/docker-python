#--------------------------------------------------------------
# build image
# https://hub.docker.com/_/microsoft-azure-functions-python
#--------------------------------------------------------------
ARG IMAGE_VERSION=buster
FROM mcr.microsoft.com/azure-functions/python:${IMAGE_VERSION}

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
    pip install --upgrade isort && \
    # install azure-functions-core-tools-3
    apt install -y azure-functions-core-tools-3 && \
    # install az command
    apt update && \
    apt install -y gcc libffi-dev musl-dev && \
    pip install mock==4.0.2 && \
    pip install azure-cli && \
    # setting commands
    curl -sSfL https://raw.githubusercontent.com/y-miyazaki/cloud-commands/master/install.sh | sh -s -- ${CLOUD_COMMANDS_VERSION}
