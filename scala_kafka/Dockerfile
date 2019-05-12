FROM centos:latest
RUN yum -y update
RUN yum update -y \
  && yum install -y \
  epel-release \
  python-pip \
  java-1.8.0-openjdk \
  && yum clean all
RUN echo 'export JAVA_HOME=/usr/lib/jvm/jre-1.8.0-openjdk' | tee -a /etc/profile
RUN echo 'export JRE_HOME=/usr/lib/jvm/jre' | tee -a /etc/profile
WORKDIR /usr/src/app
RUN source /etc/profile
COPY /dockershare/kafka_2.12-2.2.0 /opt/kafka_2.12-2.2.0
COPY /dockershare/scala-2.12.8.rpm .
RUN yum -y install scala-2.12.8.rpm