# 📅 Day 13 - Environment Variables Lifecycle in Docker (Hands-on + Internal Working)

---

## 📚 Topics Covered

- Running Ubuntu container with environment variables
- Checking variables inside container
- Container stop/start behavior
- Effect of container deletion
- Internal working of environment variables
- Using `docker inspect` to verify variables

---

## 🐳 1. Run Ubuntu Container with Environment Variable

### ✅ Command

```bash
docker run -it --name myubuntu -e COLLEGE=CSE ubuntu bash
```

---

### 🔍 Explanation

- `-it` → Runs container in interactive terminal mode  
- `--name myubuntu` → Assigns container name  
- `-e COLLEGE=CSE` → Sets environment variable inside container  
- `ubuntu bash` → Starts Ubuntu container with bash shell  

---

## 🧪 2. Check Inside Container

### ▶️ Command

```bash
echo $COLLEGE
```

### ✅ Output

```
CSE
```

---

### 🧠 Concept

✔️ Environment variables exist **inside the container process**  
✔️ They are available to all processes running in that container  

---

## 🛑 3. Stop the Container

### Method 1: From Inside Container

```bash
exit
```

### Method 2: From Another Terminal

```bash
docker stop myubuntu
```

---

## 🔍 4. Start Container Again and Check

### ▶️ Command

```bash
docker start -ai myubuntu
```

Now check:

```bash
echo $COLLEGE
```

---

### ❗ Output

```
CSE
```

---

## 🧠 WHY? (Important Concept)

Environment variables passed using `-e` are:

- Stored in **container configuration**  
- Persist across **stop/start**  
- ❌ Do NOT persist after container deletion  

---

## 💣 5. Remove Container and Observe

### ▶️ Remove Container

```bash
docker rm myubuntu
```

---

### ▶️ Run New Container (Without `-e`)

```bash
docker run -it ubuntu bash
echo $COLLEGE
```

---

### ❌ Output

```
(empty)
```

---

### 🧠 Concept

- Environment variables are **not stored in image**
- They must be provided again during container creation

---

## 🔥 Final Summary (Exam Ready)

| Action                          | Result                      |
|--------------------------------|----------------------------|
| `docker run -e`                | Sets environment variable  |
| `docker stop / start`          | Variable persists ✅        |
| `docker rm`                    | Variable lost ❌           |
| New container without `-e`     | Variable not available     |

---

## ⚡ Pro Tip (Interview Level)

### 🔍 Check Environment Variables Without Entering Container

```bash
docker inspect myubuntu
```

---

### 📌 Look for

```
"Env": ["COLLEGE=CSE"]
```

---

## 💡 Key Learnings

- Environment variables are part of container configuration  
- They persist across restart but not deletion  
- `-e` flag is required during container creation  
- `docker inspect` helps verify internal container details  

---
