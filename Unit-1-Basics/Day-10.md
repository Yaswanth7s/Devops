# 📅 Day 10 - docker run -it and Important Options (Detailed Notes)

## 📚 Topics Covered

* docker run -it command
* Interactive mode
* Terminal access inside container
* Important docker run options

---

# 🐳 15. docker run -it <image-name>

## 📌 Definition

The `docker run -it` command is used to **run a container in interactive mode with a terminal**.

👉 It allows the user to **interact directly with the container**.

---

## 🛠️ Syntax

```bash
docker run -it <image-name>
```

---

## 📊 Example

```bash
docker run -it ubuntu
```

---

## 🔍 Explanation of Options

| Option | Meaning                             |
| ------ | ----------------------------------- |
| -i     | Interactive mode (keeps STDIN open) |
| -t     | Allocates a terminal (TTY)          |

---

## 🎯 What Happens?

* A container is created
* Terminal is opened inside container
* You can type commands directly

---

## 💻 Example Interaction

```bash
docker run -it ubuntu
```

Inside container:

```bash
ls
pwd
whoami
```

👉 You are now working inside the container

---

# ⚙️ Why -it is Used

* To access container shell
* To run commands manually
* To debug containers

---

# 🔥 Important docker run Options (Extended)

---

## 🔹 1. -d (Detached Mode)

```bash
docker run -d nginx
```

👉 Runs container in background

---

## 🔹 2. --name

```bash
docker run --name mycontainer nginx
```

👉 Assigns custom name to container

---

## 🔹 3. -p (Port Mapping)

```bash
docker run -p 8080:80 nginx
```

👉 Maps host port to container port

---

## 🔹 4. -it (Interactive Terminal)

```bash
docker run -it ubuntu
```

👉 Opens terminal inside container

---

## 🔹 5. --rm

```bash
docker run --rm ubuntu
```

👉 Automatically removes container after exit

---

## 🔹 6. -v (Volume Mount)

```bash
docker run -v /host:/container nginx
```

👉 Mounts host directory into container

---

## 🔹 7. -e (Environment Variable)

```bash
docker run -e MY_VAR=hello ubuntu
```

👉 Sets environment variables

---

## 🔹 8. --network

```bash
docker run --network bridge nginx
```

👉 Connects container to network

---

# 🧠 Combined Example (Very Important)

```bash
docker run -it --name yashu-container -p 8080:80 ubuntu
```

👉 This command:

* Runs container interactively
* Assigns name
* Maps port
* Opens terminal

---

# ⚠️ Important Notes

* Without `-it`, no terminal access
* Used mainly with images like ubuntu, alpine
* Not used for background services like nginx

---

# 🛠️ Practical Understanding

* Accessed container using terminal
* Executed commands inside container
* Understood interactive mode

---

# 💡 Key Learnings

* `-it` allows direct interaction with container
* Useful for debugging and learning
* Can combine with other options

---

# ❓ Doubts

* Difference between -it and -d

---

# 🧾 Summary

* docker run -it → interactive terminal
* -i → keeps input open
* -t → provides terminal
* Used to run commands inside container
