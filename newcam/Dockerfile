FROM centos:6.9

RUN yum update -y
RUN yum install -y wget
RUN yum install -y tar

RUN mkdir package
WORKDIR package

VOLUME /backup/share/

ENV JAVA_HOME /package/java7
ENV CATALINA_HOME /package/tomcat7
ENV PATH $PATH:$JAVA_HOME/bin:$CATALINA_HOME/bin

EXPOSE 8080
EXPOSE 8009
EXPOSE 9088
