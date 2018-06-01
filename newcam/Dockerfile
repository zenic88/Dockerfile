FROM centos:6.9

RUN yum update -y
RUN yum install -y wget
RUN yum install -y tar

WORKDIR package

ADD *.gz /package/

# 폴더에 있어야됨.
RUN mv apache-tomcat-7.0.63 tomcat
RUN mv jdk1.7.0_79 java7

COPY nMSC.war /package/tomcat/webapps/

VOLUME /backup/share/

ENV JAVA_HOME /package/java7
ENV CATALINA_HOME /package/tomcat
ENV PATH $PATH:$JAVA_HOME/bin:$CATALINA_HOME/bin

EXPOSE 8080
EXPOSE 8009
