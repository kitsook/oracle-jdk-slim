# Oracle JDK 10 on Debian 9

FROM debian:9-slim

RUN apt-get update -q && \
    apt-get install -q -y --no-install-recommends gnupg dirmngr ca-certificates software-properties-common && \
    echo "deb http://ppa.launchpad.net/linuxuprising/java/ubuntu bionic main" >> /etc/apt/sources.list.d/linuxuprising-java.list && \
    apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 73C3DB2A && \
    apt-get update -q && \
    echo oracle-java10-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
    apt-get install -q -y --no-install-recommends oracle-java10-installer && \
    apt-get autoremove --purge -y && \
    apt-get clean && \
    rm -fR /var/cache/oracle-jdk10-installer

CMD ["bash"]
