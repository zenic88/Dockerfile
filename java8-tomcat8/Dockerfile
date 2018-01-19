FROM centos:latest
MAINTAINER zenic88

RUN yum update -y
RUN yum install -y wget
RUN yum install -y tar

RUN mkdir package
WORKDIR package

RUN wget -c --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.tar.gz
RUN tar -xvf jdk-*
RUN mv jdk1.8.131 java8

RUN wget http://apache.tt.co.kr/tomcat/tomcat-8/v8.0.48/bin/apache-tomcat-8.0.48.tar.gz
RUN tar -xvf apache-*
RUN mv apache-tomcat-8.0.48 tomcat8

ENV JAVA_HOME /package/java8
ENV CATALINA_HOME /package/tomcat8
ENV PATH $PATH:$JAVA_HOME/bin:$CATALINA_HOME/bin

EXPOSE 8080
EXPOSE 8009
