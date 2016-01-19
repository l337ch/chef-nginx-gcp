FROM ubuntu:trusty

ENV	DEBIAN_FRONTEND noninteractive

ADD	run_chef_server /usr/local/bin/
ADD chef-server.deb /

RUN dpkg -i /chef-server.deb
RUN	dpkg-divert --local --rename --add /sbin/initctl
RUN	ln -sf /bin/true /sbin/initctl
RUN	/opt/opscode/embedded/bin/runsvdir-start & \
	chef-server-ctl reconfigure && \
	chef-server-ctl stop

ADD	. /usr/local/bin/
CMD	["run_chef_server"]

EXPOSE	443
