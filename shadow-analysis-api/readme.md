# Shadow Analysis Repository

## Overview

The Shadow Analysis repository is a Python-based application designed to perform shadow calculations on Digital Surface Model (DSM) data. This application can calculate shadows based on provided azimuth, altitude, DSM, and scale parameters. It can also retrieve shadow analysis results using a unique document ID.

## Technologies Used

- **Python**: Primary programming language for the application.
- **Docker**: Used for creating isolated environments to run the application.
- **Flask**: A micro web framework written in Python, possibly used for the API.
- **Gunicorn**: A Python WSGI HTTP Server for UNIX, used in conjunction with Flask.
- **Pip**: A package installer for Python, used to manage software packages.
- **AWS (Amazon Web Services)**: Cloud computing platform used for hosting services and potentially for other cloud-based functionalities. (Specify the AWS services used, such as EC2 for hosting, S3 for storage, etc.)

## Repository Contents

- **Dockerfile**: Instructions for creating a Docker container for the application.
- **requirements.txt**: Lists all Python dependencies for the application.
- **run.py**: The main Python script to run the application.
- **shadow_analysis**: A directory containing the application's modules and sub-components.
- **.ini, .gitignore, .dockerignore**: Configuration files for various purposes.
- **app.log**: Log file for the application.
- **readme.md**: Documentation file (this file).

## Installation and Setup

### Using Docker

1. **Build the Docker Image**
   - Ensure Docker is installed on your system.
   - Navigate to the repository's root directory.
   - Build the Docker image using the provided Dockerfile:
     ```
     docker build -t shadow_analysis .
     ```

2. **Run the Docker Container**
   - Once the image is built, you can start the container with:
     ```
     docker run -p 5001:5001 shadow_analysis
     ```
   - This command runs the container and maps the application's port 5001 to the same port on the host machine.

### Manual Setup

1. **Install Python Dependencies**
   - Ensure Python is installed on your system.
   - Install the required Python packages:
     ```
     pip install -r requirements.txt
     ```

2. **Run the Application**
   - Run `run.py` using Python:
     ```
     python run.py
     ```

## API Usage

The base URL for all API endpoints is: `http://localhost:5001/api/v1/shadow_analysis/` (when running locally).

### Endpoints

- **Test Endpoint**: To check if the API is working.
- **Calculate Shadow**: For performing shadow calculations.
- **Retrieve Results**: To get the results using a document ID.

Refer to the existing `readme.md` file in`documentation` directory for detailed API documentation and examples.

---

