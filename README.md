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
Creating the chef server standalone running in a Docker container:

Download the chef server package from chef.io  into
the docker path under this project
```bash
curl -o docker/chef-server.deb -L https://packagecloud.io/chef/stable/packages/ubuntu/trusty/chef-server-core_12.3.1-1_amd64.deb/download
```
