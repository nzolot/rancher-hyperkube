FROM rancher/hyperkube:v1.20.15-rancher1

RUN curl 'https://keyserver.ubuntu.com/pks/lookup?op=get&search=0xf7c73fcc930ac9f83b387a5613e01b7b3fe869a9' | apt-key add - \
    && echo deb http://ppa.launchpad.net/gluster/glusterfs-10/ubuntu focal main > /etc/apt/sources.list.d/gluster-ubuntu-glusterfs-10-focal.list

RUN apt-get -y update \
    && apt-get -y install systemd \
    && apt-get install -y glusterfs-client=10*
