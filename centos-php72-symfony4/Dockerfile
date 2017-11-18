FROM centos:7

LABEL maintainer="developer@nicolas-grevin.com"
LABEL version=1.0.0

ENV INSTALL_OPTION="--nodocs --assumeyes"

RUN yum install --assumeyes wget

RUN wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && \
    wget https://rpms.remirepo.net/enterprise/remi-release-7.rpm && \
    rpm -Uvh remi-release-7.rpm epel-release-latest-7.noarch.rpm

RUN yum-config-manager --enable remi-php72 && \
    yum update php\*

RUN yum install --assumeyes php72

RUN yum remove --assumeyes wget && \
    yum clean all && \
    rm -rf /var/cache/yum
