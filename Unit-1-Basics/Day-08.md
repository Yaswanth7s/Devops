# 📅 Day 08 - Container Images & Layers (Detailed Notes)

## 📚 Topics Covered

* What is a Container Image
* Structure of Docker Images
* Image Layers
* Working of Layers

---

# 🧠 1. What is a Container Image?

A **container image** is a lightweight, standalone package that contains:

* Application code
* Libraries
* Dependencies
* Configuration files

👉 It is used to create containers.

---

## 📌 Simple Definition

👉 Image = Blueprint of a container

---

## 🎯 Example

* `nginx` image → used to create Nginx container
* `mysql` image → used to create MySQL container

---

# ⚙️ 2. Structure of Docker Image

A Docker image is made up of **multiple layers** stacked together.

👉 Each layer represents a change or instruction.

---

# 🧩 3. What are Image Layers?

Image layers are **read-only units** that form a Docker image.

---

## 🔍 How Layers are Created

Each instruction in Dockerfile creates a layer:

Example:

```dockerfile
FROM ubuntu
RUN apt update
RUN apt install nginx
COPY . /app
```

👉 Each line = one layer

---

## 📊 Layer Stack

```
Layer 4 → COPY files
Layer 3 → Install nginx
Layer 2 → apt update
Layer 1 → Base OS (ubuntu)
```

---

# ⚡ 4. Features of Layers

### 🔹 1. Read-Only

* Layers cannot be modified
* New changes create new layers

---

### 🔹 2. Reusability

* Layers can be reused across images
* Saves storage

---

### 🔹 3. Caching

* Docker caches layers
* Speeds up build process

---

### 🔹 4. Efficiency

* Only changed layers are updated
* Faster image builds

---

# 🔄 5. How Containers Use Layers

When a container is created:

* All image layers are combined
* A new **writable layer** is added on top

👉 This allows runtime changes without modifying image

---

# 📦 6. Writable Layer (Important)

* Container adds its own writable layer
* Stores runtime changes
* Deleted when container is removed

---

# 💡 Key Learnings

* Images are built using layers
* Layers improve efficiency and speed
* Containers use image + writable layer

---

# 🛠️ Practical Understanding

* Observed image layers using docker history
* Understood layer-based architecture

---

# 🧾 Summary

* Image = blueprint of container
* Built using multiple layers
* Layers are reusable and efficient
* Containers add a writable layer
