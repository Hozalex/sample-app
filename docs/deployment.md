# Deployment

## Kubernetes

The app is deployed to Kubernetes using manifests in the `dev/` directory.

```bash
kubectl apply -f dev/deployment.yaml
```

### Deployment manifest

- **Image:** `ghcr.io/hozalex/sample-app:master`
- **Replicas:** 1
- **Port:** 8080
- **Namespace:** default

## CI/CD

GitHub Actions automatically builds and pushes the Docker image to `ghcr.io` on every push to `master`.

See `.github/workflows/docker-publish.yml` for details.

## Environment Variables

| Variable | Description      | Default |
|----------|------------------|---------|
| PORT     | HTTP server port | 8080    |
