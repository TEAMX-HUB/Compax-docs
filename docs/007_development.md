# Project Development

Setting up a development environment for the backend of the Compax web app involves installing the necessary tools and dependencies to start building and testing the API using FastAPI and Python. Below is a step-by-step guide to setting up the development environment:

## Dependencies

*****************************************************************************

Ensure that Python is installed on your system. FastAPI requires Python 3.9 or higher. You can download the latest version of Python from the official Python website (<https://www.python.org/downloads/>). Follow the installation instructions for your operating system. You would need a project dependency and packaging management to efficiently be able to manage all dependencies that's why Poetry is our preferred tool for managing this project.

**Install Dependencies**:

It's recommended to create a virtual environment for isolating the project's dependencies. This ensures that the dependencies for the Compax web app won't interfere with other projects.

Navigate to the root directory of the project (where `pyproject.toml` is located) and install the required dependencies using Poetry. If you haven't installed Poetry, follow the installation instructions from the Poetry website (<https://python-poetry.org/docs/#installation>).

Create a virtual environment with Poetry by invoking the following command: `poetry shell`

This would create `.venv` directory or cached virtual environment depending on the configurations set for the tool. While your project environment has been successfully created, poetry will automatically try to activate the environment. If you do not see any such thing; proceed to activate the environment using the following commands.

**Windows**:   `compax-env\Scripts\activate`

**Mac / Linux**:    `source compax-env/bin/activate`

Run the following command to install the project dependencies:  `poetry install`

This will install all the required packages specified in the `pyproject.toml` file.

*****************************************************************************

**Run Server**:

After installing the dependencies, you can run the development server using `uvicorn`, the ASGI server implementation.

`uvicorn main:app --reload`

This will start the FastAPI development server, and the API will be accessible at `http://127.0.0.1:8000`.

**Testing**:
  
With the development server running, you can now test the API using tools like `curl`, Postman, or any API testing tool of your choice. For an interactive API documentation, open your web browser and go to `http://127.0.0.1:8000/api/bare/docs`. This will display the automatically generated Swagger documentation, where you can explore the available endpoints and test them interactively.

## Connecting Databases

*****************************************************************************

**Database Configuration**:

Ensure that you have PostgreSQL installed and running on your system or in a docker instance or on a remote database instance (because we used Supabase for all our PostgreSQL database interactions). To communicate with your database, a connection url or the database details are usually stored in an `.env` as show below and retrieved for any level of interaction.

```toml
ENV_NAME='development'
SUPABASE_CLIENT_URL='client_url_authentication'
SUPABASE_CLIENT_KEY='client_anon_key_authentication'
DB_URL='supabase_instance_dsn'
DB_NAME='supabase'
DB_USER='supabase'
DB_PASSWORD='very_long_password'
DB_HOST='supabase_instance_link'
DB_PORT='normal_port'

```

Update the database settings in the backend code to point to your PostgreSQL database. The information is then retrieved from the **gitignored `.env`** and passed along to anywhere it is needed in the code with a cache wrapper.

```python
from functools import lru_cache
from pathlib import Path

from pydantic import BaseSettings

cwd = Path.cwd()
base_env = cwd / ".env"
prod_env = cwd / "prod.env"


class Settings(BaseSettings):
    env_name: str = ""
    supabase_client_url: str = ""
    supabase_client_key: str = ""
    db_url: str = ""
    db_name: str = ""
    db_user: str = ""
    db_port: int = 0
    db_password: str = ""
    db_host: str = ""

    class Config:
        # allows the import of environment variables from .env
        # env file has variables included as attributes in
        # this class and more. you can decide to go with the
        # default preset used above or set your own .env file
        env_file = base_env
        env_file_encoding = "utf-8"


@lru_cache
def get_settings() -> Settings:
    settings = Settings()
    return settings
```

**Implement Endpoints and Features**:
  
With the development environment set up, you can now start implementing the various endpoints and features required for the Compax web app. Use the provided Python files (`admin.py`, `auth.py`, `building.py`, etc.) as a starting point and customize them based on your project requirements.

**Version Control**:
  
Use a version control system like Git to track changes in your code. Initialize a Git repository in the project directory and commit your code regularly.

By following these steps, you'll have a fully functional development environment set up for the backend of the Compax web app. You can now start building and testing the API, implementing the required endpoints, and working on other features of the web application.
