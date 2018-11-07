FROM hub.slyak.com/bamboo
USER root:root
RUN apt-get update \
    && apt-get -y install openssh-server \
    && apt-get -y install vim \
    && apt-get -y install wget \
    && wget http://mirror.nus.edu.sg/apache/maven/maven-3/3.3.9/binaries/apache-maven-3.3.9-bin.tar.gz \
    && mkdir /usr/lib/maven \
    && tar -zxf apache-maven-3.3.9-bin.tar.gz  -C /usr/lib/maven
COPY maven.sh /etc/profile.d/