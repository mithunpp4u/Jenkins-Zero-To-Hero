# Use Java 17 base image
FROM mithunpp4u/maven-mithun-docker-agent

# Argument for artifact path
ARG artifact=target/spring-boot-web.jar

# Working directory inside the container
WORKDIR /opt/app

# Copy the built JAR into the container
COPY ${artifact} app.jar

# Default command to run the Spring Boot application
ENTRYPOINT ["java", "-jar", "app.jar"]
