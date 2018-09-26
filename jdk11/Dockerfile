# Oracle JDK 11 on Debian 9

FROM debian:9-slim

RUN apt-get update -q && \
    apt-get install -q -y --no-install-recommends wget ca-certificates libasound2 && \
    cd /tmp && \
    wget --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/11+28/55eed80b163941c8885ad9298e6d786a/jdk-11_linux-x64_bin.deb && \
    dpkg -i jdk-11_linux-x64_bin.deb && \
    update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-11/bin/java 100 && \
    update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-11/bin/javac 100 && \
    rm -f /tmp/jdk-11_linux-x64_bin.deb

CMD ["bash"]
