# 📅 Day 11 - Running MySQL Container with Docker (Detailed Notes)

---

## 📚 Topics Covered

- Running MySQL container using Docker
- Environment variables in Docker
- Port mapping
- Container naming
- Managing containers (start, stop, remove)

---

## 🐳 1. Running MySQL Container

### 📌 Definition

The `docker run` command is used to create and start a MySQL container with required configurations.

---

### ✅ Correct Command (Single Line)

```bash
docker run -d \
  -e MYSQL_ROOT_PASSWORD=root123 \
  -e MYSQL_DATABASE=college \
  -e MYSQL_USER=admin \
  -e MYSQL_PASSWORD=admin123 \
  --name mysql-container \
  -p 3306:3306 \
  mysql:8
```

---

### 🔍 Explanation

- `docker run` → Create and start container  
- `-d` → Run in background (detached mode)  
- `-e` → Set environment variables  
- `--name mysql-container` → Assign container name  
- `-p 3306:3306` → Map host port to container port  
- `mysql:8` → MySQL version 8 image  

---

## ⚙️ 2. Environment Variables (Very Important)

Environment variables are required to configure MySQL container.

---

### 📊 Variables Used

| Variable                | Purpose                          |
|------------------------|----------------------------------|
| MYSQL_ROOT_PASSWORD     | Sets root password (mandatory)   |
| MYSQL_DATABASE          | Creates a database automatically |
| MYSQL_USER              | Creates a user                  |
| MYSQL_PASSWORD          | Password for the user           |

---

### ⚠️ Important Rule

👉 If `MYSQL_ROOT_PASSWORD` is missing → container will **NOT start**

---

## 🌐 3. Port Mapping

```bash
-p 3306:3306
```

### 🎯 Meaning

- Left side → Host system port  
- Right side → Container port  

### 🎯 Purpose

Allows external applications (like PHP, MySQL Workbench) to connect

---

## 🏷️ 4. Container Naming

```bash
--name mysql-container
```

👉 Assigns a custom name for easy management

---

### ⚠️ Important

- Container names must be unique  
- Even stopped containers reserve the name  

---

## 🔄 5. Managing Containers

### ▶️ Start Container
```bash
docker start mysql-container
```

### ⛔ Stop Container
```bash
docker stop mysql-container
```

👉 Gracefully stops the container  

---

### ❌ Remove Container
```bash
docker rm mysql-container
```

👉 Removes stopped container  

---

### ⚡ Force Remove
```bash
docker rm -f mysql-container
```

👉 Stops and removes container immediately  

---

## 📋 6. View Containers

### Running Containers
```bash
docker ps
```

### All Containers
```bash
docker ps -a
```

---

## 🔍 7. Image Pulling (Automatic)

When running:

```bash
docker run mysql:8
```

👉 If image is not available locally:

- Docker pulls image from Docker Hub  
- Downloads all layers  
- Stores locally  

---

## ⚠️ 8. Common Issues (Conceptual Understanding)

### 🔹 Name Conflict

Occurs when same container name already exists  

👉 Solution:
```bash
docker rm mysql-container
```
OR use a different name  

---

### 🔹 Port Already in Use

If port `3306` is occupied  

👉 Solution:
```bash
-p 3307:3306
```

---

### 🔹 Missing Environment Variable

MySQL container fails to start  

👉 Always include:
```bash
MYSQL_ROOT_PASSWORD
```

---

## 🛠️ Practical

- Ran MySQL container using Docker  
- Configured database and user  
- Exposed port for external access  
- Managed containers (start, stop, remove)  

---

## 💡 Key Learnings

- Environment variables are essential for MySQL  
- Docker automatically pulls images if not present  
- Container names must be unique  
- Port mapping allows external connection  

---

## ❓ Doubts

- How to connect MySQL container with applications  

---

## 🧾 Summary

- `docker run` → Create and run container  
- `-e` → Set environment variables  
- `-p` → Map ports  
- `docker stop` → Stop container  
- `docker rm` → Remove container  

---
