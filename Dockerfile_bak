FROM ubuntu

MAINTAINER pbeniwal@yahoo.com

RUN apt update

RUN apt install -y curl

RUN mkdir /opt/tomcat/

WORKDIR /opt/tomcat

RUN curl -O https://mirrors.estointernet.in/apache/tomcat/tomcat-9/v9.0.33/bin/apache-tomcat-9.0.33.tar.gz

RUN gunzip apache-tomcat-9.0.33.tar.gz

RUN tar -xvf apache-tomcat-9.0.33.tar

RUN mv apache-tomcat-9.0.33/* /opt/tomcat/.

RUN apt install -y openjdk-8-jdk

COPY helloedureka.war /opt/tomcat/webapps/

CMD ["/opt/tomcat/bin/catalina.sh", "run"]
