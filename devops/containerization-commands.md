# Containerization Commands

Build the container image:
```bash
podman build -t fastapi-hello-world .
```

To view container images built locally:
```bash
podman images
```

To delete local container images:
```bash
podman rmi -f <hash>
```

Run the container image:
```bash
podman run -p 8000:8000 localhost/fastapi-hello-world:latest
```

Traditionally, to load the container image into the minkube cluster:
```bash
minikube image load localhost/fastapi-hello-world:latest
```

However, this wasn't working so we used a tarball:
```bash
podman save -o fastapi.tar localhost/fastapi-hello-world:latest
minikube image load fastapi.tar
```
Now, the container image is built and pushed into the cluster. deploy.yaml can now use this container image.

To view active pods:
```bash
kubectl get pods
```

To view container images inside of minikube:
```bash
minikube image ls
```

To start minikube and using podman:
```bash
minikube start --driver=podman
```

To fresh restart minikibe:
```bash
minikube stop
minikube delete --all --purge
```

To restart pods:
```bash
kubectl rollout restart deploy/fastapi-hello-world
```

To view active servies:
```bash
minikube service list
```

To access a service via URL:
```bash
minikube service fastapi-hello-world-service --url
```

To enable ingress:
```bash
minikube addons enable ingress
```
`
