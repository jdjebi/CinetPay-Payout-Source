FROM openjdk:17-jdk-alpine3.14

RUN addgroup -S spring && adduser -S spring -G spring

USER spring:spring

ARG JAR_FILE=target/*.jar

COPY ${JAR_FILE} app.jar

EXPOSE 8070:8070

ENTRYPOINT ["java","-jar","/app.jar"]