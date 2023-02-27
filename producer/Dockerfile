FROM openjdk:11-jdk-slim

COPY build/libs/producer-1.0-SNAPSHOT.jar /producer-app.jar

ENTRYPOINT ["java","-jar","/producer-app.jar"]
