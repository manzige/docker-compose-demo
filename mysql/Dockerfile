FROM mysql:5.7

MAINTAINER Tank <tankphper@gmail.com>

RUN /bin/ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

RUN apt-get update \
    && apt-get install -y \
    vim \ 
    curl \
    wget \
    zip \
    lsof \
    procps \
    && apt-get clean \
    && apt-get autoremove

COPY ./conf.d/my.cnf /etc/mysql/conf.d/custom.cnf

RUN chmod 644 /etc/mysql/conf.d/custom.cnf
