FROM openjdk:8-jdk-alpine

LABEL maintainer="avinash@outlook.com"

# Add a volume pointing to /tmp
VOLUME /tmp

# Make port 8080 available to the world outside this container
EXPOSE 8761

# The application's jar file
ARG JAR_FILE=target/service-discovery-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} app-service-discovery.jar

# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app-service-discovery.jar"]