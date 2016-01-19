# chef-nginx-gcp

Deploying an application to google compute with Chef

chef-zero installation
------------
chef-zero  can be installed as a Ruby Gem.
```
    $ gem install chef-zero
```
chef server docker container
------------
chef server standalone can be deployed a host as a Docker container.
```
creating the chef server standalone container

Download the chef server package from chef.io  into
the docker path under this project
```
curl -o docker/chef-server.deb -L https://packagecloud.io/chef/stable/packages/ubuntu/trusty/chef-server-core_12.3.1-1_amd64.deb/download
```
https://packagecloud.io/chef/stable/packages/ubuntu/trusty/chef-server-core_12.3.1-1_amd64.deb/download
Create a DockerFile
```
FROM ubuntu:trusty

ADD  chef-server.core_12.3.1-1_amd64.deb

RUN deb -i chef-server.core_12.3.1-1_amd64.deb
```
