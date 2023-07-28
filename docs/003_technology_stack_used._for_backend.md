# Technology Stack

**********************************************************************************

The technology stack used in the backend of the Compax web app is chosen to provide a robust, scalable, and high-performance foundation for handling API requests, managing data, and ensuring security. Here's an elaborate explanation of the technology stack components:

## Programming Language

### [Python](https://www.python.org) <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="30" height="30"/> </a>
*Python* is the programming language chosen for the backend development. It is known for its simplicity, readability, and versatility, making it a popular choice for web development tasks.

*FastAPI*, being a Python-based framework, allows developers to leverage Python's extensive ecosystem of libraries and packages for additional functionalities.

## Backend Server

### [FastAPI](https://fastapi.tiangolo.com) <a href="https://fastapi.tiangolo.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/fastapi-colored.svg" width="30" height="30" alt="Fast API" /></a>
*FastAPI* is the primary backend web framework used for building APIs with Python. It offers high performance, thanks to its asynchronous capabilities, making it suitable for handling a large number of concurrent requests.

*FastAPI* is designed to be easy to use and developer-friendly, enabling rapid development with automatic validation and interactive API documentation generation.

### [Uvicorn](https://www.uvicorn.org/) <a href="https://www.uvicorn.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/tomchristie/uvicorn/master/docs/uvicorn.png" width="30" height="30" alt="Fast API" /></a>

*Uvicorn* is an ASGI (Asynchronous Server Gateway Interface) server implementation used to run the FastAPI application.

*Uvicorn* provides high-performance asynchronous handling of requests, making it an excellent choice for FastAPI applications.

## Databases

### [PostgreSQL](https://www.postgresql.org) <a href="https://www.postgresql.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="postgresql" width="30" height="30"/> </a>

*PostgreSQL* is the database management system used to store and manage data for the Compax web app. It is an open-source, powerful, and scalable relational database.

*PostgreSQL* offers features like JSONB data type, which allows storing semi-structured data, making it suitable for scenarios where flexibility in data storage is needed.

### [Supabase](https://www.supabase.com/) <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" id="IconChangeColor" height="30" width="30"><title>Supabase</title><path d="M21.362 9.354H12V.396a.396.396 0 0 0-.716-.233L2.203 12.424l-.401.562a1.04 1.04 0 0 0 .836 1.659H12v8.959a.396.396 0 0 0 .716.233l9.081-12.261.401-.562a1.04 1.04 0 0 0-.836-1.66z" id="mainIconPathAttribute" fill="green"></path></svg>

*Supabase* is our primary soure for database also providing real-time capabilities and authentication services.

It can be used for features like real-time updates or user authentication, depending on the project requirements.

## CI/CD and Version Control

### [Docker](https://www.docker.com/) <a href="https://www.docker.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="30" height="30"/> </a>

*Docker* is used for containerizing the backend application, ensuring consistency and portability across different environments.

*Containerization* with Docker allows for easy deployment and scaling, making it a popular choice for modern web application development.

### [Git](https://git-scm.com/) <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="30" height="30"/> </a>

*Git* is used for version control, enabling collaborative development, and keeping track of changes in the source code.

The chosen technology stack ensures that the backend of the Compax web app is efficient, secure, and well-structured. It leverages the power of FastAPI and Python for handling API requests, PostgreSQL for data management, and JWT for secure authentication.

Additionally, the use of Docker enables seamless deployment and scaling, while Git allows for version control and easy collaboration among developers.
