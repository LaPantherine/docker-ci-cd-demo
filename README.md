# Docker CI/CD Demo

![CI](https://github.com/LaPantherine/docker-ci-cd-demo/actions/workflows/docker-build.yml/badge.svg)

This repository demonstrates a simple CI/CD pipeline using Docker and GitHub Actions.
The project builds and runs a Python application inside a Docker container and validates the setup through an automated workflow.

## Tech Stack

- Docker
- Python 3.11 (slim)
- GitHub Actions

## Architecture

User → Docker container (Python application) → HTTP response

## How to Run Locally

Build the Docker image:

```bash
docker build -t devops-demo .
```

Run the container:

```bash
docker run -p 5001:5000 devops-demo
```

If port 5000 is already in use, map another port (e.g., 5001).

## CI/CD Pipeline

The pipeline is configured using GitHub Actions and runs automatically on every push to the main branch.

Pipeline steps:
- Build Docker image
- Validate project structure

## Project Structure

```
docker-ci-cd-demo
├── app/
│   └── app.py
├── Dockerfile
├── README.md
└── .github/
    └── workflows/
        └── docker-build.yml
```

## Future Improvements

- Push Docker image to Docker Hub
- Add automated tests
- Deploy application to a cloud platform (AWS, Render, Railway)
