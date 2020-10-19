FROM ubuntu:18.04

ENV APP /home/app
ENV WDir /home/build
RUN mkdir -p "$APP"
RUN mkdir -p "$WDir"

WORKDIR $WDir

RUN apt-get update && apt-get install -y default-jdk git maven \
&& git clone https://github.com/zi10ge/HW12.git \
&& mvn package -f ./HW12/App42PaaS-Java-MySQL-Sample/pom.xml

RUN cp "$WDir/HW12/App42PaaS-Java-MySQL-Sample/target/app_name.war" "$APP/app.war"