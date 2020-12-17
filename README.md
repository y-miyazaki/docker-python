# Various samples for python language

## Overview

This repository is a collection of Dockerfile, VS Code Remote Development settings, VS Code settings, python development, and all necessary settings.

## Description

## setting for VS CODE

- [.vscode/settings.json](https://github.com/y-miyazaki/config/blob/master/.vscode/settings.json)  
  I don't manage this repository, This files basically manage the settings required for VS CODE.  
  Color settings, font size, etc. are your preference, so it is better to modify them freely.

- [.vscode/cspell.json](https://github.com/y-miyazaki/config/blob/master/.vscode/cspell.json)  
  Settings for extensions to prevent misspellings. Although it prevents misspellings in English, various settings are made to respond to spelling such as commands and imports.
  \
  \
  https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker

- [.editorconfig](https://github.com/y-miyazaki/config/blob/master/.editorconfig)  
  Since it is not possible to make detailed settings for each extension only with VSCODE settings.json, .editorconfig is used.  
  This setting requires the following extensions.
  \
  \
  https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig

## docker for python build and development environment

- [docker](docker)  
  docker was created for build for python language and local development environment.  
  All docker images themselves are uploaded to [docker hub](https://hub.docker.com/).
  \
  \
  https://hub.docker.com/u/ymiyazakixyz

- [docker/base](docker/base)  
  There is a base image Dockerfile mainly for build, local development, and test.
  There is a base image that contains a CLI that is likely to be used for python development.
  \
  https://hub.docker.com/r/ymiyazakixyz/python-local

<!-- - [docker/build](docker/build)
  This is a sample for build. Some people may need to modify the Dockerfile.

- [docker/local](docker/local)
  This is a sample for local. Some people may need to modify the Dockerfile.

- [docker/test](docker/test)
  This is a sample for test. Some people may need to modify the Dockerfile. -->

## env for VS Code Remote Development

- [env](env)  
  This directory contains sample configuration files for [VS Code Remote Development](https://code.visualstudio.com/docs/remote/remote-overview).  
  \
  Normally, I think that some people were working in the docker container with `docker exec -it {container name} bash` etc. from terminal, By linking VS CODE and the Docker container, you can directly operate the Docker container with VS CODE and you can use the extension and settings as they are.  
  \
  There is a python environment and an environment for additional lambda development environments. The serverless framework CLI is also installed in the lambda development environment.

- [env/base](env/base)  
  There are templates and examples for python development environment used in [VS Code Remote Development](https://code.visualstudio.com/docs/remote/remote-overview).

---

## Required

- Visual Code Studio  
  https://code.visualstudio.com/download
- Docker  
  https://www.docker.com/

## Other Link

- docker hub  
  https://hub.docker.com/
- VS CODE Remote Development  
  https://code.visualstudio.com/docs/remote/remote-overview
- VS CODE Remote Development Container  
  https://code.visualstudio.com/docs/remote/containers
