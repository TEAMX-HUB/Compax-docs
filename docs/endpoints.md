# Endpoints for the Compax App
**********************************************************************************

Based on the provided Python files, here are the updated endpoints for the Compax web app:

- admin.py:

    - `GET /admin/users`: Retrieves a list of users for administrative purposes.
    - `PUT /admin/users/{id}`: Updates the details of a specific user for administrative purposes.

- auth.py:

    - `POST /auth/register`: Registers a new user.
    - `POST /auth/login`: Authenticates and logs in a user.
    - `POST /auth/logout`: Logs out a user.

- building.py:

    - `GET /buildings`: Retrieves a list of available buildings.
    - `GET /buildings/{id}`: Retrieves detailed information about a specific building.
    - `POST /buildings`: Creates a new building.
    - `PUT /buildings/{id}`: Updates the details of a specific building.
    - `DELETE /buildings/{id}`: Deletes a specific building.

- classroom.py:

    - `GET /classrooms`: Retrieves a list of available classrooms.
    - `GET /classrooms/{id}`: Retrieves detailed information about a specific classroom.
    - `POST /classrooms`: Creates a new classroom.
    - `PUT /classrooms/{id}`: Updates the details of a specific classroom.
    - `DELETE /classrooms/{id}`: Deletes a specific classroom.

- laboratory.py:

    - `GET /laboratories`: Retrieves a list of available laboratories.
    - `GET /laboratories/{id}`: Retrieves detailed information about a specific laboratory.
    - `POST /laboratories`: Creates a new laboratory.
    - `PUT /laboratories/{id}`: Updates the details of a specific laboratory.
    - `DELETE /laboratories/{id}`: Deletes a specific laboratory.

- office.py:

    - `GET /offices`: Retrieves a list of available offices.
    - `GET /offices/{id}`: Retrieves detailed information about a specific office.
    - `POST /offices`: Creates a new office.
    - `PUT /offices/{id}`: Updates the details of a specific office.
    - `DELETE /offices/{id}`: Deletes a specific office.

- ratings.py:

    - `GET /ratings/classrooms/{id}`: Retrieves ratings and reviews for a specific classroom.
    - `GET /ratings/laboratories/{id}`: Retrieves ratings and reviews for a specific laboratory.
    - `POST /ratings/classrooms/{id}`: Adds a new rating and review for a specific classroom.
    - `POST /ratings/laboratories/{id}`: Adds a new rating and review for a specific laboratory.

- schedule.py:

    - `GET /schedule/classrooms/{id}`: Retrieves the schedule of bookings for a specific classroom.
    - `GET /schedule/laboratories/{id}`: Retrieves the schedule of bookings for a specific laboratory.
    - `POST /schedule/classrooms/{id}`: Creates a new booking for a specific classroom.
    - `POST /schedule/laboratories/{id}`: Creates a new booking for a specific laboratory.
    - `PUT /schedule/classrooms/{id}/{booking_id}`: Updates the details of a specific booking for a classroom.
    - `PUT /schedule/laboratories/{id}/{booking_id}`: Updates the details of a specific booking for a laboratory.
    - `DELETE /schedule/classrooms/{id}/{booking_id}`: Deletes a specific booking for a classroom.
    - `DELETE /schedule/laboratories/{id}/{booking_id}`: Deletes a specific booking for a laboratory.

- user.py:

    - `GET /users/{id}`: Retrieves detailed information about a specific user.
    - `PUT /users/{id}`: Updates the details of a specific user.

- errors.py:

    - `GET /errors/{error_code}`: Retrieves detailed information about a specific error code.