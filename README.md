# Task 5: Kubernetes Cluster with Minikube

## Overview
This repository contains the deliverables for the DevOps Internship Task 5. I set up a Kubernetes cluster using Minikube on an Ubuntu EC2 instance, deployed an Nginx application, and exposed it via a NodePort service accessible on the EC2 public IP.

## Files
- `deployment.yaml`: Defines the Nginx deployment with 2 replicas.
- `service.yaml`: Exposes the Nginx app on port 30007 (NodePort).
- `pods.txt`: Output of `kubectl get pods`.
- `services.txt`: Output of `kubectl get services`.
- (Screenshots uploaded separately or linked if hosted.)

## Steps
1. Installed Docker, kubectl, and Minikube.
2. Started Minikube with Docker driver.
3. Created and applied `deployment.yaml` for Nginx.
4. Exposed the app with `service.yaml` (NodePort 30007).
5. Scaled the deployment to 4 replicas.
6. Verified pods, services, and accessed the app at `http://<ec2-public-ip>:30007`.

## Access
The Nginx app is accessible at `http://<ec2-public-ip>:30007` (replace with actual IP).

## Notes
- Ensure EC2 security group allows port 30007.
- Screenshots of the browser and terminal outputs are included or linked.

