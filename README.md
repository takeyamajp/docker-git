# git
[![Docker Stars](https://img.shields.io/docker/stars/takeyamajp/git.svg)](https://hub.docker.com/r/takeyamajp/git/)
[![Docker Pulls](https://img.shields.io/docker/pulls/takeyamajp/git.svg)](https://hub.docker.com/r/takeyamajp/git/)
[![license](https://img.shields.io/github/license/takeyamajp/docker-git.svg)](https://github.com/takeyamajp/docker-git/blob/master/LICENSE)

### Supported tags and respective Dockerfile links  
- [`latest`, `centos8`](https://github.com/takeyamajp/docker-git/blob/master/centos8/Dockerfile)
- [`centos7`](https://github.com/takeyamajp/docker-git/blob/master/centos7/Dockerfile)

### Image summary
    FROM centos:centos8  
    MAINTAINER "Hiroki Takeyama"
    
    ENV TIMEZONE Asia/Tokyo
    
    ENV REQUIRE_SSL true
    
    ENV HTTPD_LOG true  
    ENV HTTPD_LOG_LEVEL warn
    
    ENV GIT_REPOSITORY dev.git  
    ENV GIT_USER user1,user2  
    ENV GIT_PASSWORD password1,password2
    
    VOLUME /git
    
    EXPOSE 80  
    EXPOSE 443
    
