# 📅 Day 15 - Advanced Dockerfile Instructions (Detailed Notes)

## 📚 Topics Covered

- WORKDIR  
- ADD vs COPY  
- ENV instruction  
- EXPOSE  
- CMD vs ENTRYPOINT  

---

## 🐳 1. WORKDIR

### 📌 Definition  
WORKDIR sets the working directory inside the container.

### 💻 Command / Example  
`WORKDIR /app`

### 🔍 Explanation  
- Sets default directory for instructions  
- All commands run inside this directory  
- Creates directory if not exists  

### 💡 Concept  
- Avoids writing full paths  
- Improves readability  

---

## 📂 2. ADD vs COPY

### 📌 Definition  
ADD and COPY are used to transfer files into container.

### 💻 Command / Example  
`COPY file.txt /app/`  
`ADD file.tar.gz /app/`

### 🔍 Explanation  
- COPY → simple file copy  
- ADD → supports URL and extraction  
- ADD automatically extracts tar files  

### 💡 Concept  
- Use COPY for simplicity  
- Use ADD only when required  

---

## 🌍 3. ENV Instruction

### 📌 Definition  
ENV sets environment variables inside Dockerfile.

### 💻 Command / Example  
`ENV APP_ENV=production`

### 🔍 Explanation  
- Sets variable during build  
- Available inside container  
- Used by applications  

### 💡 Concept  
- Used for configuration  
- Avoids hardcoding  

---

## 🌐 4. EXPOSE

### 📌 Definition  
EXPOSE informs Docker about container port.

### 💻 Command / Example  
`EXPOSE 80`

### 🔍 Explanation  
- Declares port used by container  
- Does NOT publish port  
- Used for documentation  

### 💡 Concept  
- Works with `-p` flag  
- Helps in container networking  

---

## ⚙️ 5. CMD vs ENTRYPOINT

### 📌 Definition  
CMD and ENTRYPOINT define container startup behavior.

### 💻 Command / Example  
`CMD ["node", "app.js"]`  
`ENTRYPOINT ["node"]`

### 🔍 Explanation  
- CMD → default command  
- ENTRYPOINT → fixed command  
- CMD can be overridden  

### 💡 Concept  
- ENTRYPOINT ensures fixed execution  
- CMD provides flexibility  

---

## 🧪 6. Practical

### 📌 Definition  
Hands-on using advanced Dockerfile instructions.

### 💻 Command / Example  
`docker build -t advanced:v1 .`  
`docker run -p 8080:80 advanced:v1`

### 🔍 Explanation  
- Build image with advanced instructions  
- Run container and verify output  

### 💡 Concept  
- Helps understand real usage  
- Used in production environments  

---

## 💡 7. Key Learnings

### 📌 Definition  
Important takeaways.

### 💻 Command / Example  
`docker build`  

### 🔍 Explanation  
- WORKDIR simplifies paths  
- ENV used for configuration  
- ENTRYPOINT controls execution  

### 💡 Concept  
- Advanced instructions improve control  
- Helps in real-world apps  

---

## ❓ 8. Doubts

### 📌 Definition  
Common questions.

### 💻 Command / Example  
`docker inspect container`

### 🔍 Explanation  
- Difference between CMD & ENTRYPOINT  
- When to use ADD vs COPY  

### 💡 Concept  
- Understanding improves debugging  

---

## 🔥 9. Summary

### 📌 Definition  
Quick recap.

### 💻 Command / Example  
`docker build -t app:v1 .`

### 🔍 Explanation  
- Advanced instructions enhance Dockerfile  
- Improve flexibility and control  

### 💡 Concept  
- Important for production setups  

---
