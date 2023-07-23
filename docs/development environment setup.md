# Development Environment Setup

Setting up a development environment for the backend of the Compax web app involves installing the necessary tools and dependencies to start building and testing the API using FastAPI and Python. Below is a step-by-step guide to setting up the development environment:

- **Install Python**:
   - Ensure that Python is installed on your system. FastAPI requires Python 3.7 or higher. You can download the latest version of Python from the official Python website (https://www.python.org/downloads/). Follow the installation instructions for your operating system.
   
- **Create a Virtual Environment (Optional)**:
    -  It's recommended to create a virtual environment for isolating the project's dependencies. This ensures that the dependencies for the Compax web app won't interfere with other projects.
   - To create a virtual environment, open your terminal or command prompt and run the following command:

   ```bash
   python -m venv compax-env
   ```

   This will create a new virtual environment named `compax-env`.

- **Activate the Virtual Environment**:
   - Activate the virtual environment to start using it. The activation steps depend on your operating system:

   - **Windows**:

   ```bash
   compax-env\Scripts\activate
   ```

   - **Mac / Linux**:

   ```bash
   source compax-env/bin/activate
   ```

- **Install Dependencies**:
   - With the virtual environment activated, navigate to the root directory of the backend project (where `pyproject.toml` is located) and install the required dependencies using `poetry`. If you haven't installed `poetry`, follow the installation instructions from the Poetry website (https://python-poetry.org/docs/#installation).
   - Run the following command to install the project dependencies:

   ```bash
   poetry install
   ```

   This will install all the required packages specified in the `pyproject.toml` file.

- **Run the Development Server**:
   - After installing the dependencies, you can run the development server using `uvicorn`, the ASGI server implementation.

   ```bash
   uvicorn main:app --reload
   ```

   This will start the FastAPI development server, and the API will be accessible at `http://127.0.0.1:8000`.

- **Testing the API**:
   - With the development server running, you can now test the API using tools like `curl`, Postman, or any API testing tool of your choice.
   - For interactive API documentation, open your web browser and go to `http://127.0.0.1:8000/docs`. This will display the automatically generated Swagger documentation, where you can explore the available endpoints and test them interactively.

- **Database Configuration**:
   - Ensure that you have PostgreSQL installed and running on your system. Create a new database for the Compax web app and configure the connection settings in the backend code (e.g., in a `.env` file).
   - Update the database settings in the backend code to point to your PostgreSQL database.

- **Implement Endpoints and Features**:
   - With the development environment set up, you can now start implementing the various endpoints and features required for the Compax web app. Use the provided Python files (`admin.py`, `auth.py`, `building.py`, etc.) as a starting point and customize them based on your project requirements.

- **Version Control**:
   - Use a version control system like Git to track changes in your code. Initialize a Git repository in the project directory and commit your code regularly.

By following these steps, you'll have a fully functional development environment set up for the backend of the Compax web app. You can now start building and testing the API, implementing the required endpoints, and working on other features of the web application.