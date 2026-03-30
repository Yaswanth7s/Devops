# 📅 Day 06 - Docker Container Commands (Detailed Notes)

## 📚 Topics Covered

* Running containers
* Executing commands inside containers
* Naming containers
* Stopping and removing containers
* Listing containers

---

# 🐳 6. docker run <image-name>

## 📌 Definition

The `docker run` command is used to **create and start a container from a Docker image**.

---

## 🛠️ Syntax

```bash
docker run <image-name>
```

---

## 📊 Example

```bash
docker run httpd
```

---

## 🔄 What Happens Internally?

1. Docker checks if image exists locally
2. If not → pulls image from Docker Hub
3. Creates a new container
4. Starts the container

---

## 🎯 Purpose

* Run applications inside containers
* Start services like web servers

---

## 💡 Key Point

👉 `docker run` = **pull + create + start container**

---

# 💻 7. docker run httpd echo "Hello world"

## 📌 Definition

This command runs a container and **executes a custom command instead of default behavior**.

---

## 🛠️ Syntax

```bash
docker run <image-name> <command>
```

---

## 📊 Example

```bash
docker run httpd echo "Hello world"
```

---

## 🔍 Explanation

* Normally `httpd` starts Apache server
* Here, default command is overridden
* Container runs `echo "Hello world"`
* Prints output and exits immediately

---

## 🎯 Purpose

* Run temporary tasks
* Execute custom commands inside containers

---

## 💡 Key Point

👉 Container stops after command execution is complete

---

# 🏷️ 8. docker run --name <container-name> <image> <command>

## 📌 Definition

This command creates a container with a **custom name** and runs a command inside it.

---

## 🛠️ Syntax

```bash
docker run --name <container-name> <image-name> <command>
```

---

## 📊 Example

```bash
docker run --name yashcontainer httpd echo "Hello world"
```

---

## 🎯 Purpose

* Easily identify containers
* Avoid random container names

---

## 💡 Key Point

👉 Naming helps in managing containers easily

---

# ⛔ 9. docker stop <container-name or id>

## 📌 Definition

Stops a running container **gracefully**.

---

## 🛠️ Syntax

```bash
docker stop <container-name>
```

---

## 🔄 What Happens Internally?

1. Docker sends **SIGTERM signal**
2. Gives container time to stop (default 10 sec)
3. If not stopped → sends **SIGKILL** (force stop)

---

## 🎯 Purpose

* Safely stop running containers

---

## 💡 Key Point

👉 Always prefer `docker stop` before removing container

---

# 🗑️ 10. docker rm <container-name or id>

## 📌 Definition

Removes (deletes) a container from Docker.

---

## 🛠️ Syntax

```bash
docker rm <container-name>
```

---

## ⚠️ Important Rule

👉 Container must be **stopped first**

---

## 🎯 Purpose

* Clean unused containers
* Free system resources

---

## 💡 Key Point

👉 Cannot remove running container

---

# ⚡ 11. docker rm -f <container-name>

## 📌 Definition

Forcefully removes a container.

---

## 🛠️ Syntax

```bash
docker rm -f <container-name>
```

---

## 🔍 What -f Means

* Stops container (if running)
* Removes it immediately

---

## 🎯 Purpose

* Quick cleanup
* No need to stop manually

---

## 💡 Key Point

👉 `-f` = force (stop + remove)

---

# 🔄 12. docker run -d <image-name>

## 📌 Definition

Runs a container in **detached (background) mode**.

---

## 🛠️ Syntax

```bash
docker run -d <image-name>
```

---

## 📊 Example

```bash
docker run -d httpd
```

---

## 🎯 Purpose

* Run services in background
* Keep terminal free

---

## 💡 Key Point

👉 Used for servers like Nginx, Apache

---

# 📋 13. docker ps

## 📌 Definition

Displays all **currently running containers**.

---

## 🛠️ Syntax

```bash
docker ps
```

---

## 📊 Output Shows

* Container ID
* Image used
* Status
* Ports
* Names

---

## 🎯 Purpose

* Monitor active containers

---

## 💡 Key Point

👉 Shows only running containers

---

# 📦 14. docker ps -a

## 📌 Definition

Displays **all containers** in Docker.

---

## 🛠️ Syntax

```bash
docker ps -a
```

---

## 📊 Includes

* Running containers
* Stopped containers
* Exited containers

---

## 🎯 Purpose

* View complete container history

---

## 💡 Key Point

👉 Use this to check stopped containers

---

# 🛠️ Practical

* Ran containers using docker run
* Executed custom commands
* Named containers
* Stopped and removed containers
* Listed running and all containers

---

# 💡 Key Learnings

* `docker run` creates and starts containers
* Containers can run custom commands
* Containers must be stopped before removing
* `docker ps` helps track containers
* `-d` runs containers in background

---

# ❓ Doubts

* Difference between container lifecycle states

---

# 🧾 Summary

* docker run → Create and start container
* docker stop → Stop container
* docker rm → Remove container
* docker rm -f → Force remove container
* docker ps → Show running containers
* docker ps -a → Show all containers
