# Docker CI/CD Demo

This project demonstrates a basic DevOps CI/CD pipeline using Docker and GitHub Actions.

## Tech Stack

- Docker
- Python
- GitHub Actions

## Project Structure

docker-ci-cd-demo
├── app
│   └── app.py
├── Dockerfile
├── README.md
└── .github/workflows/docker-build.yml

## How to run locally

docker build -t devops-demo .
docker run -p 5000:5000 devops-demo
