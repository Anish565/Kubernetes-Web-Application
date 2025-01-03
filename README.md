# Kubernetes Web Application Deployment

This project demonstrates deploying a simple To-Do web application using Kubernetes, Docker, and AWS EKS. The assignment covers containerization, deployment, replication, rolling updates, health monitoring, and alerting in Kubernetes.

---

Reference Document - https://docs.google.com/document/d/1c5FSy6-Lg5Zbf5bdS_R9Me0Ey7ZjLBE7rpGHWhZ-6ZM/edit?usp=sharing

---

## Objective

The goal is to learn how to:

- Containerize applications using Docker.
- Deploy the application locally using Minikube.
- Deploy the application on AWS Elastic Kubernetes Service (EKS).
- Utilize Kubernetes features like replication controllers, rolling updates, health monitoring, and alerting.

---

## Prerequisites

Before starting, ensure you have:

- Basic understanding of Docker and Kubernetes.
- Docker installed.
- Minikube and kubectl installed.
- AWS account and Docker Hub account.

---

## Project Structure

1. **Application**: A simple To-Do app using Flask and MongoDB.
2. **Docker**:
   - `Dockerfile` for the Flask app.
   - Docker image for MongoDB and Flask app.
   - `docker-compose.yml` to test locally.
3. **Minikube Deployment**:
   - Two Kubernetes pods (Flask app and MongoDB).
   - Deployment and service configurations.
4. **AWS EKS Deployment**:
   - Deploy the application on EKS.
   - Configure EKS for replication, health monitoring, and alerting.

---

## Step-by-Step Instructions

### Part 1: Application

- Create a simple To-Do web application with Flask and MongoDB.
- Clone the source code and set up the application locally.

### Part 2: Containerization with Docker

- Write a `Dockerfile` for the Flask app.
- Build the Docker image and push it to Docker Hub.
- Test locally using `docker-compose.yml`.

### Part 3: Deploy on Minikube

1. Start Minikube.
2. Create pods for the Flask app and MongoDB.
3. Define a deployment with replicas and container port configurations.
4. Expose the deployment using a Kubernetes service.
5. Test using the Minikube service URL.

### Part 4: Deploy on AWS EKS

1. Create an EKS cluster.
2. Configure `kubectl` to connect to the cluster.
3. Deploy the application using Kubernetes deployment and service configurations.
4. Test the deployment via the public EKS URL.

### Part 5: Replication Controller

- Create a replication controller configuration file.
- Manage replicas by scaling up or down.
- Verify auto-healing of pods by deleting one intentionally.

### Part 6: Rolling Updates

1. Configure a rolling update strategy in the deployment.
2. Update the application image to a new version.
3. Monitor progress using `kubectl` or Kubernetes Dashboard.
4. Test the updated application.

### Part 7: Health Monitoring

- Configure liveness and readiness probes.
- Test health monitoring by introducing a deliberate error.

### Part 8: Alerting (Extra Credit)

- Set up Prometheus for monitoring.
- Configure alerts for failing probes.
- Integrate Slack for notifications.
- Test by deleting a pod and verifying alert notifications.

---

## Required Files

- `Dockerfile`: Defines the Docker image for the application.
- Kubernetes configuration files:
  - Deployment configuration.
  - Service configuration.
- Documentation with screenshots:
  - Application running on Minikube.
  - Application running on AWS EKS.

---

## Testing

- Verify application functionality locally using Docker Compose.
- Confirm deployment on Minikube and EKS.
- Test health monitoring, rolling updates, and alerting configurations.

---

## Conclusion

This project highlights the integration of Docker, Kubernetes, and AWS EKS for deploying and managing scalable web applications. It demonstrates best practices for containerization, deployment, monitoring, and alerting in a cloud-native environment.
