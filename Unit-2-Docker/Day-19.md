# 📅 Day 19 - Port Mapping & Container Linking

## 📚 Topics Covered

- Port mapping  
- Linking containers  
- Communication basics  

---

## 🌐 1. Port Mapping

### 📌 Definition  
Port mapping connects host port to container port.

### 💻 Command / Example  
`docker run -p 8080:80 nginx`

### 🔍 Explanation  
- 8080 → Host  
- 80 → Container  
- Enables browser access  

### 💡 Concept  
- Required for web applications  
- Makes container accessible  

---

## 🔗 2. Linking Containers

### 📌 Definition  
Linking allows one container to communicate with another.

### 💻 Command / Example  
`docker run --link db:dbapp app`

### 🔍 Explanation  
- db → container name  
- dbapp → alias  
- Enables communication  

### 💡 Concept  
- Old method  
- Replaced by networks  

---

## 🔄 3. Container Communication

### 📌 Definition  
Containers communicate using ports or networks.

### 💻 Command / Example  
`docker run --network mynet nginx`

### 🔍 Explanation  
- Same network required  
- Uses container names  

### 💡 Concept  
- Core for microservices  

---

## 🧪 4. Practical

### 📌 Definition  
Hands-on communication.

### 💻 Command / Example  
`docker run -d -p 8080:80 nginx`  
`docker run -d -p 8081:80 nginx`

### 🔍 Explanation  
- Run multiple containers  
- Access using different ports  

### 💡 Concept  
- Demonstrates port mapping  

---

## 💡 5. Key Learnings

### 📌 Definition  
Important takeaways.

### 💻 Command / Example  
`docker run -p`

### 🔍 Explanation  
- Port mapping enables access  
- Linking is outdated  

### 💡 Concept  
- Use networks instead of linking  

---

## ❓ 6. Doubts

### 📌 Definition  
Common questions.

### 💻 Command / Example  
`docker ps`

### 🔍 Explanation  
- Why linking is deprecated?  
- How containers communicate?  

### 💡 Concept  
- Helps in architecture  

---

## 🔥 7. Summary

### 📌 Definition  
Quick recap.

### 💻 Command / Example  
`docker run -p`

### 🔍 Explanation  
- Ports expose containers  
- Networks connect containers  

### 💡 Concept  
- Communication is essential  

---
