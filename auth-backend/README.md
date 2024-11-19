# Authentication Backend

A Spring Boot application that provides authentication services with user registration and login functionality.

## Prerequisites

- Java 17 or higher
- Maven 3.6.3 or higher
- MySQL 8.0 or higher

## Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd auth-backend
```

2. Create MySQL database:
```sql
CREATE DATABASE authdb;
```

3. Update database credentials in `src/main/resources/application.properties`

4. Build the project:
```bash
mvn clean install
```

5. Run the application:
```bash
mvn spring-boot:run
```

## API Endpoints

### Register User
```
POST /api/auth/register
Content-Type: application/json

{
    "username": "user",
    "password": "password"
}
```

### Login User
```
POST /api/auth/login
Content-Type: application/json

{
    "username": "user",
    "password": "password"
}
```

## Testing

Run tests using:
```bash
mvn test
```

## Features

- User registration with unique username validation
- Secure password hashing
- Login with attempt tracking
- Account locking after 3 failed attempts
- CORS configuration for frontend integration