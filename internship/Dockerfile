FROM openjdk:17-jdk-alpine
WORKDIR /app
ADD target/backend-docker.jar backend-docker.jar
COPY . .
RUN ./mvnw clean package -DskipTests
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/backend-docker.jar"]

