# Database Design and Schema

The database design and schema for the Compax web app are crucial components that define the structure and organization of data within the application. A well-designed database schema ensures efficient data storage, retrieval, and integrity. Below is an elaboration of the database design and schema for the Compax web app:

-  **Entity-Relationship Diagram (ERD)**:

   An Entity-Relationship Diagram (ERD) is a visual representation of the database schema, showing the entities (tables) and their relationships. The ERD for the Compax web app might include the following entities:

   - **Users**: Represents information about the users of the application, including regular users, administrators, and exam officers. It stores user details such as username, email, password (hashed), role, and other relevant information.

   - **Buildings**: Contains details about the different buildings available within the educational institution. Information may include building name, address, capacity, etc.

   - **Classrooms**: Stores information about individual classrooms within the buildings. It may include attributes like classroom number, seating capacity, facilities, and the associated building.

   - **Laboratories**: Similar to classrooms, this entity stores details about laboratories, such as lab number, equipment, capacity, and the corresponding building.

   - **Offices**: Contains information about offices within the institution, such as office number, occupant, contact details, etc.

   - **Ratings**: Stores ratings and reviews given by users for classrooms and laboratories. It may include attributes like user ID, classroom/laboratory ID, rating value, review text, etc.

   - **Bookings**: Tracks bookings made by users for specific classrooms or laboratories. It includes details like user ID, classroom/laboratory ID, booking date, start time, end time, and status.

   The ERD provides a clear visualization of the relationships between different entities and helps in understanding how data is interconnected within the database.

- **Table Structure and Data Types**:

   The table structure for each entity in the database is defined by specifying the columns (attributes) and their corresponding data types. For example:

   - **Users Table**:
     - `id`: Primary key, auto-incremented integer.
     - `username`: Unique string, used for user identification.
     - `email`: Unique email address of the user.
     - `password_hash`: Hashed representation of the user's password for security.
     - `role`: Enum field representing the user's role (regular, admin, exam officer).
     - `created_at`: Timestamp indicating when the user account was created.
     - `updated_at`: Timestamp indicating the last update to the user account.

   - **Classrooms Table**:
     - `id`: Primary key, auto-incremented integer.
     - `classroom_number`: String representing the classroom number or identifier.
     - `capacity`: Integer specifying the seating capacity of the classroom.
     - `building_id`: Foreign key referencing the ID of the associated building.

   - **Bookings Table**:
     - `id`: Primary key, auto-incremented integer.
     - `user_id`: Foreign key referencing the ID of the user making the booking.
     - `classroom_id`: Foreign key referencing the ID of the booked classroom.
     - `booking_date`: Date when the booking was made.
     - `start_time`: Time of the booking's start.
     - `end_time`: Time of the booking's end.
     - `status`: Enum field indicating the booking status (confirmed, pending, canceled, etc.).

   The choice of data types for each column ensures that the database efficiently stores and retrieves the data, while also enforcing data integrity constraints.

- **Normalization and Data Integrity**:

   Database normalization is applied to ensure data integrity and to reduce data redundancy. The schema is organized into multiple tables, with each table focused on a specific entity. Relationships between entities are established using foreign keys, maintaining referential integrity.

- **Indexes and Performance Optimization**:

   Proper indexing is essential for improving query performance. Indexes are created on columns that are frequently used for filtering or searching data, such as the user ID, building ID, classroom ID, etc. Additionally, unique constraints and primary keys help maintain data uniqueness and integrity.

- **Real-time Data (Supabase, Optional)**:

   If the application requires real-time data updates, features like real-time notifications for bookings or reviews, Supabase can be used as an optional addition to the database stack.

The database design and schema should be carefully planned and optimized to meet the specific requirements of the Compax web app. Regular backups and maintenance procedures should be implemented to ensure data reliability and security.