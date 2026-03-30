# blue-green-deployment
Implemented Blue-Green Deployment in Kubernetes to achieve zero-downtime releases with instant rollback using service-based traffic switching.

Project: Blue-Green Deployment in Kubernetes


This project demonstrates a Blue-Green Deployment strategy using Kubernetes to achieve zero downtime application releases and instant rollback.

Two versions of the application (Blue and Green) are deployed simultaneously, and traffic is switched between them using a Kubernetes Service.


🧱 Architecture
Blue Deployment → Current live version
Green Deployment → New version
Kubernetes Service → Routes traffic between versions

👉 Traffic switching is done by updating service selectors.


🛠️ Tech Stack
Docker
Kubernetes 
NGINX
kubectl


⚙️ Implementation Steps
Created two applications:
Blue version
Green version
Dockerized both applications
Created Kubernetes Deployments:
blue-deployment
green-deployment
Created a Kubernetes Service pointing to Blue
Switched traffic to Green by updating Service selector


📁 Project Structure
blue-green-deployment/
│
├── blue-app/
│   ├── Dockerfile
│   └── index.html
│
├── green-app/
│   ├── Dockerfile
│   └── index.html
│
├── k8s/
│   ├── blue-deployment.yaml
│   ├── green-deployment.yaml
│   └── service.yaml
│
└── README.md
