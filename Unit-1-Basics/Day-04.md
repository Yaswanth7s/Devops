# 📅 Day 04 - Control Groups (cgroups) for Resource Management

## 📚 Topics Covered

* Introduction to Control Groups (cgroups)
* Resource Limiting in Containers
* Importance of cgroups in DevOps

---

# 🧠 1. What are Control Groups (cgroups)?

Control Groups (cgroups) are a feature of the Linux kernel that allows us to **limit, control, and monitor system resources** used by processes.

👉 In simple terms:
cgroups help in controlling **how much CPU, memory, and other resources a process or container can use**.

---

# 🎯 2. Why cgroups are Needed

In a system running multiple applications or containers:

* One process may consume all CPU
* Another may use too much memory
* This affects system performance

👉 To avoid this, cgroups are used.

---

### 🔴 Problem Without cgroups

* No control over resource usage
* System can become slow or crash
* One application can dominate all resources

---

### 🟢 Solution with cgroups

* Limit CPU usage
* Restrict memory usage
* Control disk and network usage
* Ensure fair resource sharing

---

# ⚙️ 3. How cgroups Work

cgroups group processes together and apply limits to that group.

---

### 🔧 Example

Suppose you have 2 applications:

* App A → Needs more CPU
* App B → Needs less CPU

Using cgroups:

* Assign 70% CPU to App A
* Assign 30% CPU to App B

👉 Now both run efficiently without conflict.

---

# 📦 4. cgroups in Containers

Containers use cgroups to control resources.

---

### 🐳 In Docker

When you run a container:

* Docker automatically uses cgroups
* You can set limits like:

```bash
docker run --memory=512m nginx
```

👉 This limits the container to **512 MB RAM**

---

```bash
docker run --cpus=1 nginx
```

👉 This limits the container to **1 CPU core**

---

# 📊 5. Types of Resources Controlled by cgroups

### 🔹 CPU

* Limits how much CPU a process can use

### 🔹 Memory

* Controls RAM usage

### 🔹 Disk I/O

* Controls read/write speed

### 🔹 Network

* Controls bandwidth usage

---

# 🧠 6. Real-Life Analogy

👉 Think of a hostel mess:

* Total food = System resources
* Students = Processes

Without control:

* One student eats everything 😅

With control (cgroups):

* Everyone gets fixed portion

👉 Ensures fairness and stability

---

# 💡 7. Importance in DevOps

cgroups are very important because:

* Ensure system stability
* Improve performance
* Enable efficient container management
* Prevent resource overuse

---

# 🛠️ Practical Understanding

* Learned how resources are controlled in containers
* Understood importance of limiting CPU and memory

---

# 💡 Key Learnings

* cgroups control resource usage
* Used heavily in Docker and containers
* Helps maintain system performance
* Prevents resource overconsumption

---

# ❓ Doubts

* How cgroups work internally in Linux kernel

---

# 🧾 Summary

* cgroups are used to control system resources
* They limit CPU, memory, and other resources
* Containers use cgroups for efficient execution
* Essential for stable and scalable systems
