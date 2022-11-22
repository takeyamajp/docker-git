# git
Star this repository if it is useful for you.  
[![Docker Stars](https://img.shields.io/docker/stars/takeyamajp/git.svg)](https://hub.docker.com/r/takeyamajp/git/)
[![Docker Pulls](https://img.shields.io/docker/pulls/takeyamajp/git.svg)](https://hub.docker.com/r/takeyamajp/git/)
[![license](https://img.shields.io/github/license/takeyamajp/docker-git.svg)](https://github.com/takeyamajp/docker-git/blob/master/LICENSE)

### Supported tags and respective Dockerfile links  
- [`latest`, `rocky9`](https://github.com/takeyamajp/docker-git/blob/master/rocky9/Dockerfile) (Rocky Linux 9)
- [`rocky8`](https://github.com/takeyamajp/docker-git/blob/master/rocky8/Dockerfile) (Rocky Linux 8)
- [`centos8`](https://github.com/takeyamajp/docker-git/blob/master/centos8/Dockerfile) (We have finished support for CentOS 8.)
- [`centos7`](https://github.com/takeyamajp/docker-git/blob/master/centos7/Dockerfile)

### Image summary
    FROM rockylinux/rockylinux:9  
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
    
