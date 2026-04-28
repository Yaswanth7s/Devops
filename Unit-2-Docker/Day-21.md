# 📅 Day 21 - Copy-on-Write Mechanism

## 📚 Topics Covered

- Copy-on-write  
- Layer modification  
- Storage efficiency  

---

## 🧱 1. Copy-on-Write

### 📌 Definition  
Mechanism where data is copied only when modified.

### 💻 Command / Example  
`docker run ubuntu`

### 🔍 Explanation  
- Base image remains unchanged  
- Changes stored in new layer  

### 💡 Concept  
- Saves storage  
- Improves performance  

---

## 🔄 2. Layer Modification

### 📌 Definition  
Changes create new layers.

### 💻 Command / Example  
`docker commit container`

### 🔍 Explanation  
- Original layer unchanged  
- New layer added  

### 💡 Concept  
- Supports versioning  

---

## 🧪 3. Practical

### 📌 Definition  
Hands-on layering.

### 💻 Command / Example  
`docker run ubuntu`  
`touch file.txt`

### 🔍 Explanation  
- Create file  
- Stored in new layer  

### 💡 Concept  
- Demonstrates copy-on-write  

---

## 💡 4. Key Learnings

### 📌 Definition  
Important takeaways.

### 💻 Command / Example  
`docker history`

### 🔍 Explanation  
- Layers are efficient  
- Changes are isolated  

### 💡 Concept  
- Core of Docker storage  

---

## ❓ 5. Doubts

### 📌 Definition  
Common questions.

### 💻 Command / Example  
`docker inspect`

### 🔍 Explanation  
- How layers work internally?  

### 💡 Concept  
- Helps in optimization  

---

## 🔥 6. Summary

### 📌 Definition  
Quick recap.

### 💻 Command / Example  
`docker history`

### 🔍 Explanation  
- Copy-on-write saves storage  

### 💡 Concept  
- Essential Docker feature  

---
