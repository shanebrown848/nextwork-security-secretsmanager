# 🔐 Nextwork Security: Secrets Manager Integration

Securely manage AWS credentials in your Python web applications using **AWS Secrets Manager**.

This project demonstrates how to replace hardcoded AWS credentials with secure retrieval from Secrets Manager—enhancing security and following AWS best practices.

---

## 🚀 Features

- 🔑 Secure AWS credential access via Secrets Manager
- 🐍 Built with Python + Flask
- 🐳 Dockerized for easy deployment
- 🛡️ Emphasizes best practices in secrets handling

---

## 🛠️ Tech Stack

- **Backend:** Python, Flask  
- **Cloud:** AWS (Secrets Manager, IAM)  
- **DevOps:** Docker  
- **Version Control:** Git + GitHub

---

## 📦 Installation & Setup

### 1. Clone the Repo

```bash
git clone https://github.com/shanebrown848/nextwork-security-secretsmanager.git
cd nextwork-security-secretsmanager
````

### 2. Set Up AWS Secrets Manager

Create a new secret in **AWS Secrets Manager** containing your credentials:

* Access Key
* Secret Key

Take note of your **Secret Name** and **AWS Region**.

### 3. Set Environment Variables

```bash
export SECRET_NAME=your-secret-name
export AWS_REGION=your-region
```

(You can also use a `.env` file if preferred.)

### 4. Run with Docker

```bash
docker build -t secrets-manager-app .
docker run -p 5000:5000 \
  -e SECRET_NAME=$SECRET_NAME \
  -e AWS_REGION=$AWS_REGION \
  secrets-manager-app
```

Visit `http://localhost:5000` in your browser.

---

## 🧪 Usage

Once running, the app fetches AWS credentials securely from Secrets Manager and lists S3 buckets associated with the credentials.


---

## 📜 License

MIT License – use freely, improve freely. ✌️

---

## 🙏 Acknowledgments

* AWS Documentation for Secrets Manager
* Flask for being awesome
* Nextwork.org for the project inspiration

---

> 🔒 Always remember: Never hardcode your secrets. Ever.

