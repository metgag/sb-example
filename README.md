## Example Spring Boot Application

### Overview

This project is a simple Spring Boot application that demonstrates basic CRUD operations for managing software engineer records. It follows a clean architecture with controller, service, and repository layers, providing a RESTful API for data interaction.

The project was inspired by the tutorial video available at [this link](https://www.youtube.com/watch?v=Cw0J6jYJtzw&t=238s) from the [Amigoscode YouTube channel](https://www.youtube.com/@amigoscode), which offers clear and practical lessons on Spring Boot development.

### Project Structure

```
.
├── pom.xml
├── src
│   ├── main
│   │   ├── java/com/metgag/example
│   │   │   ├── ExampleApplication.java
│   │   │   ├── SoftwareEngineerController.java
│   │   │   ├── SoftwareEngineerService.java
│   │   │   ├── SoftwareEngineerRepository.java
│   │   │   └── SoftwareEngineer.java
│   │   └── resources
│   │       ├── application.properties
│   │       ├── static/
│   │       └── templates/
│   └── test/java/com/metgag/example
│       └── ExampleApplicationTests.java
```

### Prerequisites

* Java 17 or later
* Maven 3.8+
* Docker (optional, for running services defined in `docker-compose.yml`)

### Running the Application

You can run the application in several ways:

#### Using Maven

```bash
mvn spring-boot:run
```

#### Using the Executable Jar

```bash
mvn clean package
java -jar target/example-0.0.1-SNAPSHOT.jar
```

### API Endpoints

| Method     | Endpoint                          | Description                          |
| ---------- | --------------------------------- | ------------------------------------ |
| **GET**    | `/api/v1/software-engineers`      | Retrieve all software engineers      |
| **GET**    | `/api/v1/software-engineers/{id}` | Retrieve a software engineer by ID   |
| **POST**   | `/api/v1/software-engineers`      | Create a new software engineer       |

### Configuration

Application settings such as database connection details are located in:

```
src/main/resources/application.properties
```

This file is typically excluded from version control for security and environment-specific reasons.

### Testing

To run tests:

```bash
mvn test
```
