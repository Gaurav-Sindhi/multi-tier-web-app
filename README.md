# 🚀 Multi-Tier Web Application Deployment on AWS

## 📌 Overview

This project demonstrates a Multi-Tier Web Application architecture on AWS by separating the application into multiple layers:

* Frontend Layer
* Backend Layer
* Database Layer

The architecture improves scalability, maintainability, and separation of concerns by allowing independent deployment and communication between services.

---

# 🧰 AWS Services Used

* Amazon EC2
* Amazon RDS (MySQL)
* Application Load Balancer (ALB)
* Security Groups

---

# 🏗️ Architecture

```text id="1newmulti"
User
  ↓
Frontend EC2 (Apache)
  ↓
Backend EC2 (Node.js)
  ↓
Amazon RDS (MySQL Database)
```

---

# ⚙️ Features

✅ Frontend and backend separation
✅ Backend API communication
✅ Database layer integration using RDS
✅ Multi-tier architecture deployment
✅ Node.js backend hosting
✅ Apache frontend hosting
✅ AWS cloud deployment

---

# 💻 Frontend Code

## 🟢 Frontend HTML

```html id="2newmulti"
<h1>Frontend Server</h1>

<button onclick="callBackend()">Call Backend</button>

<p id="result"></p>

<script>
function callBackend() {
  fetch("http://15.206.68.19:3000")
    .then(response => response.text())
    .then(data => {
      document.getElementById("result").innerText = data;
    });
}
</script>
```

---

# 💻 Backend Code

## 🟢 app.js

```javascript id="3newmulti"
const http = require('http');

http.createServer((req, res) => {
  res.write("Backend Running");
  res.end();
}).listen(3000);

console.log("Backend running on port 3000");
```

---

# ⚙️ Deployment Workflow

## 1️⃣ Launch Frontend EC2

* Install Apache
* Configure frontend interface

---

## 2️⃣ Launch Backend EC2

* Install Node.js
* Run backend API on port 3000

---

## 3️⃣ Configure Amazon RDS

* Create MySQL database instance
* Configure connectivity and credentials

---

## 4️⃣ Configure Security Groups

* Allow frontend traffic on port 80
* Allow backend traffic on port 3000
* Allow database communication

---

## 5️⃣ Connect Frontend → Backend

* Frontend fetch request calls backend API

---

## 6️⃣ Backend → Database Architecture

* Backend designed to connect with RDS database layer

---

# 📸 Screenshots

## 🔹 Frontend Server Running

![Frontend](screenshots/Screenshot%202026-04-26%20195605.png)

---

## 🔹 Backend Server Running

![Backend](screenshots/Screenshot%202026-04-26%20200848.png)

---

## 🔹 Frontend to Backend Communication

![Frontend Backend](screenshots/Screenshot%202026-04-26%20200911.png)

---

## 🔹 Backend Response in Browser

![Backend Response](screenshots/Screenshot%202026-04-26%20201021.png)

---

## 🔹 AWS Infrastructure Automation using boto3

![AWS Automation](screenshots/Screenshot%202026-04-27%20003815.png)

---

## 🔹 Amazon RDS Database Instance

![RDS Database](screenshots/Screenshot%202026-05-14%20181122.png)

---

# 📊 Results

✅ Frontend deployed successfully
✅ Backend API running successfully
✅ Frontend and backend communication established
✅ Amazon RDS database configured
✅ Multi-tier architecture implemented successfully

---

# 💡 Key Learnings

* Multi-tier cloud architecture
* Frontend/backend separation
* Node.js backend deployment
* Apache web server configuration
* Amazon RDS database setup
* AWS EC2 networking and communication

---

# 🚀 Future Improvements

* Add Auto Scaling
* Add Load Balancer
* Add Docker containerization
* Add CI/CD pipeline
* Add HTTPS using ACM
* Add Terraform automation

---

# 📂 Project Structure

```text id="4newmulti"
multi-tier-web-app/
│── frontend/
│── backend/
│── README.md
│── screenshots/
│     ├── Screenshot 2026-04-26 195605.png
│     ├── Screenshot 2026-04-26 200848.png
│     ├── Screenshot 2026-04-26 200911.png
│     ├── Screenshot 2026-04-26 201021.png
│     ├── Screenshot 2026-04-27 003815.png
│     └── Screenshot 2026-05-14 181122.png
```

---

# 🔗 GitHub Commands

```bash id="5newmulti"
cd "D:\AWS Projects\multi-tier-web-app"

git init
git add .
git commit -m "Multi-Tier Web Application Deployment on AWS"

git branch -M main

git remote add origin https://github.com/Gaurav-Sindhi/multi-tier-web-app.git

git push -u origin main
```

---

# 🎯 Interview Summary

> Built a multi-tier web application architecture on AWS by separating frontend, backend, and database layers using EC2 and Amazon RDS. Implemented API communication between services and deployed applications using Apache and Node.js.

---
