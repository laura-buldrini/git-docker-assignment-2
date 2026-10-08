# Git and Docker Starter Application

This repository contains a small Python web application used to practice Git, GitHub, and Docker workflows.

## Application

The application listens on port 8000 and returns a text response when accessed over HTTP.

## Verification

The running application should be verified using an HTTP request to port 8000.

## Running the Application with Docker

Build the Docker image:

```bash
docker build -t git-docker-app:test .
```

Run the application:

```bash
docker run -d --name app-test -p 8080:8000 git-docker-app:test
```

Verify the application:

```bash
curl http://localhost:8080/
```

Expected response:

```text
Advanced Git Docker App
Status: healthy - lauraaraujobuldrini
```

Stop and remove the container:

```bash
docker stop app-test
docker rm app-test
```
