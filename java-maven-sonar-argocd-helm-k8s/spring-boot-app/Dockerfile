# Use Java 17 base image
FROM madiva/openjdk17

# Install Maven
RUN apt-get update && \
    apt-get install -y maven && \
    apt-get clean

# Argument for artifact path
ARG artifact=target/spring-boot-web.jar

# Working directory inside the container
WORKDIR /opt/app

# Copy the built JAR into the container
COPY ${artifact} app.jar

# Default command to run the Spring Boot application
ENTRYPOINT ["java", "-jar", "app.jar"]
