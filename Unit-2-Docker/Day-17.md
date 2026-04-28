# 📅 Day 17 - Docker Networking Basics (Detailed Notes)

## 📚 Topics Covered

- Bridge network  
- Custom network  
- Container communication  

---

## 🐳 1. Bridge Network

### 📌 Definition  
Default network for containers.

### 💻 Command / Example  
`docker network ls`

### 🔍 Explanation  
- Automatically created  
- Containers communicate via IP  

### 💡 Concept  
- Suitable for single host  

---

## 🔗 2. Custom Network

### 📌 Definition  
User-defined network for better control.

### 💻 Command / Example  
`docker network create mynet`

### 🔍 Explanation  
- Creates isolated network  
- Containers communicate using names  

### 💡 Concept  
- Better DNS support  

---

## 🔄 3. Container Communication

### 📌 Definition  
Containers communicate within same network.

### 💻 Command / Example  
`docker run --network mynet nginx`

### 🔍 Explanation  
- Same network required  
- Uses container names  

### 💡 Concept  
- Enables microservices  

---

## 🧪 4. Practical

### 📌 Definition  
Hands-on networking.

### 💻 Command / Example  
`docker network create appnet`  
`docker run --network appnet nginx`

### 🔍 Explanation  
- Create network  
- Run containers  

### 💡 Concept  
- Real-world communication  

---

## 💡 5. Key Learnings

### 📌 Definition  
Important takeaways.

### 💻 Command / Example  
`docker network ls`

### 🔍 Explanation  
- Networks connect containers  
- Custom networks are better  

### 💡 Concept  
- Core for microservices  

---

## ❓ 6. Doubts

### 📌 Definition  
Common questions.

### 💻 Command / Example  
`docker inspect network`

### 🔍 Explanation  
- Difference between bridge & custom network  

### 💡 Concept  
- Helps understanding networking  

---

## 🔥 7. Summary

### 📌 Definition  
Quick recap.

### 💻 Command / Example  
`docker network create`

### 🔍 Explanation  
- Networks enable communication  

### 💡 Concept  
- Essential for distributed systems  

---
