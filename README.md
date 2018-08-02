# Jenkins Agent with chef and nvm

[![](https://images.microbadger.com/badges/image/dwolla/jenkins-agent-chef-nvm.svg)](https://microbadger.com/images/dwolla/jenkins-agent-chef-nvm)
[![license](https://img.shields.io/github/license/dwolla/jenkins-agent-docker-chef-nvm.svg?style=flat-square)](https://github.com/Dwolla/jenkins-agent-docker-chef-nvm/blob/master/LICENSE)

Docker image based on [Dwolla’s Jenkins Agent Chef Docker image](https://github.com/Dwolla/jenkins-agent-docker-chef) making [nvm](https://github.com/creationix/nvm) and [chef](https://github.com/chef/chef) available to Jenkins jobs.  With that, you get the ancillary benefits of a [Ruby](https://www.ruby-lang.org/en/) environment.


###  Local machine usage


#### Build

Example command to build this and add an image tag.

```
docker build -t my-really-cool-docker-image .
```

#### Run

Example command to run this while mounting AWS credentials as well as the current working directory:

```
docker run -it
  -v $HOME/.aws:/home/jenkins/.aws:ro \
  -v "$PWD":/home/jenkins/$(basename $PWD) \
  my-really-cool-docker-image /bin/bash
```
