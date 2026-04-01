📅 Day 12 - Using Host Environment Variables & .env Files in Docker
📚 Topics Covered
Passing host environment variables to containers
Using .env file with --env-file
🌍 1. Host Environment Variables
📌 Definition

Host environment variables are variables defined on your local system.
They can be used to dynamically pass values into Docker containers at runtime.

🪟 PowerShell (Windows)

✅ Set Variable

$env:APP_PORT=8080

✅ Access Variable

echo $env:APP_PORT
🎯 Use Case in Docker
$env:APP_PORT=8080
docker run -d -p $env:APP_PORT`:3306 mysql:8
👉 Explanation:
$env:APP_PORT → Host variable
-p $env:APP_PORT:3306 → Maps host port dynamically to container port
📄 2. Using .env File (--env-file)
📌 Definition

A .env file stores environment variables in key=value format.
Docker can read this file using the --env-file flag to set container variables.

🔹 Step 1: Create .env File
MYSQL_ROOT_PASSWORD=root123
MYSQL_DATABASE=college
MYSQL_USER=admin
MYSQL_PASSWORD=admin123
🔹 Step 2: Use .env File in Docker
docker run -d \
  --env-file .env \
  --name mysql-container \
  -p 3306:3306 \
  mysql:8
⚡ Advantages
Cleaner commands (no long -e list)
Reusable configuration across projects
Easy to manage multiple environment variables
Industry standard for DevOps practice
🔄 3. Comparison: -e vs --env-file
Feature	-e (inline)	--env-file
Usage	Inline per variable	Load all from file
Best for	Few variables	Many variables
Readability	Low	High
Reusability	Low	High
💡 Key Learnings
Host variables allow dynamic configuration at runtime
.env file simplifies environment management
--env-file is preferred for multiple variables or team projects
$env:VAR can be used in PowerShell to pass host values
