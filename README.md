# K8 Fullstack Helloworld

## Technologies

- Client: Vite
- API: Express

## Deployment Cycle

From the root directory. Also, replace joshbrusa/k8-fullstack-helloworld in the commands, k8s/deployments.yaml and k8s/services.yaml with your own.

### Build Images

```bash

docker build -t joshbrusa/k8-fullstack-helloworld-client ./client

```

```bash

docker build -t joshbrusa/k8-fullstack-helloworld-api ./api

```

### Push Images to Docker Hub

```bash

docker push joshbrusa/k8-fullstack-helloworld-client

```

```bash

docker push joshbrusa/k8-fullstack-helloworld-api

```

### Start Minikube

```bash

minikube start

```

### Apply Deployments and Services

```bash

kubectl apply -f k8s/deployments.yaml

```

```bash

kubectl apply -f k8s/services.yaml

```

### Make Cluster Discoverable

```bash

minikube tunnel

```

### When Done

```code

minikube delete --all

```

Prevents stale images.
