# 📅 Day 05 - Basic Docker Commands (Detailed Notes)

## 📚 Topics Covered

* Docker version command
* Docker system information
* Docker image history
* Pulling images from Docker Hub
* Listing Docker images

---

# 🐳 1. docker --version

## 📌 Definition

The `docker --version` command is used to **check the installed version of Docker** on your system.

---

## 🛠️ Syntax

```bash
docker --version
```

---

## 📊 Example Output

```
Docker version 24.0.5, build abc123
```

---

## 🎯 Purpose

* Verify Docker installation
* Check which version is running
* Useful for debugging and compatibility

---

## 💡 Key Point

👉 Always run this command after installing Docker to confirm it is working properly.

---

# ⚙️ 2. docker info

## 📌 Definition

The `docker info` command displays **detailed system-wide information** about Docker.

---

## 🛠️ Syntax

```bash
docker info
```

---

## 📊 Information Displayed

* Total number of containers
* Number of running/stopped containers
* Number of images
* Storage driver used
* CPU and memory details
* Docker root directory
* Operating system details

---

## 🎯 Purpose

* Understand Docker environment
* Check system configuration
* Troubleshoot Docker issues

---

## 💡 Key Point

👉 This command gives a **complete overview of Docker setup** on your machine.

---

# 📦 3. docker history <image-name>

## 📌 Definition

The `docker history` command shows how a Docker image was built **layer by layer**.

---

## 🛠️ Syntax

```bash
docker history <image-name>
```

---

## 📊 Example

```bash
docker history httpd
```

---

## 📋 Output Columns Explained

| Column     | Meaning                          |
| ---------- | -------------------------------- |
| IMAGE      | Unique ID of each layer          |
| CREATED    | When the layer was created       |
| CREATED BY | Command used to create the layer |
| SIZE       | Size of that layer               |

---

## 🎯 Purpose

* Understand image structure
* Debug image creation
* Analyze image size

---

## 💡 Key Point

👉 Every Docker image is made up of **multiple layers**, and this command shows those layers.

---

# 📥 4. docker pull <image-name>

## 📌 Definition

The `docker pull` command is used to **download an image from Docker Hub (or registry)** to your local system.

---

## 🛠️ Syntax

```bash
docker pull <image-name>
```

---

## 📊 Example

```bash
docker pull httpd
```

---

## 🔄 What Happens Internally?

1. Docker checks if image exists locally
2. If not → connects to Docker Hub
3. Downloads image layer by layer
4. Stores it locally

---

## 🎯 Purpose

* Get required images before running containers
* Use official or custom images

---

## 💡 Key Point

👉 `docker run` automatically performs `docker pull` if image is not available.

---

# 🖼️ 5. docker images / docker image ls

## 📌 Definition

This command lists all Docker images available on your local system.

---

## 🛠️ Syntax

```bash
docker images
```

OR

```bash
docker image ls
```

---

## 📊 Example Output

```
REPOSITORY   TAG       IMAGE ID       CREATED        SIZE
nginx        latest    abc123         2 days ago     133MB
httpd        latest    def456         3 days ago     150MB
```

---

## 📋 Columns Explained

| Column     | Meaning           |
| ---------- | ----------------- |
| REPOSITORY | Image name        |
| TAG        | Version of image  |
| IMAGE ID   | Unique identifier |
| CREATED    | Creation time     |
| SIZE       | Image size        |

---

## 🎯 Purpose

* View downloaded images
* Manage local images
* Check available versions

---

## 💡 Key Point

👉 Helps you know which images are already available locally.

---

# 🛠️ Practical

* Checked Docker version
* Viewed Docker system information
* Pulled images from Docker Hub
* Listed available images
* Explored image layers using history

---

# 💡 Key Learnings

* Docker commands help manage containers and images
* Images are built using multiple layers
* Docker Hub is used to download images
* System information can be checked using docker info

---

# ❓ Doubts

* Difference between image and container (to be explored further)

---

# 🧾 Summary

* `docker --version` → Check Docker version
* `docker info` → View system details
* `docker history` → See image layers
* `docker pull` → Download images
* `docker images` → List local images
