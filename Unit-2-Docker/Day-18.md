# 📅 Day 18 - Docker Networking (Host, Bridge, Overlay, DNS)

## 📚 Topics Covered

- Host network  
- Bridge network (recap)  
- Overlay network  
- DNS inside Docker  

---

## 🐳 1. Host Network

### 📌 Definition  
Host network allows container to share host’s network directly.

### 💻 Command / Example  
`docker run --network host nginx`

### 🔍 Explanation  
- No network isolation  
- Uses host IP directly  
- Faster communication  

### 💡 Concept  
- No port mapping needed  
- Used for high-performance apps  

---

## 🌉 2. Bridge Network (Recap)

### 📌 Definition  
Default network used by Docker containers.

### 💻 Command / Example  
`docker network ls`

### 🔍 Explanation  
- Containers get private IP  
- Can communicate via IP  

### 💡 Concept  
- Default for standalone containers  
- Limited DNS support  

---

## 🌐 3. Overlay Network

### 📌 Definition  
Overlay network connects containers across multiple hosts.

### 💻 Command / Example  
`docker network create -d overlay myoverlay`

### 🔍 Explanation  
- Used in Docker Swarm  
- Enables cross-host communication  

### 💡 Concept  
- Required for distributed systems  
- Supports microservices  

---

## 🔍 4. DNS Inside Docker

### 📌 Definition  
Docker provides internal DNS for container communication.

### 💻 Command / Example  
`docker run --name web nginx`

### 🔍 Explanation  
- Containers can access others using names  
- Works in custom networks  

### 💡 Concept  
- No need for IP addresses  
- Improves service discovery  

---

## 🧪 5. Practical

### 📌 Definition  
Hands-on with networking.

### 💻 Command / Example  
`docker network create mynet`  
`docker run --network mynet --name c1 nginx`  
`docker run --network mynet --name c2 nginx`

### 🔍 Explanation  
- Create network  
- Run containers  
- Test communication  

### 💡 Concept  
- Demonstrates DNS + networking  

---

## 💡 6. Key Learnings

### 📌 Definition  
Important takeaways.

### 💻 Command / Example  
`docker network create`

### 🔍 Explanation  
- Host network removes isolation  
- Overlay used for multi-host  

### 💡 Concept  
- Networking is core for communication  

---

## ❓ 7. Doubts

### 📌 Definition  
Common questions.

### 💻 Command / Example  
`docker network inspect`

### 🔍 Explanation  
- When to use overlay network?  
- Difference between host & bridge?  

### 💡 Concept  
- Helps in system design  

---

## 🔥 8. Summary

### 📌 Definition  
Quick recap.

### 💻 Command / Example  
`docker network ls`

### 🔍 Explanation  
- Different network types available  
- Used based on requirement  

### 💡 Concept  
- Networking enables connectivity  

---
