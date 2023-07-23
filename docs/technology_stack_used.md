# Technology Stack Used
**********************************************************************************

The technology stack used in the backend of the Compax web app is chosen to provide a robust, scalable, and high-performance foundation for handling API requests, managing data, and ensuring security. Here's an elaborate explanation of the technology stack components:

## FastAPI:

  - *FastAPI* is the primary backend web framework used for building APIs with Python. It offers high performance, thanks to its asynchronous capabilities, making it suitable for handling a large number of concurrent requests.

 - *FastAPI* is designed to be easy to use and developer-friendly, enabling rapid development with automatic validation and interactive API documentation generation.

## Python:

-   *Python* is the programming language chosen for the backend development. It is known for its simplicity, readability, and versatility, making it a popular choice for web development tasks.

- *FastAPI*, being a Python-based framework, allows developers to leverage Python's extensive ecosystem of libraries and packages for additional functionalities.

## PostgreSQL:

- *PostgreSQL* is the database management system used to store and manage data for the Compax web app. It is an open-source, powerful, and scalable relational database.

- *PostgreSQL* offers features like JSONB data type, which allows storing semi-structured data, making it suitable for scenarios where flexibility in data storage is needed.

## JSON Web Tokens (JWT):

- For *authentication*, the backend uses JSON Web Tokens (JWT). JWT is a stateless authentication mechanism that allows securely transmitting information between parties as JSON objects.

- *JWT tokens* are used to verify the identity of users and grant access to protected endpoints, ensuring secure communication between the frontend and backend.

## Docker:

- *Docker* is used for containerizing the backend application, ensuring consistency and portability across different environments.

- *Containerization* with Docker allows for easy deployment and scaling, making it a popular choice for modern web application development.

## Uvicorn:

- *Uvicorn* is an ASGI (Asynchronous Server Gateway Interface) server implementation used to run the FastAPI application.

- *Uvicorn* provides high-performance asynchronous handling of requests, making it an excellent choice for FastAPI applications.

## Supabase (Optional):

- *Supabase* is an optional addition to the technology stack, providing real-time capabilities and authentication services.

- It can be used for features like real-time updates or user authentication, depending on the project requirements.

## Git:

- *Git* is used for version control, enabling collaborative development, and keeping track of changes in the source code.

- The chosen technology stack ensures that the backend of the Compax web app is efficient, secure, and well-structured. It leverages the power of FastAPI and Python for handling API requests, PostgreSQL for data management, and JWT for secure authentication. 

- Additionally, the use of Docker enables seamless deployment and scaling, while Git allows for version control and easy collaboration among developers.