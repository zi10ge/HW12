FROM maven:alpine

WORKDIR /app/
RUN apk update git;\
    apk add --no-cache git ;\
    git clone https://github.com/zi10ge/HW12.git
WORKDIR /app/HW12/App42PaaS-Java-MySQL-Sample/
RUN mvn install
