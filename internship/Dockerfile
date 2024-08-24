FROM openjdk:17-jdk-alpine
WORKDIR /app
ADD target/internship-0.0.1-SNAPSHOT.jar internship-0.0.1-SNAPSHOT.jar
COPY . .
RUN ./mvnw clean package -DskipTests
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "target/internship-0.0.1-SNAPSHOT.jar"]