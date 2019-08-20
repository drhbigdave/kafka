FROM myrepo/kafka_scala:v1
RUN yum -y update
RUN yum update -y \
  && yum install -y \
  epel-release \
  python-pip \
  java-1.8.0-openjdk \
  && yum clean all
RUN echo 'export JAVA_HOME=/usr/lib/jvm/jre-1.8.0-openjdk' | tee -a /etc/profile
RUN echo 'export JRE_HOME=/usr/lib/jvm/jre' | tee -a /etc/profile
RUN echo 'export KAFKA_HOME=/opt/kafka_2.12-2.2.0 | tee -a /etc/profile'
RUN echo 'export PATH=$KAFKA_HOME/bin/:$PATH | tee -a /etc/profile'
WORKDIR /usr/src/app
RUN source /etc/profile
COPY ./kafka_2.12-2.2.0 /opt/kafka_2.12-2.2.0
COPY ./zookeeper-3.4.14 /opt/zookeeper-3.4.14