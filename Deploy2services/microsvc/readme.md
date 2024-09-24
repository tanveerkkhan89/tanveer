# Microservices Setup with Helm on Minikube

## Overview
This setup includes two microservices (`blog-service` and `all-course-service`) using a single Helm chart with one deployment and one service, along with ingress to route traffic.

## Steps

1. **Remove unnecessary files**:
   - Clean up large files like `as` and `hpatest` which were not needed for this project also i have removed test folder and hpa file

2. **Start Minikube**:
   - make user minikube is running! ( cluster )
   minikube start

3. **Build and Push the images in your repo**:
- docker build -t <your-dockerhub-username>/blog-service:latest .
- docker push <your-dockerhub-username>/blog-service:latest

- docker build -t <your-dockerhub-username>/all-course-service:latest .
-  docker push <your-dockerhub-username>/all-course-service:latest

4. **Use Minikube's Built-in Nginx**:
- If you're using Minikube, you can also use its built-in Nginx setup without Helm:
   - **minikube addons enable ingress**

5. **Helm Chart**:

Single Helm chart for both services, using two different images.
Ingress is configured for routing.

Deploy with Helm: ( First Time )
helm install microservices ./microsvc -n course

if any changes done:
helm upgrade microservices ./microsvc -n course