# Kubernetes Web Application Deployment

A simple Node.js web application containerized using Docker and deployed on a Kubernetes cluster using Kubernetes Deployment and Service manifests.

## 📌 Project Overview

This project demonstrates how to:

* Build a simple Node.js web application
* Create a Docker image for the application
* Run the application using Docker
* Deploy the application to Kubernetes
* Create multiple replicas using a Kubernetes Deployment
* Expose the application using a Kubernetes Service
* Access the application using Minikube
* Manage the application using `kubectl`

## 🛠️ Technologies Used

* **Node.js** – Application runtime
* **Docker** – Containerization
* **Kubernetes** – Container orchestration
* **Minikube** – Local Kubernetes cluster
* **kubectl** – Kubernetes command-line tool
* **YAML** – Kubernetes configuration
* **Git & GitHub** – Version control

## 📁 Project Structure

```text
k8s-demo/
│
├── app.js
├── package.json
├── package-lock.json
├── Dockerfile
├── deployment.yaml
├── service.yaml
├── .gitignore
└── README.md
```

## 🚀 Application

The application is a basic Node.js web server that returns a response when accessed through the browser.

The application is containerized using Docker and deployed to Kubernetes.

## 🐳 Step 1: Build the Docker Image

Build the Docker image from the project directory:

```bash
docker build -t k8s-demo-app:latest .
```

Check the image:

```bash
docker images
```

## ▶️ Step 2: Run the Application Using Docker

Run the container:

```bash
docker run -p 3000:3000 k8s-demo-app:latest
```

The application can then be accessed through:

```text
http://localhost:3000
```

## ☸️ Step 3: Start Minikube

Start the local Kubernetes cluster:

```bash
minikube start
```

Check the cluster:

```bash
kubectl get nodes
```

## 📦 Step 4: Load Docker Image into Minikube

Load the locally built Docker image into Minikube:

```bash
minikube image load k8s-demo-app:latest
```

Verify the image:

```bash
minikube image ls
```

## 🚢 Step 5: Deploy the Application

Apply the Kubernetes Deployment:

```bash
kubectl apply -f deployment.yaml
```

Apply the Kubernetes Service:

```bash
kubectl apply -f service.yaml
```

Check the Deployment:

```bash
kubectl get deployments
```

Check the Pods:

```bash
kubectl get pods
```

Check the Service:

```bash
kubectl get services
```

## 📈 Step 6: Scale the Application

The application can be scaled to multiple replicas.

For example, to run 4 replicas:

```bash
kubectl scale deployment k8s-demo-deployment --replicas=4
```

Verify:

```bash
kubectl get pods
```

You should see multiple application Pods running.

## 🌐 Step 7: Access the Application

Use Minikube to access the Kubernetes Service:

```bash
minikube service k8s-demo-service
```

This opens the application through the Kubernetes Service.

You can also check the Service details:

```bash
kubectl get svc
```

## 🔍 Useful Kubernetes Commands

### Check Pods

```bash
kubectl get pods
```

### Check Deployments

```bash
kubectl get deployments
```

### Check Services

```bash
kubectl get services
```

### Get detailed Pod information

```bash
kubectl describe pod <pod-name>
```

### View Pod logs

```bash
kubectl logs <pod-name>
```

### Check all resources

```bash
kubectl get all
```

### Delete the Deployment

```bash
kubectl delete -f deployment.yaml
```

### Delete the Service

```bash
kubectl delete -f service.yaml
```

## 🧹 Cleanup

To remove the Kubernetes resources:

```bash
kubectl delete -f deployment.yaml
kubectl delete -f service.yaml
```

To completely remove the Minikube cluster:

```bash
minikube delete
```

## 🎯 What I Learned

Through this project, I practiced:

* Docker image creation
* Docker container management
* Kubernetes Deployments
* Kubernetes Pods
* Kubernetes Services
* Kubernetes YAML manifests
* Application scaling
* Minikube cluster management
* `kubectl` commands
* Containerized application deployment

## 💼 Resume Project Description

**Kubernetes Web Application Deployment**

* Containerized a Node.js web application using Docker and deployed it on a Kubernetes cluster using Minikube.
* Created Kubernetes Deployment and Service YAML manifests to manage application Pods and expose the application.
* Implemented application scaling using Kubernetes replicas and managed resources using `kubectl`.

## 👩‍💻 Author

**Priyanka Chauhan**

DevOps & Cloud Computing Enthusiast
