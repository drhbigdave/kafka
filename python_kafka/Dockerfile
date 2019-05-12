FROM centos:latest
RUN yum -y update
RUN yum -y install epel-release
RUN yum -y install python-pip
RUN pip install --upgrade pip
RUN yum -y install java-1.8.0-openjdk
RUN echo 'export JAVA_HOME=/usr/lib/jvm/jre-1.8.0-openjdk' | tee -a /etc/profile
RUN echo 'export JRE_HOME=/usr/lib/jvm/jre' | tee -a /etc/profile
RUN source /etc/profile
RUN pip install kafka-python && yum clean all