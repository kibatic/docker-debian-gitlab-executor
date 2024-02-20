Docker debian gitlab-ci executor
===============================

This is a docker image based on debian-slim with docker installed and used for the CI/CD pipeline in gitlab.

## Usage

The configuration to remember in your .gitlab-ci.yml file are :

```yaml
image: kibatic/debian-gitlab-executor:latest

variables:
  DOCKER_HOST: tcp://docker:2375
  DOCKER_TLS_CERTDIR: ""
  DOCKER_DRIVER: overlay2

services:
  - docker:dind
```
