# Oracle JDK 11 on Debian 9

FROM debian:9-slim

RUN apt-get update -q && \
    apt-get install -q -y --no-install-recommends wget ca-certificates libasound2 && \
    cd /tmp && \
    wget --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/11.0.2+9/f51449fcd52f4d52b93a989c5c56ed3c/jdk-11.0.2_linux-x64_bin.deb && \
    dpkg -i jdk-11.0.2_linux-x64_bin.deb && \
    update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-11.0.2/bin/java 100 && \
    update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-11.0.2/bin/javac 100 && \
    rm -f /tmp/jdk-11.0.2_linux-x64_bin.deb

CMD ["bash"]
