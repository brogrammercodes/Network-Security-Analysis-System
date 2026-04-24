```markdown
## 🔐 Deployment & Setup (AWS + Docker)

### 📌 GitHub Secrets Configuration
Set the following secrets in your GitHub repository:

```

AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key
AWS_REGION=us-east-1
AWS_ECR_LOGIN_URI=788614365622.dkr.ecr.us-east-1.amazonaws.com/networkssecurity
ECR_REPOSITORY_NAME=networkssecurity

````

---

### 🐳 Docker Setup on AWS EC2

Run the following commands on your EC2 instance:

#### 🔄 Update System (Optional)
```bash
sudo apt-get update -y
sudo apt-get upgrade -y
````

#### ⚙️ Install Docker (Required)

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

#### 👤 Grant Docker Permissions

```bash
sudo usermod -aG docker ubuntu
newgrp docker
```

---

### 🚀 Deployment Workflow

1. Build Docker image locally or via CI/CD
2. Push image to AWS ECR
3. Pull and run container on EC2
4. Serve model via API

---

### 🔥 Key Notes

* Ensure AWS IAM user has proper permissions (ECR + EC2)
* Never expose your AWS credentials publicly
* Use GitHub Secrets for secure CI/CD pipelines

```
```
