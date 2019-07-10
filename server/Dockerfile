#Very similar to the springboot hello world Dockerfile
FROM maven as build
WORKDIR /build
COPY . .
RUN mvn clean package
FROM java:8
COPY --from=build /build/target/Spring_Day_Two-0.0.1-SNAPSHOT.jar /opt/app.jar
ENTRYPOINT ["java", "-jar", "/opt/app.jar"]
