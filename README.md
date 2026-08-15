# CI/CD Python Flask Project

A simple Python Flask application built to practice DevOps and CI/CD concepts using GitHub Actions, Docker, and Docker Hub.

## 🛠️ Technologies Used

- Python
- Flask
- Pytest
- GitHub Actions
- Docker
- Docker Hub
- Git

## 🔄 CI/CD Pipeline

Every time code is pushed to the `main` branch, GitHub Actions automatically:

1. Checks out the code
2. Sets up Python
3. Installs dependencies
4. Runs automated tests
5. Builds a Docker image
6. Logs in to Docker Hub
7. Pushes the Docker image to Docker Hub


## 🐳 Docker

### Build the image

```bash
docker build -t cicd-python-app .

### Pipeline

```text
Developer
    ↓
Git Push
    ↓
GitHub
    ↓
GitHub Actions
    ↓
Run Tests
    ↓
Tests Pass?
   ↙      ↘
 No        Yes
 ↓          ↓
Stop    Build Docker Image
             ↓
        Docker 