FROM centos:7

LABEL maintainer="developer@nicolas-grevin.com"

RUN yum install -y gcc-c++ \
                   make \
                   wget

RUN curl --silent --location https://rpm.nodesource.com/setup_8.x | bash - && \
    wget https://dl.yarnpkg.com/rpm/yarn.repo -O /etc/yum.repos.d/yarn.repo

RUN yum install -y nodejs \
                   yarn

WORKDIR /src
