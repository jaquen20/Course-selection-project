FROM openjdk:17-jdk-alpine
WORKDIR /app
COPY . .
RUN ./mvnw clean package -DskipTests
ENTRYPOINT ["java", "-jar", "target/your-app-name.jar"]
