# Node.js CI/CD Pipeline using GitHub Actions and Docker

## Project Overview
This project automates the build and delivery of a Node.js application using GitHub Actions and Docker.

## Technologies Used
- Node.js
- Git and GitHub
- GitHub Actions
- Docker
- Docker Hub
- Ubuntu (WSL)

## CI/CD Workflow
1. Push code to the GitHub main branch.
2. GitHub Actions automatically triggers the workflow.
3. Check out the source code.
4. Set up Node.js and validate the application.
5. Build the Docker image.
6. Log in to Docker Hub using GitHub repository secrets.
7. Push the Docker image to Docker Hub.

## Docker Hub Image
`project0123/nodejs-app:latest`

## Run the Application Locally

Pull the Docker image:

```bash
docker pull project0123/nodejs-app:latest
```

Run the container:

```bash
docker run -d --name nodejs-app -p 3000:3000 project0123/nodejs-app:latest
```

Open the application in your browser:

http://localhost:3000

## Verify the Container

```bash
docker ps
docker logs nodejs-app
```

## Result
Successfully built and pushed the Docker image to Docker Hub using GitHub Actions. The application was tested locally in a Docker container.
