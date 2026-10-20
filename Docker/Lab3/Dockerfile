FROM maven:3.9-eclipse-temurin-17-alpine

WORKDIR /app

RUN addgroup -S appgroup && adduser -S appuser -G appgroup

COPY . .

RUN chown -R appuser:appgroup /app

RUN mvn package

CMD ["java", "-jar", "target/calculator.jar"]

USER appuser

EXPOSE 8080
