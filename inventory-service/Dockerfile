# Use official Java 17 JDK as base image
FROM eclipse-temurin:17-jdk-alpine

# Set working directory inside the container
WORKDIR /app

# Copy Maven build files
COPY pom.xml .
COPY src ./src

# Build the application
RUN ./mvnw clean package -DskipTests || mvn clean package -DskipTests

# Expose port (must match application.yml)
EXPOSE 8082

# Run the Spring Boot application
ENTRYPOINT ["java", "-jar", "target/inventory-service-0.0.1.jar"]
