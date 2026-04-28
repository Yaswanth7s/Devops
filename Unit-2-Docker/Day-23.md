# 📅 Day 23 - Private Registries & Authentication

## 📚 Topics Covered

- Private registry  
- Authentication  
- Access tokens  

---

## 🔐 1. Private Registry

### 📌 Definition  
Registry accessible only to authorized users.

### 💻 Command / Example  
`docker run -d -p 5000:5000 registry`

### 🔍 Explanation  
- Runs local registry  
- Stores private images  

### 💡 Concept  
- Secure storage  

---

## 🔑 2. Authentication

### 📌 Definition  
Process of verifying user identity.

### 💻 Command / Example  
`docker login`

### 🔍 Explanation  
- Requires username/password  
- Stores credentials  

### 💡 Concept  
- Ensures security  

---

## 🪪 3. Access Tokens

### 📌 Definition  
Tokens used instead of passwords.

### 💻 Command / Example  
`docker login --username user`

### 🔍 Explanation  
- More secure  
- Used in automation  

### 💡 Concept  
- Preferred in CI/CD  

---

## 🧪 4. Practical

### 📌 Definition  
Hands-on authentication.

### 💻 Command / Example  
`docker login`  
`docker push private/image`

### 🔍 Explanation  
- Login  
- Push image  

### 💡 Concept  
- Used in real deployments  

---

## 💡 5. Key Learnings

### 📌 Definition  
Important takeaways.

### 💻 Command / Example  
`docker login`

### 🔍 Explanation  
- Security is important  
- Tokens are safer  

### 💡 Concept  
- Essential for production  

---

## ❓ 6. Doubts

### 📌 Definition  
Common questions.

### 💻 Command / Example  
`docker logout`

### 🔍 Explanation  
- Why tokens instead of passwords?  

### 💡 Concept  
- Improves security  

---

## 🔥 7. Summary

### 📌 Definition  
Quick recap.

### 💻 Command / Example  
`docker login`

### 🔍 Explanation  
- Private registries secure images  

### 💡 Concept  
- Required in enterprise  

---
