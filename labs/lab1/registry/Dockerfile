FROM registry.access.redhat.com/rhel7
MAINTAINER Student <student@foo.io>

ADD ./custom.repo /etc/yum.repos.d/custom.repo

RUN yum -y install docker-registry --enablerepo=rhel-7-server-extras-rpms && yum clean all

EXPOSE 5000

ENTRYPOINT ["/usr/bin/registry"]

CMD ["serve", "/etc/docker-distribution/registry/config.yml"]
