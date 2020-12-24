FROM fedora:33
RUN yum -y update
RUN yum -y install podman buildah
RUN sed -i -e s/^#mount_program/mount_program/ /etc/containers/storage.conf
COPY containers.conf /etc/containers/containers.conf
