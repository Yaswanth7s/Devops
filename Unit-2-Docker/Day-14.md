# 📅 Day 14 - Dockerfile Basics & Image Creation (Detailed Notes)

## 📚 Topics Covered

- Dockerfile introduction  
- Writing Dockerfile  
- Basic instructions (FROM, RUN, COPY, CMD)  
- Image creation using docker build  
- Image layering concept  
- Build context & .dockerignore  

---

## 🐳 1. Dockerfile Basics

📌 Definition  

A Dockerfile is a text file that contains a set of instructions used to automatically build a Docker image.

▶️ Command  

```bash
docker build -t myapp:v1 .

🔍 Explanation

The docker build command reads instructions from the Dockerfile and creates an image.

-t myapp:v1 → Tags the image with name and version
. → Refers to current directory (build context)

🧠 Concept

✔ Dockerfile acts as a blueprint for image creation
✔ Eliminates manual installation
✔ Ensures consistent environments

⚙️ 2. Writing a Basic Dockerfile

📌 Example

FROM ubuntu
RUN apt update
RUN apt install -y nginx
CMD ["nginx", "-g", "daemon off;"]

🔍 Explanation

FROM → Base image
RUN → Executes commands
CMD → Default command when container starts

🧠 Concept

✔ Instructions are executed step-by-step
✔ Each instruction creates a layer

🧱 3. Image Layering

📌 Definition

Each instruction in Dockerfile creates a separate layer.

🧠 Concept

✔ Layers are cached
✔ Improves build speed
✔ Only modified layers rebuild

🌍 4. Environment Variables

📌 Definition

Environment variables can be defined inside Dockerfile using ENV.

▶️ Example

ENV APP_ENV=production

🧠 Concept

✔ Used for configuration
✔ Accessible inside container

🌐 5. Port Mapping

📌 Definition

Port mapping exposes container ports to host.

▶️ Command

docker run -p 8080:80 nginx

🧠 Concept

✔ Host port → Container port
✔ Enables browser access

🏷️ 6. Container Naming

📌 Definition

Containers can be given custom names.

▶️ Command

docker run --name mycontainer nginx

🧠 Concept

✔ Helps in easy identification
✔ Used for linking and networking

🔧 7. Managing Containers

▶️ Commands

docker start mycontainer
docker stop mycontainer
docker rm mycontainer

🧠 Concept

✔ start → Runs stopped container
✔ stop → Stops running container
✔ rm → Deletes container

📋 8. View Containers

▶️ Commands

docker ps
docker ps -a

🧠 Concept

✔ docker ps → Running containers
✔ docker ps -a → All containers

📥 9. Image Pulling

▶️ Command

docker pull nginx

🧠 Concept

✔ Downloads image from Docker Hub
✔ Required before running container

⚠️ 10. Common Issues

❗ Issue 1: Build fails

Reason: Wrong Dockerfile syntax
Solution: Check instructions

❗ Issue 2: Large image size

Reason: Unnecessary files
Solution: Use .dockerignore

❗ Issue 3: Slow build

Reason: Large build context
Solution: Optimize files
🧪 11. Practical

▶️ Step 1: Create Dockerfile

FROM nginx:alpine
COPY index.html /usr/share/nginx/html/

▶️ Step 2: Build Image

docker build -t myweb:v1 .

▶️ Step 3: Run Container

docker run -d -p 8080:80 myweb:v1

▶️ Step 4: Verify

Open browser → http://localhost:8080

💡 12. Key Learnings

✔ Dockerfile automates image creation
✔ Layering improves performance
✔ Build context must be optimized
✔ .dockerignore reduces unnecessary files

❓ 13. Doubts
Difference between RUN and CMD?
Why layering improves performance?
What happens if Dockerfile changes?
🔥 14. Summary

Action Result
Dockerfile Automates image creation
docker build Creates image
Layers Improve performance
Port Mapping Exposes container
Container Naming Easy identification
docker ps View containers
docker pull Download images
