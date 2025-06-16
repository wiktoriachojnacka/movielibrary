# 🎬 MovieLibrary

A simple Java application with a MySQL database running in a Docker container. This demo project showcases the integration of Spring Boot, MySQL, and Docker.

## Technologies

- **Java 17**
- **Spring Boot**
- **MySQL**
- **Docker**
- **Postman** (for testing the API)

## How to Run the Project

1. **Clone the repository:**

   ```bash
   git clone https://github.com/wiktoriachojnacka/movielibrary.git
   cd movielibrary
   ```

2. **Build the project:**

  Make sure you have Maven and Docker installed. Then build the project:

   ```bash
   ./mvnw clean package
   ```

3. **Run the application in a Docker container:**

   If you have a docker-compose.yml file, you can run the app and database with:

   ```bash
   docker-compose up --build
   ```

 If you're running manually, start the MySQL database container first, then run the Spring Boot application, ensuring the connection settings in application.properties are correctly configured.

4. **Check if the application is running:**

  The app should be available at:

   ```
   http://localhost:8080
   ```

## Endpoints

| Method | Endpoint       | Description                         |
|--------|----------------|------------------------------|
| GET    | `/movies`      | Get a list of all movies         |
| POST   | `/movies`      | Add a new movie              |
| DELETE | `/movies/{id}` | Delete a movie by its ID       |

Test the API using Postman or any other HTTP client.

## Project Structure

```
movielibrary/
├── src/
│   └── main/
│       ├── java/
│       │   └── com/example/movielibrary/
│       │       ├── controller/
│       │       ├── model/
│       │       └── repository/
│       └── resources/
│           ├── application.properties
│           └── data.sql
├── pom.xml
├── Dockerfile
└── README.md
```
