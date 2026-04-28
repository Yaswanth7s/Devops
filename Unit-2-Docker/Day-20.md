# 📅 Day 20 - Docker Storage (Volumes vs Bind Mounts)

## 📚 Topics Covered

- Volumes  
- Bind mounts  
- Data persistence  

---

## 📦 1. Volumes

### 📌 Definition  
Volumes are managed storage used by Docker.

### 💻 Command / Example  
`docker volume create myvol`

### 🔍 Explanation  
- Stored in Docker directory  
- Managed by Docker  

### 💡 Concept  
- Best for persistent data  

---

## 📂 2. Bind Mounts

### 📌 Definition  
Bind mounts map host directory to container.

### 💻 Command / Example  
`docker run -v /host:/container nginx`

### 🔍 Explanation  
- Direct mapping  
- Uses host file system  

### 💡 Concept  
- Useful for development  

---

## 💾 3. Data Persistence

### 📌 Definition  
Data stored outside container lifecycle.

### 💻 Command / Example  
`docker run -v myvol:/data nginx`

### 🔍 Explanation  
- Data survives container deletion  
- Stored in volume  

### 💡 Concept  
- Important for databases  

---

## 🧪 4. Practical

### 📌 Definition  
Hands-on storage.

### 💻 Command / Example  
`docker volume create data`  
`docker run -v data:/app nginx`

### 🔍 Explanation  
- Create volume  
- Use in container  

### 💡 Concept  
- Ensures persistent storage  

---

## 💡 5. Key Learnings

### 📌 Definition  
Important takeaways.

### 💻 Command / Example  
`docker volume ls`

### 🔍 Explanation  
- Volumes are safer  
- Bind mounts are flexible  

### 💡 Concept  
- Choose based on use case  

---

## ❓ 6. Doubts

### 📌 Definition  
Common questions.

### 💻 Command / Example  
`docker volume inspect`

### 🔍 Explanation  
- Difference between volume & bind mount?  

### 💡 Concept  
- Helps in storage design  

---

## 🔥 7. Summary

### 📌 Definition  
Quick recap.

### 💻 Command / Example  
`docker volume create`

### 🔍 Explanation  
- Volumes store data  
- Bind mounts map host  

### 💡 Concept  
- Persistence is critical  

---
