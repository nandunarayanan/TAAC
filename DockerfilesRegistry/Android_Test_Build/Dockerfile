 FROM ubuntu:bionic

RUN apt-get update && \
	apt-get install -y build-essential git wget software-properties-common

RUN export SAUCE_USERNAME="sachinsk5526"
RUN export SAUCE_ACCESS_KEY="910af542886e46668c2481e0b1ec436f"

RUN add-apt-repository ppa:openjdk-r/ppa
RUN apt -y install openjdk-14-jdk

RUN export JAVA_HOME=/usr/lib/jvm/openjdk-14-jdk

RUN export PATH=$PATH:$JAVA_HOME/bin

RUN java -version 	

RUN apt -y install maven

RUN mvn -version

WORKDIR /src/AndroidTest/Test_Mobile_Andriod_demo_docker/

#COPY AndroidBuild.sh .

#RUN chmod 777 AndroidBuild.sh

#CMD ./AndroidBuild.sh
CMD mvn clean
