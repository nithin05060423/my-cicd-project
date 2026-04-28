# my-cicd-project

# 🚀 CI/CD Project using Jenkins

This project demonstrates a basic **CI/CD pipeline** using Jenkins integrated with GitHub.

---

## 📌 Project Overview

* Source Code is hosted on GitHub
* Jenkins pulls the code automatically
* Build process is triggered manually or via webhook
* Demonstrates Continuous Integration (CI)

---

## 🛠️ Technologies Used

* Jenkins
* GitHub
* AWS EC2
* Git

---

## ⚙️ Setup Steps

### 1. Launch EC2 Instance

* Ubuntu Server
* Open ports: 22, 8080

### 2. Install Jenkins

```bash
sudo apt update
sudo apt install openjdk-17-jdk -y
wget https://get.jenkins.io/debian-stable/jenkins_2.492.1_all.deb
sudo apt install ./jenkins_2.492.1_all.deb -y
```

### 3. Start Jenkins

```bash
sudo systemctl start jenkins
sudo systemctl enable jenkins
```

### 4. Access Jenkins

```
http://<EC2-PUBLIC-IP>:8080
```

---

## 🔐 Jenkins Setup

* Install required plugins:

  * Git Plugin
  * GitHub Plugin
  * Pipeline

* Add GitHub credentials using Personal Access Token (PAT)

---

## 🔗 GitHub Integration

* Connect repository in Jenkins
* Configure branch: `main`
* Add build step:
  ```bash
  echo "CI/CD Pipeline Working 🚀"
  ```

---

## 🔁 Webhook Setup

* Add webhook in GitHub:
  ```
  http://<EC2-IP>:8080/github-webhook/
  ```

* Enable:

  * GitHub hook trigger for GITScm polling

---

## ✅ Output

* Jenkins automatically builds project on every push
* Successful integration between GitHub and Jenkins

---

## 📈 Future Improvements

* Add Docker support
* Deploy application automatically
* Use Jenkinsfile (Pipeline as Code)

---

## 👨‍💻 Author

Nithin
