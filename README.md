# Demo Spring Boot Application

## Overview
This is a simple Spring Boot application packaged into a Docker container. The application is built using Maven and Java JDK 17.

## Prerequisites
- Java JDK 17
- Maven 3.8.4 or later
- Docker

## Project Structure
- `src/main/java/com/example/demo/Application.java` - The main application class.
- `pom.xml` - The Maven configuration file.
- `Dockerfile` - The Docker configuration file for building the container image.

## Building the Project
To build the project, run the following command:
```sh
mvn clean package -DskipTests
```

## Creating a Docker Image
To create a Docker image for the application, run the following command in the project's root directory:
```sh
docker build -t my-spring-boot-app .
```

## Running the Docker Container
To run the Docker container, use the following command:
```sh
docker run -p 8080:8080 my-spring-boot-app
```
The application will be accessible at `http://localhost:8080`.

## Dockerfile Overview
The Dockerfile consists of the following stages:
1. **Build Stage**: Uses the official Maven image to compile the project and create the JAR file.
2. **Runtime Stage**: Uses the OpenJDK image to run the application.

## License
This project is licensed under the MIT License.

---
