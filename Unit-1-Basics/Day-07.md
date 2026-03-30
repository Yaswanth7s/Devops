# 📅 Day 07 - Process Isolation & Namespaces (Detailed Notes)

## 📚 Topics Covered

* Process Isolation
* Introduction to Namespaces
* Types of Namespaces in Linux
* Role of Namespaces in Containers

---

# 🧠 1. What is Process Isolation?

Process isolation means that **each process runs independently without interfering with other processes**.

👉 In simple terms:
One process cannot see or affect another process.

---

## 🔴 Problem Without Isolation

* One application can access another application’s data
* Security risks
* System instability
* Conflicts between applications

---

## 🟢 Solution: Process Isolation

* Each process runs in its own environment
* Limited visibility of system resources
* Safe and secure execution

---

## 🎯 Example

If two applications are running:

* App A cannot access App B’s memory
* App B cannot interfere with App A

👉 This ensures **security and stability**

---

# 📦 2. What are Namespaces?

Namespaces are a feature of the Linux kernel used to **provide isolation between processes**.

👉 They create separate environments for processes.

---

## 📌 Definition

A namespace limits what a process can see.

👉 Each container has its own namespace.

---

## 🔍 Simple Meaning

👉 Think of namespaces as **invisible boundaries** around processes.

---

# 🏠 Real-Life Analogy

Imagine a hostel:

* Each room → separate namespace
* Students → processes

👉 Each student sees only their room, not others

---

# ⚙️ 3. How Namespaces Work

* The system creates multiple namespaces
* Each process is assigned to a namespace
* Processes can only see resources inside their namespace

---

# 🔗 4. Namespaces in Containers

Containers use namespaces to achieve isolation.

👉 That’s why:

* Each container has its own processes
* Each container behaves like a separate system

---

## 💡 Important Point

👉 Containers are isolated **not because of virtual machines**,
but because of **namespaces + cgroups**

---

# 🧩 5. Types of Namespaces

Linux provides different types of namespaces:

---

## 🔹 1. PID Namespace (Process ID)

* Isolates process IDs
* Each container has its own process numbering

👉 Same PID can exist in different containers

---

## 🔹 2. NET Namespace (Network)

* Provides separate network stack
* Each container has its own:

  * IP address
  * Network interfaces

---

## 🔹 3. MNT Namespace (Mount)

* Isolates file system
* Each container has its own file structure

---

## 🔹 4. IPC Namespace (Inter-Process Communication)

* Isolates communication between processes
* Prevents processes from different containers interacting

---

## 🔹 5. UTS Namespace

* Allows each container to have its own hostname

---

## 🔹 6. USER Namespace

* Controls user and group IDs
* Enhances security

---

# 📊 6. Namespaces vs cgroups

| Feature | Namespaces 🔒      | cgroups ⚙️       |
| ------- | ------------------ | ---------------- |
| Purpose | Isolation          | Resource control |
| Focus   | Visibility         | Usage limits     |
| Example | Separate processes | Limit CPU/memory |

---

# 🎯 7. Why Namespaces are Important

* Provide strong isolation
* Improve security
* Enable containers to run independently
* Make containers lightweight

---

# 🛠️ Practical Understanding

* Learned how containers isolate processes
* Understood role of namespaces in Docker

---

# 💡 Key Learnings

* Namespaces provide isolation
* Each container has its own environment
* Multiple types of namespaces exist
* Essential for container functioning

---

# ❓ Doubts

* How namespaces are implemented internally in Linux

---

# 🧾 Summary

* Process isolation ensures independent execution
* Namespaces provide isolation in Linux
* Containers use namespaces for separation
* Namespaces + cgroups = container foundation
