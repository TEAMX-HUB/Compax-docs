# Error Handling

*****************************************************************************

Error handling and logging are critical aspects of the backend development process, ensuring that the Compax web app can identify, handle, and log errors effectively. Proper error handling provides meaningful feedback to users and helps developers identify and fix issues quickly. Here's an elaboration on error handling and logging for the backend of the Compax web app:

- ## Custom Error Classes

```python

from fastapi import HTTPException

class CompaxException(HTTPException):
    def __init__(self, status_code: int, detail: str):
        super().__init__(status_code, detail=detail)

class BuildingNotFoundException(CompaxException):
    def __init__(self, building_id: str):
        detail = f"Building with ID {building_id} not found."
        super().__init__(status_code=404, detail=detail)

class ClassroomNotFoundException(CompaxException):
    def __init__(self, classroom_id: str):
        detail = f"Classroom with ID {classroom_id} not found."
        super().__init__(status_code=404, detail=detail)

class LaboratoryNotFoundException(CompaxException):
    def __init__(self, laboratory_id: str):
        detail = f"Laboratory with ID {laboratory_id} not found."
        super().__init__(status_code=404, detail=detail)

class OfficeNotFoundException(CompaxException):
    def __init__(self, office_id: str):
        detail = f"Office with ID {office_id} not found."
        super().__init__(status_code=404, detail=detail)

class UserNotFoundException(CompaxException):
    def __init__(self, message: str):
        detail = f"{message}"
        super().__init__(status_code=404, detail=detail)

class UserReferenceFoundException(CompaxException):
    def __init__(self, ref: int):
        detail = f"User with Reference {int} not found."
        super().__init__(status_code=404, detail=detail)

class UserNameNotFoundException(CompaxException):
    def __init__(self, username: str):
        detail = f"User with name {username} not found."
        super().__init__(status_code=404, detail=detail)

class AuthInvalidCredentialsException(CompaxException):
    def __init__(self):
        super().__init__(
            status_code=401,
            detail="Invalid credentials. "
            + "User might exist. User with reference might exist. "
            + "User year group might be Incorrect",
        )

class InvalidRatingException(CompaxException):
    def __init__(self):
        super().__init__(
            status_code=401,
            detail="Invalid credentials. Details Provided might incorrect!",
        )

class UnauthorizedException(CompaxException):
    def __init__(self):
        super().__init__(status_code=403, detail="Unauthorized access.")

class BookingNotFoundException(CompaxException):
    def __init__(self, booking_id: str):
        detail = f"Booking with ID {booking_id} not found."
        super().__init__(status_code=404, detail=detail)

```

- ## Global Exception Handler Middleware

  - Implement a global exception handler middleware to catch unhandled exceptions and provide consistent error responses to the client.

- ## Logging

  - Implement logging to record application events, errors, and debugging information. Use Python's built-in `logging` module or third-party libraries like `structlog` to handle logging effectively.

- ## Request and Response Logging

  - Consider logging incoming requests and outgoing responses to understand application flow and debug issues.

- ## Handling Expected Errors

  - For known and expected errors, raise custom error classes with appropriate status codes and error details.

- ## Unit Tests for Error Handling

  - Write unit tests to ensure that the error handling and responses are working as expected.

- ## Sensitive Information Handling

  - Ensure that error responses do not expose sensitive information that could be used for malicious purposes.

By implementing robust error handling and logging in the backend, the Compax web app can provide informative error responses to clients, facilitate debugging, and enhance the overall reliability and user experience. Proper logging helps identify potential issues early and enables developers to respond quickly to errors, improving the stability and security of the application.
