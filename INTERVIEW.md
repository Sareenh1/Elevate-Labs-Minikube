# Task 5: Kubernetes Interview Questions and Answers

Below are the answers to the interview questions provided in the DevOps Internship Task 5 document, based on my experience setting up a Kubernetes cluster with Minikube on an Ubuntu EC2 instance.

## 1. What is Kubernetes?
**Answer**: Kubernetes is an open-source platform for automating the deployment, scaling, and management of containerized applications. It organizes containers into pods and provides tools for load balancing, auto-scaling, and self-healing. In this task, I used Kubernetes with Minikube to deploy an Nginx application on an EC2 instance, managing its pods and services.

## 2. What is the role of kubelet?
**Answer**: Kubelet is an agent running on each Kubernetes node, responsible for managing pods and their containers. It communicates with the Kubernetes API server to ensure containers are running as specified. In my Minikube cluster, kubelet ensured the Nginx pods were healthy and running on the single node.

## 3. Explain pods, deployments, and services.
**Answer**: 
- **Pods**: The smallest unit in Kubernetes, containing one or more containers that share network and storage. In my task, each pod ran an Nginx container serving web content.
- **Deployments**: A resource that manages multiple pods, ensuring the desired number of replicas and handling updates. I created a deployment for Nginx with two replicas, later scaled to four.
- **Services**: A resource that exposes pods to network traffic, providing a stable endpoint. I used a NodePort service to make the Nginx app accessible on port 30007.

## 4. How do you scale in Kubernetes?
**Answer**: Scaling adjusts the number of pod replicas in a deployment. You can use the `kubectl scale` command or update the `replicas` field in the deployment YAML. In my task, I scaled the Nginx deployment to four replicas using:
```bash
kubectl scale deployment/nginx-deployment --replicas=4
