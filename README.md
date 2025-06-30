# Acknowledgements

Originally forked from LondheShubham153/django-notes-app.

Huge thanks to Shubham Londhe bhiya for building the app and open‑sourcing.

Using this project, which was originally created by Shubham Londhe bhaiya for learning purposes, I built a fully containerized environment with Docker and successfully deployed it to a Kubernetes cluster. It serves as a practical base to explore and implement modern DevOps practices, including Docker image creation, orchestration with Docker Compose, and scalable deployment using Kubernetes.

once again thanks to Shubham Londhe bhiya (trainwithshubham)

# Simple Notes App
This is a simple notes app built with React and Django.

## Requirements
1. Python 3.9
2. Node.js
3. React

## Installation
1. Clone the repository
```
git clone https://github.com/LondheShubham153/django-notes-app.git
```

```
cd django-notes-app
git checkout dev
```

# Using Docker Deployment

2. Build the app
```
docker build -t notes-app .
```

3. Run the app
```
docker run -d -p 8000:8000 notes-app:latest
```

4. Using docker-compose.yml
```
docker-compose up -d
```

# Using Kubernetes Deployment

1. Build the image
```
docker build -t <your-dockerhub-username>/notes-app:latest .
```

2. Push the image on docker hub
```
docker push <your-dockerhub-username>/notes-app:latest
```

3. Create Kubernetes deployment and service YAMLs for notes-app

4. Apply the manifests
```
kubectl apply -f kubernetes/
```

Make sure to configure Secrets or ConfigMaps for sensitive environment variables


## Nginx

Install Nginx reverse proxy to make this application available

`sudo apt-get update`
`sudo apt install nginx`