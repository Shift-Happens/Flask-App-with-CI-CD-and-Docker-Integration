# Flask App with CI/CD and Docker Integration

## Overview

This project is a simple Flask application that displays "Hello, World!" on the home page. The project is set up with continuous integration and continuous deployment (CI/CD) using GitHub Actions, and can be containerized and run using Docker.

## Features

- Simple Flask web application.
- Automated testing with pytest.
- CI/CD pipeline configured with GitHub Actions.
- Docker support for containerization.

## Directory Structure

```
.
├── .github
│   └── workflows
│       └── ci.yml          # GitHub Actions workflow configuration
├── app.py                  # Main Flask application
├── Dockerfile              # Docker configuration file
├── requirements.txt        # Python dependencies
├── tests
    └── test_app.py         # Unit tests
```

## Getting Started

### Prerequisites

- Python 3.9 or higher
- Docker (for running the application in a container)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Shift_Happens/cw_lista_nr_2.git
   cd cw_lista_nr_2
   ```

2. **Create a virtual environment and install dependencies:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```

3. **Run the Flask application:**
   ```bash
   flask run
   ```

   The application will be accessible at `http://localhost:5000`.

### Running Tests

To run the unit tests for the Flask application, use:

```bash
pytest
```

### Using Docker

1. **Build the Docker image:**
   ```bash
   docker build -t cw_lista_nr_2 .
   ```

2. **Run the Docker container:**
   ```bash
   docker run -p 5000:5000 cw_lista_nr_2
   ```

   The application will be accessible at `http://localhost:5000`.
![image](https://github.com/Shift-Happens/cw_lista_nr_2/assets/90008035/47b633a3-9b02-4705-ba55-8febf2c770bc)


## Continuous Integration and Deployment

This project uses GitHub Actions for CI/CD. The workflow configuration file (`.github/workflows/ci.yml`) defines the pipeline steps which include:

- Checking out the repository.
- Setting up Python.
- Installing dependencies.
- Running tests.

## Useful Resources

- [Flask Documentation](https://flask.palletsprojects.com/)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Docker Documentation](https://docs.docker.com/)
