# 📅 Day 14 - Dockerfile Basics & Image Creation (Detailed Notes)

## 📚 Topics Covered

- Dockerfile Introduction  
- Writing Dockerfile  
- Basic Instructions (FROM, RUN, COPY, CMD)  
- Image Creation using docker build  
- Image Layering Concept  
- Build Context & .dockerignore  
- Environment Variables  
- Port Mapping  

---

## 🐳 1. Dockerfile Introduction

### 📌 Definition  
A Dockerfile is a text file that contains instructions to automatically build a Docker image.

### 💻 Command / Example  
`docker build -t myapp:v1 .`

### 🔍 Explanation  
- Docker reads instructions from Dockerfile  
- Builds image step-by-step  
- `-t` is used for tagging  

### 💡 Concept  
- Acts as blueprint for image creation  
- Ensures consistent environments  

---

## ⚙️ 2. Writing Dockerfile

### 📌 Definition  
Writing a Dockerfile means defining step-by-step instructions to create an image.

### 💻 Command / Example  
`touch Dockerfile`

### 🔍 Explanation  
- Create a file named Dockerfile  
- Add instructions inside it  
- Save in project directory  

### 💡 Concept  
- Instructions execute sequentially  
- Each instruction creates a layer  

---

## 🧱 3. Basic Instructions (FROM, RUN, COPY, CMD)

### 📌 Definition  
Core instructions used to build and configure images.

### 💻 Command / Example  
`FROM ubuntu`  
`RUN apt update`  
`COPY file.txt /app/`  
`CMD ["echo", "Hello"]`

### 🔍 Explanation  
- FROM → Base image  
- RUN → Executes commands  
- COPY → Copies files  
- CMD → Default command  

### 💡 Concept  
- Defines image behavior  
- Each instruction creates a layer  

---

## 🏗️ 4. Image Creation using docker build

### 📌 Definition  
Docker image is created using build command.

### 💻 Command / Example  
`docker build -t myimage:v1 .`

### 🔍 Explanation  
- Reads Dockerfile  
- Builds image step-by-step  
- Tags image  

### 💡 Concept  
- Automates image creation  
- Supports versioning  

---

## 🧱 5. Image Layering Concept

### 📌 Definition  
Each Dockerfile instruction creates a separate layer.

### 💻 Command / Example  
`FROM ubuntu`  
`RUN apt update`  
`RUN apt install -y nginx`

### 🔍 Explanation  
- Each command creates a layer  
- Layers are reused  
- Only modified layers rebuild  

### 💡 Concept  
- Improves performance  
- Saves storage  

---

## 📦 6. Build Context & .dockerignore

### 📌 Definition  
Build context is the files sent to Docker; .dockerignore excludes unnecessary files.

### 💻 Command / Example  
`docker build -t app:v1 .`

### 🔍 Explanation  
- `.` means current directory  
- All files are sent  
- .dockerignore removes unwanted files  

### 💡 Concept  
- Reduces image size  
- Improves build speed  

---

## 🌍 7. Environment Variables

### 📌 Definition  
Variables used to configure container behavior.

### 💻 Command / Example  
`docker run -e APP_ENV=production nginx`

### 🔍 Explanation  
- `-e` sets environment variable  
- Available inside container  
- Used for configuration  

### 💡 Concept  
- Avoids hardcoding values  
- Makes applications flexible  

---

## 🌐 8. Port Mapping

### 📌 Definition  
Connects container port with host port.

### 💻 Command / Example  
`docker run -p 8080:80 nginx`

### 🔍 Explanation  
- 8080 → Host port  
- 80 → Container port  
- Enables browser access  

### 💡 Concept  
- Required for web apps  
- Allows external communication  

---

## 🧪 9. Practical

### 📌 Definition  
Hands-on implementation of Dockerfile and image creation.

### 💻 Command / Example  
`touch Dockerfile`  
`docker build -t myweb:v1 .`  
`docker run -d -p 8080:80 myweb:v1`

### 🔍 Explanation  
- Create Dockerfile  
- Build image  
- Run container  

### 💡 Concept  
- Practical helps understand real workflow  
- Used in real DevOps projects  

---

## 💡 10. Key Learnings

### 📌 Definition  
Important concepts learned from this topic.

### 💻 Command / Example  
`docker build`  
`docker run`

### 🔍 Explanation  
- Dockerfile automates image creation  
- Layering improves efficiency  
- Build context affects performance  

### 💡 Concept  
- Docker simplifies deployment  
- Images are reusable  

---

## ❓ 11. Doubts

### 📌 Definition  
Common questions that may arise.

### 💻 Command / Example  
`docker history image_name`

### 🔍 Explanation  
- Difference between RUN and CMD  
- Why layering is important  
- What happens when Dockerfile changes  

### 💡 Concept  
- Understanding internals improves debugging  
- Helps in interviews  

---

## 🔥 12. Summary

### 📌 Definition  
Quick recap of all concepts.

### 💻 Command / Example  
`docker build -t app:v1 .`  
`docker run -p 8080:80 app:v1`

### 🔍 Explanation  
- Dockerfile builds images  
- Containers run applications  
- Ports expose services  

### 💡 Concept  
- Dockerfile → Image → Container  
- Core workflow of Docker  

---
