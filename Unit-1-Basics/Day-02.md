# 📅 Day 02 - Docker Installation & Nginx Setup

## 📚 Topics Covered

* Introduction to Docker
* Installation of Docker
* Running first container
* Introduction to Nginx using Docker

---

## 🐳 What is Docker?

Docker is a platform used to **develop, ship, and run applications inside containers**.

It ensures that applications run the same in all environments.

---

## 🎯 Why Docker is Used

* Fast and lightweight
* Easy deployment
* Consistent environment
* Isolation of applications

---

## ⚙️ Docker Installation

Docker was installed on all systems during the lab session.

### 🛠️ Steps Followed

* Downloaded Docker Desktop
* Installed and completed setup
* Restarted system (if required)

---

## ✅ Verification of Docker

```bash
docker --version
```

👉 Checks installed version

```bash
docker run hello-world
```

👉 Runs a test container to verify Docker is working

---

## 🌐 Running Nginx using Docker

Nginx is a **web server** used to serve web pages.

We ran Nginx inside a Docker container.

---

### 🛠️ Command Used

```bash
docker run -d -p 8080:80 nginx
```

---

### 🔍 Explanation of Command

* `docker run` → Run a container
* `-d` → Run in background (detached mode)
* `-p 8080:80` → Map port 8080 (host) to 80 (container)
* `nginx` → Official Nginx image

---

### 🌍 Output

* Open browser
* Go to:

```
http://localhost:8080
```

👉 Nginx welcome page is displayed ✅

---

## 🛠️ Practical

* Installed Docker
* Verified Docker installation
* Ran hello-world container
* Deployed Nginx container

---

## 💡 Learnings

* Docker can run applications easily using containers
* Nginx can be deployed quickly using Docker
* Port mapping allows access through browser

---

## ❓ Doubts

* How port mapping works internally

---

## 🧾 Summary

* Docker installation completed successfully
* First container executed
* Nginx web server deployed using Docker
