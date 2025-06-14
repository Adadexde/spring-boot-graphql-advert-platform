# Spring Boot GraphQL Advert Platform

![GitHub release](https://img.shields.io/github/release/Adadexde/spring-boot-graphql-advert-platform.svg) ![GitHub issues](https://img.shields.io/github/issues/Adadexde/spring-boot-graphql-advert-platform.svg) ![GitHub stars](https://img.shields.io/github/stars/Adadexde/spring-boot-graphql-advert-platform.svg)

Welcome to the **Spring Boot GraphQL Advert Platform**! This project is designed to help users create and manage advertisements easily. Built on the powerful Spring Boot framework, this web platform provides a robust GraphQL API and ensures secure access through JWT-based authentication.

## Table of Contents

1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Getting Started](#getting-started)
4. [Usage](#usage)
5. [API Documentation](#api-documentation)
6. [Contributing](#contributing)
7. [License](#license)
8. [Contact](#contact)

## Features

- **User Registration**: Users can register and create their accounts.
- **Authentication**: Secure login with JWT tokens.
- **Ad Management**: Users can create, read, update, and delete advertisements.
- **GraphQL API**: Flexible and efficient data retrieval.
- **Responsive Design**: Works well on various devices.

## Technologies Used

- **Java**: The primary programming language.
- **Spring Boot**: Framework for building the backend.
- **GraphQL**: For efficient data querying.
- **Gradle**: Build automation tool.
- **JWT**: For secure user authentication.
- **HTML/CSS**: For the front-end interface.

## Getting Started

To get started with the Spring Boot GraphQL Advert Platform, follow these steps:

1. **Clone the Repository**: 
   ```bash
   git clone https://github.com/Adadexde/spring-boot-graphql-advert-platform.git
   cd spring-boot-graphql-advert-platform
   ```

2. **Build the Project**:
   Make sure you have Gradle installed. Then run:
   ```bash
   ./gradlew build
   ```

3. **Run the Application**:
   Start the application using:
   ```bash
   ./gradlew bootRun
   ```

4. **Access the API**:
   Open your browser and go to `http://localhost:8080/graphql` to access the GraphQL interface.

For the latest releases, check out the [Releases section](https://github.com/Adadexde/spring-boot-graphql-advert-platform/releases).

## Usage

Once the application is running, you can use the GraphQL API to manage advertisements. Here are some example queries and mutations:

### User Registration

To register a new user, use the following mutation:

```graphql
mutation {
  registerUser(username: "newUser", password: "securePassword") {
    id
    username
  }
}
```

### User Login

To log in and receive a JWT token, use:

```graphql
mutation {
  login(username: "existingUser", password: "securePassword") {
    token
  }
}
```

### Create Advertisement

To create a new advertisement:

```graphql
mutation {
  createAd(title: "My First Ad", description: "This is a great ad!", price: 100) {
    id
    title
    description
  }
}
```

### Fetch Advertisements

To fetch all advertisements:

```graphql
query {
  ads {
    id
    title
    description
    price
  }
}
```

## API Documentation

The API is built using GraphQL, allowing for flexible and efficient data queries. For detailed API documentation, you can explore the GraphQL interface at `http://localhost:8080/graphql`.

### Authentication

JWT tokens are used for secure authentication. After logging in, include the token in the Authorization header for subsequent requests:

```
Authorization: Bearer <your_token>
```

## Contributing

Contributions are welcome! If you have suggestions or improvements, please create an issue or submit a pull request. 

1. Fork the repository.
2. Create your feature branch:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add some feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/YourFeature
   ```
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries, please reach out via GitHub or open an issue in the repository.

For the latest releases, visit the [Releases section](https://github.com/Adadexde/spring-boot-graphql-advert-platform/releases).

---

Thank you for checking out the Spring Boot GraphQL Advert Platform! We hope you find it useful for your advertisement management needs.