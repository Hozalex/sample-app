# sample-app

A simple Go HTTP service that serves colored PNG images.

## Overview

This service exposes two endpoints:

- `GET /blue` — returns a 100x100 blue PNG image
- `GET /red` — returns a 100x100 red PNG image

## Tech Stack

- **Language:** Go 1.23
- **Container:** Docker (distroless base)
- **Orchestration:** Kubernetes
- **CI/CD:** GitHub Actions

## Local Development

```bash
go run main.go
```

Service starts on port `8080`.

## Docker

```bash
docker build -t sample-app .
docker run -p 8080:8080 sample-app
```

## Kubernetes Deployment

```bash
kubectl apply -f dev/deployment.yaml
```

## Environment

| Variable | Description        | Default |
|----------|--------------------|---------|
| PORT     | HTTP server port   | 8080    |
