# Use OpenJDK 17 base image (Alpine for small size)
FROM openjdk:17-alpine

# Create the application directory
RUN mkdir -p /opt/app

# Set environment variable for project path
ENV PROJECT_HOME=/opt/app

# Copy the built JAR file into the container
COPY target/spring-petclinic-rest-3.4.3.jar $PROJECT_HOME/spring-petclinic-rest.jar

# Set the working directory
WORKDIR $PROJECT_HOME

# Expose port 8080 (used by Spring Boot by default)
EXPOSE 9966

# Command to run the application
CMD ["java", "-jar", "spring-petclinic-rest.jar"]
