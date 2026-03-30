# 📅 Day 03 - Introduction to Containers & Container Runtime (Detailed Notes)

## 📚 Topics Covered

* Origin of Containers
* Evolution of Deployment Models
* Emergence of Modern Containerization
* Containers in DevOps
* Container Runtime

---

# 🧠 1. Origin of Containers

In the early days of computing, applications were deployed directly on **physical servers**.

### 🔴 Problem with Physical Servers

* Each server runs only one application
* Hardware resources (CPU, RAM) are underutilized
* Expensive to maintain multiple servers
* Difficult to scale applications

👉 Example:
If you have 5 applications, you need 5 separate servers → inefficient and costly.

---

# 🔄 2. Evolution of Deployment Models

To solve these problems, technology evolved step by step:

---

## 🖥️ Stage 1: Physical Machines

* One application per machine
* No sharing of resources
* High cost and low efficiency

---

## 🏢 Stage 2: Virtual Machines (VMs)

Virtualization was introduced to improve resource utilization.

### ⚙️ How VMs Work

* A **hypervisor** is installed on hardware
* Multiple virtual machines run on top of it
* Each VM has its own operating system

---

### ✅ Advantages of VMs

* Better resource utilization
* Isolation between applications
* Multiple environments on one system

---

### ❌ Limitations of VMs

* Each VM requires a full OS
* High memory and CPU usage
* Slow startup time
* Heavy in size

👉 Example:
Running 5 VMs means running 5 operating systems → resource heavy.

---

## 📦 Stage 3: Containers (Modern Approach)

Containers were introduced to overcome the limitations of virtual machines.

---

# 🚀 3. Emergence of Modern Containerization

Containers provide a lightweight way to run applications.

### ⚙️ How Containers Work

* Containers **share the host operating system**
* Only application and dependencies are packaged
* No need for separate OS per container

---

### ⚡ Key Features of Containers

* **Lightweight** → Uses less memory
* **Fast Startup** → Starts in seconds
* **Portable** → Runs anywhere
* **Efficient** → Better resource utilization
* **Isolated** → Applications run independently

---

### 📊 Containers vs Virtual Machines

| Feature        | Virtual Machines 🏢 | Containers 📦 |
| -------------- | ------------------- | ------------- |
| OS             | Separate OS         | Shared OS     |
| Size           | Large               | Small         |
| Startup Time   | Slow                | Fast          |
| Resource Usage | High                | Low           |

---

### 🏠 Real-Life Analogy

* 🏡 Independent House → Physical Machine
* 🏢 Apartment → Virtual Machines
* 🛏️ PG System → Containers

👉 Containers share resources but maintain isolation.

---

# 🔗 4. Containers in DevOps

Containers are widely used in DevOps because they solve many real-world problems.

---

### 🎯 Benefits in DevOps

* **Consistency**
  → Same application runs everywhere (dev, test, production)

* **Faster Deployment**
  → Containers start quickly

* **Scalability**
  → Easily run multiple containers

* **Automation Support**
  → Works well with CI/CD pipelines

---

### 📌 Why Developers Prefer Containers

* No “works on my machine” problem
* Easy to share applications
* Faster development cycle

---

# ⚙️ 5. What is a Container Runtime?

A **container runtime** is software responsible for running containers.

👉 It acts as an engine that executes container images.

---

### 🔧 Responsibilities of Container Runtime

* Pull container images from registry
* Create and start containers
* Stop and delete containers
* Manage resources (CPU, memory)
* Maintain isolation

---

### 📦 How It Works (Simple Flow)

1. Developer creates container image
2. Runtime pulls the image
3. Runtime creates container
4. Application runs inside container

---

### 📌 Examples of Container Runtime

* Docker Engine
* containerd
* CRI-O (advanced)

---

# 🛠️ Practical Understanding

* Learned how containers evolved
* Understood why containers are better than VMs
* Got idea of how container runtime works

---

# 💡 Key Learnings

* Containers are lightweight and efficient
* Virtual machines are heavy due to full OS
* Container runtime manages container execution
* Containers play an important role in DevOps

---

# ❓ Doubts

* Difference between Docker and container runtime
* Internal working of container runtime

---

# 🧾 Final Summary

* Physical systems were inefficient
* Virtual machines improved utilization but were heavy
* Containers provide lightweight and fast solution
* Container runtime is responsible for running containers
* Containers are essential in modern DevOps practices
