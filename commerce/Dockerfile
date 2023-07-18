# Use Ubuntu as the base image
FROM ubuntu:latest

# Install OpenJDK 17
RUN apt-get update && apt-get install -y openjdk-17-jdk

# Set Java environment variables
ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
ENV PATH=$PATH:$JAVA_HOME/bin

RUN apt-get -y install maven
RUN apt-get -y install ant

WORKDIR /commerce

CMD tail -f /dev/null