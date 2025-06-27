# 🚀 Simple Web App with Kubernetes

This is a beginner-friendly project to deploy a simple web server inside a Kubernetes cluster using **k3s** and basic manifests. It marks the start of my Kubernetes learning journey.

---

## 📦 Project Structure

```
simple-web-app/
├── deployment.yml       # Kubernetes Deployment manifest
├── service.yml          # Kubernetes Service manifest
├── docker-compose.yml   # (For local Docker setup or comparison)
└── web/                 # Web server code (static HTML or minimal app)
```

---

## 🧠 What This Project Demonstrates

- ✅ Creating a Dockerized web application
- ✅ Writing Kubernetes Deployment and Service manifests
- ✅ Deploying to a local k3s cluster using `kubectl`
- ✅ Exposing the app using NodePort and accessing via browser

---

## 🛠 How to Use

### 1. Clone this repository

```bash
git clone https://github.com/lele-maxwell/simple-web-app.git
cd simple-web-app
```

### 2. Build Docker Image Locally


```bash
docker build -t web-app:latest ./web

```

### 3. Apply Kubernetes Manifests

Make sure you're connected to your `k3s` cluster:

```bash
kubectl apply -f deployment.yml
kubectl apply -f service.yml
```

### 4. Access the App

Find the Node IP and NodePort:

```bash
kubectl get svc
```

Then open in your browser:

```
http://<NODE-IP>:<NODE-PORT>
```

---

## ✍️ Author

**Lele Maxwell**  
This project is my **first step into Kubernetes**, and I’ll continue building from here.

---

## 🧊 License

This project is open-source and free to use.