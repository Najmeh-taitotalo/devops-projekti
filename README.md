# DevOps Projekti

A simple Docker-based web application demonstrating DevOps best practices with automated CI/CD deployment.

## 📋 Project Overview

This project contains a lightweight nginx web server running a Finnish-language landing page. The application is containerized using Docker, making it easy to deploy across different environments consistently.

## 📁 Project Structure

```
devops-projekti/
├── Dockerfile          # Docker image configuration for nginx
├── index.html          # Static web page content
└── README.md           # Project documentation
```

## 🚀 Quick Start

### Prerequisites

- Docker installed on your system ([Get Docker](https://www.docker.com/get-started/))

### Building the Docker Image

```bash
docker build -t devops-projekti .
```

### Running the Container

```bash
docker run -p 80:80 devops-projekti
```

Then open your browser and navigate to `http://localhost`

## 📦 Docker Configuration

The project uses:
- **Base Image**: `nginx:alpine` (lightweight, ~10MB)
- **Port**: 80 (HTTP)
- **Static Content**: Served from `/usr/share/nginx/html/`

## 🔧 Customization

To modify the web page content, edit `index.html` and rebuild the Docker image:

```bash
docker build -t devops-projekti .
docker run -p 80:80 devops-projekti
```

## 🔄 CI/CD Pipeline

This project includes automated CI/CD using GitHub Actions. The pipeline:

- **Triggers**: Runs on every push to the repository
- **Validation**: Checks the HTML content
- **Build**: Builds the Docker image to ensure it works correctly

The workflow file is located at `.github/workflows/ci.yml`.

## 📝 Changelog

- Added GitHub Actions CI/CD pipeline for automated validation and Docker builds



