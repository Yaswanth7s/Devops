# 📅 Day 09 - Image Registries & Distribution (Detailed Notes)

## 📚 Topics Covered

* What is Image Registry
* Docker Hub
* Private Registries
* Image Distribution Process

---

# 🧠 1. What is an Image Registry?

An **image registry** is a storage system used to store and distribute Docker images.

👉 It is like a **repository for images**.

---

## 📌 Simple Definition

👉 Registry = place where images are stored

---

## 🎯 Example

* Docker Hub
* GitHub Container Registry

---

# 🌐 2. Docker Hub

Docker Hub is the **default public registry**.

---

## 🔹 Features

* Stores public images
* Provides official images
* Easy to use
* Accessible worldwide

---

## 📊 Example Images

* nginx
* mysql
* ubuntu

---

# 🔐 3. Private Registries

Private registries are used to store **secure and private images**.

---

## 🎯 Why Needed?

* Protect company data
* Store custom images
* Control access

---

## 📌 Examples

* GitHub Container Registry (GHCR)
* Self-hosted registry

---

# 🔄 4. Image Distribution Process

---

## 📥 Pull Process

```bash
docker pull nginx
```

👉 Steps:

1. Request image from registry
2. Download layers
3. Store locally

---

## 📤 Push Process

```bash
docker push myimage
```

👉 Steps:

1. Upload image layers
2. Store in registry
3. Make available for others

---

# 📊 5. Flow of Image Distribution

```
Developer → Build Image → Push to Registry → Pull → Run Container
```

---

# 🎯 6. Importance in DevOps

* Enables sharing of images
* Supports CI/CD pipelines
* Ensures consistency
* Simplifies deployment

---

# 💡 Key Learnings

* Registry stores Docker images
* Docker Hub is public registry
* Private registries provide security
* Images are shared using push and pull

---

# 🛠️ Practical Understanding

* Pulled images from Docker Hub
* Understood image distribution flow

---

# 🧾 Summary

* Image registry stores images
* Docker Hub is default registry
* Images are distributed using push/pull
* Important for DevOps workflows
