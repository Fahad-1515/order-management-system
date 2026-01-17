# Use official Java 17 JDK as base image
FROM eclipse-temurin:17-jdk-alpine

# Set working directory inside the container
WORKDIR /app

# Copy Maven build files
COPY pom.xml .
COPY src ./src

# Build the application (skip tests to speed up Docker build)
RUN ./mvnw clean package -DskipTests || mvn clean package -DskipTests

# Expose the port your service will run on
EXPOSE 8081

# Run the Spring Boot application
ENTRYPOINT ["java", "-jar", "target/order-service-0.0.1.jar"]
