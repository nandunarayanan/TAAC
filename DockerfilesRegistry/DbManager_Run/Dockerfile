FROM ubuntu:bionic

RUN apt-get update && \
	apt-get install -y build-essential git wget software-properties-common

RUN add-apt-repository ppa:openjdk-r/ppa

RUN apt -y install openjdk-14-jdk

RUN export JAVA_HOME=/usr/lib/jvm/openjdk-14-jdk

RUN export PATH=$PATH:$JAVA_HOME/bin

RUN java -version 	

RUN apt -y install maven

RUN mvn -version

WORKDIR /src/Android_DB_Insert

CMD chmod 777 dbmanager.sh && ./dbmanager.sh
