📅 Day 14 - Dockerfile Basics & Core Concepts (Detailed Notes)
📚 Topics Covered
What is Dockerfile
Image layering
Build context
.dockerignore
Basic instructions (FROM, RUN, COPY, CMD)
🐳 1. What is a Dockerfile?

📌 Definition

A Dockerfile is a text file that contains a set of instructions to automatically build a Docker image.

🧠 Concept

Automates image creation
Ensures consistency across environments
Used in CI/CD pipelines
🧱 2. Image Layering Concept

📌 Each instruction in Dockerfile creates a separate layer

FROM ubuntu
RUN apt update
RUN apt install -y nginx

🧠 Concept

Layers are cached
Faster rebuilds
Reusability of layers
📦 3. Basic Dockerfile Example
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
CMD ["nginx", "-g", "daemon off;"]
🔍 4. Build Context
docker build -t myapp:v1 .

🧠 Concept

. means current directory
All files are sent to Docker daemon
🚫 5. .dockerignore

📌 Used to exclude unnecessary files

node_modules
.git
.env
🔥 Final Summary (Exam Ready)
Concept	Purpose
Dockerfile	Automates image creation
Layers	Improves build speed
Build context	Files sent to Docker
.dockerignore	Excludes files
