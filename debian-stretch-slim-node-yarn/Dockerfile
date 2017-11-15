FROM debian:stretch-slim

LABEL maintainer="developer@nicolas-grevin.com"

RUN apt update && \
    apt install -y build-essential curl

RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - && \
    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

RUN apt install -y nodejs \
                   yarn

RUN apt clean && \
    apt autoclean && \
    apt autoremove && \
    rm -rf /var/lib/apt/lists/*

RUN groupadd -g 1000 node && \
    useradd -u 1000 -g 1000 node

