# Architecture and System Design

**********************************************************************************

The backend architecture of the Compax web app follows a layered and modular approach to ensure maintainability, scalability, and separation of concerns.

## Layers

- Presentation Layer: Handles the incoming HTTP requests and outgoing HTTP responses. It interacts with the frontend and exposes the API endpoints.
- Business Layer: Contains the business logic of the application, including handling user authentication, classroom search, booking management, and user profile management.
- Data Access Layer: Responsible for interacting with the database. It includes functions to perform CRUD operations and retrieve data using an ORM library such as SQLAlchemy.
- Database Layer: Represents the chosen database system (e.g., SQLite or PostgreSQL) and stores the application's data.

## System Components

- API Router: Receives the incoming requests and directs them to the appropriate API handler functions based on the requested endpoint.
- API Handlers: Implements the logic for each API endpoint. It validates incoming requests, performs necessary actions, and returns appropriate responses.
- Authentication Middleware: Intercepts and validates requests to ensure the user is authenticated and authorized to access protected endpoints.
- Data Models: Defines the object-relational mapping for the entities (e.g., User, Classroom, Booking) using an ORM library. It represents the database tables and relationships.
